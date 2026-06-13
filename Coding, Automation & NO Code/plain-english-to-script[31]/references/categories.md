# Category Reference: Plain-English to Script

Quick-reference patterns and gotchas for common automation categories.

---

## File & Folder Operations

**Always include a dry-run mode for destructive operations:**
```python
import argparse
parser = argparse.ArgumentParser()
parser.add_argument("--dry-run", action="store_true", help="Preview changes without applying them")
args = parser.parse_args()

if args.dry_run:
    print(f"[DRY RUN] Would rename: {old} → {new}")
else:
    os.rename(old, new)
```

**For bulk rename / move / delete:**
- Always print a summary before doing anything: "Found 47 files. Proceeding..."
- Log what was done to a `operation_log.txt` in the output folder
- Use `pathlib.Path` over `os.path` (cleaner, more Pythonic)

**Glob patterns cheatsheet:**
```python
from pathlib import Path
list(Path("folder").glob("*.csv"))         # direct children only
list(Path("folder").rglob("*.csv"))        # recursive
list(Path("folder").glob("report_*.xlsx")) # prefix match
```

---

## CSV / Excel / JSON Data Processing

**Deps:** `pip install pandas openpyxl xlrd`

**Chunked reading for large files (>100k rows):**
```python
for chunk in pd.read_csv("big.csv", chunksize=10_000):
    process(chunk)
```

**Encoding issues (common with non-ASCII data):**
```python
pd.read_csv("file.csv", encoding="utf-8-sig")  # handles BOM from Excel exports
```

**Writing Excel with formatting:**
```python
with pd.ExcelWriter("output.xlsx", engine="openpyxl") as writer:
    df.to_excel(writer, index=False, sheet_name="Results")
```

**JSON with nested structures:**
```python
import json
from pandas import json_normalize
with open("data.json") as f:
    data = json.load(f)
df = json_normalize(data, record_path=["items"])  # flatten nested arrays
```

---

## Web Scraping

**Deps:** `pip install requests beautifulsoup4 lxml`  
**For JS-rendered pages:** `pip install playwright` + `playwright install chromium`

**Always include:**
```python
import time
HEADERS = {"User-Agent": "Mozilla/5.0 (compatible; research-bot/1.0)"}

# Rate limiting — be a good citizen
time.sleep(1)  # between requests
```

**Static pages → requests + BeautifulSoup:**
```python
import requests
from bs4 import BeautifulSoup

resp = requests.get(url, headers=HEADERS, timeout=10)
resp.raise_for_status()
soup = BeautifulSoup(resp.text, "lxml")
```

**JS-rendered pages → Playwright:**
```python
from playwright.sync_api import sync_playwright

with sync_playwright() as p:
    browser = p.chromium.launch(headless=True)
    page = browser.new_page()
    page.goto(url)
    page.wait_for_load_state("networkidle")
    content = page.content()
    browser.close()
```

**Note to include in output:**  
> Always check a site's `robots.txt` and Terms of Service before scraping. This script is for personal/research use.

---

## API Calls & Webhooks

**Deps:** `pip install requests`

**Retry with backoff (for flaky APIs):**
```python
import time
import requests
from requests.adapters import HTTPAdapter
from urllib3.util.retry import Retry

session = requests.Session()
retry = Retry(total=3, backoff_factor=1, status_forcelist=[429, 500, 502, 503])
session.mount("https://", HTTPAdapter(max_retries=retry))
```

**Pagination pattern:**
```python
results = []
page = 1
while True:
    resp = session.get(url, params={"page": page, "per_page": 100})
    data = resp.json()
    if not data["items"]:
        break
    results.extend(data["items"])
    page += 1
```

**Rate limit handling:**
```python
if resp.status_code == 429:
    wait = int(resp.headers.get("Retry-After", 60))
    print(f"Rate limited. Waiting {wait}s...")
    time.sleep(wait)
```

**Webhooks (receive):** Use `flask` or `fastapi` with `ngrok` for local testing.

---

## Email Automation

**Gmail App Password (simpler than OAuth for personal use):**
1. Enable 2FA on Google account
2. Go to myaccount.google.com → Security → App passwords
3. Generate password for "Mail"

**Send email via SMTP:**
```python
import smtplib
from email.mime.text import MIMEText
from email.mime.multipart import MIMEMultipart

def send_email(to, subject, body, from_addr, password):
    msg = MIMEMultipart()
    msg["From"] = from_addr
    msg["To"] = to
    msg["Subject"] = subject
    msg.attach(MIMEText(body, "html"))
    
    with smtplib.SMTP_SSL("smtp.gmail.com", 465) as server:
        server.login(from_addr, password)
        server.send_message(msg)
```

**Read email via IMAP:**
```python
import imaplib
import email

with imaplib.IMAP4_SSL("imap.gmail.com") as mail:
    mail.login(user, password)
    mail.select("inbox")
    _, msg_ids = mail.search(None, 'UNSEEN')
    for mid in msg_ids[0].split():
        _, data = mail.fetch(mid, "(RFC822)")
        msg = email.message_from_bytes(data[0][1])
```

**For Microsoft 365/Outlook:** Use `O365` library (`pip install O365`) — handles OAuth cleanly.

---

## Scheduling

**One-time setup, runs forever → APScheduler (Python):**
```python
# pip install apscheduler
from apscheduler.schedulers.blocking import BlockingScheduler

scheduler = BlockingScheduler()

@scheduler.scheduled_job("cron", hour=8, minute=0)  # every day at 8am
def job():
    run_task()

scheduler.start()
```

**System-level (recommended for production):**

*macOS/Linux — cron:*
```
# crontab -e
0 8 * * *  /usr/bin/python3 /path/to/script.py >> /tmp/script.log 2>&1
```

*Windows — Task Scheduler:*
```
schtasks /create /tn "MyScript" /tr "python C:\path\script.py" /sc daily /st 08:00
```

**Note:** Always use absolute paths in cron/Task Scheduler entries.

---

## PDF Manipulation

**Deps:** `pip install pypdf reportlab`  
**For reading complex PDFs:** `pip install pdfplumber`

**Extract text:**
```python
import pdfplumber

with pdfplumber.open("file.pdf") as pdf:
    for page in pdf.pages:
        text = page.extract_text()
        table = page.extract_table()  # returns list of lists
```

**Merge PDFs:**
```python
from pypdf import PdfWriter

writer = PdfWriter()
for path in pdf_paths:
    writer.append(path)
with open("merged.pdf", "wb") as f:
    writer.write(f)
```

---

## Browser Automation (Playwright / Selenium)

**Prefer Playwright** — more reliable, better async support, handles modern SPAs.

**Deps:** `pip install playwright` → `playwright install chromium`

```python
from playwright.sync_api import sync_playwright

with sync_playwright() as p:
    browser = p.chromium.launch(headless=False)  # headless=True for prod
    context = browser.new_context()
    page = context.new_page()
    
    page.goto("https://example.com/login")
    page.fill("#username", "user@example.com")
    page.fill("#password", os.environ["SITE_PASSWORD"])
    page.click("button[type=submit]")
    page.wait_for_url("**/dashboard")
    
    # Take screenshot
    page.screenshot(path="dashboard.png")
    browser.close()
```

**For form filling at scale:** Use `page.evaluate()` to inject data directly into inputs if normal fill is slow.

---

## Slack / Discord / Telegram Bots

**Slack (send message to webhook):**
```python
# pip install requests
# Set up: Slack → Apps → Incoming Webhooks
import requests

def notify_slack(webhook_url: str, message: str):
    resp = requests.post(webhook_url, json={"text": message})
    resp.raise_for_status()
```

**Slack (full bot with slash commands):** `pip install slack_bolt`

**Discord webhook:**
```python
requests.post(webhook_url, json={"content": message})
```

**Telegram bot:**
```python
# pip install python-telegram-bot
from telegram import Bot
bot = Bot(token=os.environ["TELEGRAM_TOKEN"])
await bot.send_message(chat_id=CHAT_ID, text=message)
```

---

## Node.js / JavaScript Patterns

**File system:**
```javascript
const fs = require('fs').promises;
const path = require('path');

const files = await fs.readdir('./input');
for (const file of files) {
  const full = path.join('./input', file);
  const content = await fs.readFile(full, 'utf8');
}
```

**HTTP requests:** Use `axios` (`npm install axios`) over `node-fetch` for better error handling.

**CSV:** `npm install csv-parse csv-stringify`

**Excel:** `npm install exceljs`

**CLI args:** Use `process.argv` or `npm install commander` for flags.

**Always include:**
```javascript
process.on('uncaughtException', (err) => {
  console.error('Fatal error:', err.message);
  process.exit(1);
});
```
