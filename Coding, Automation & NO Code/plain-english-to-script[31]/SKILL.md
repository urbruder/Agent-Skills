---
name: plain-english-to-script
description: >
  Convert a plain-English task description into a complete, runnable Python or JavaScript/Node.js
  script — no developer needed. Trigger this skill immediately whenever the user describes a
  repetitive task, a workflow they want to automate, or something they do "every day" that feels
  tedious. Covers: file/folder operations, CSV/Excel/JSON data processing, web scraping, API
  calls, email/calendar automation, bulk renaming, scheduled tasks, form submissions, screenshot
  capture, PDF manipulation, Slack/Notion/Airtable integrations, and anything that sounds like
  "I want to automate X". Trigger even when the user doesn't say "script" or "code" — phrases
  like "can Claude just do this automatically", "is there a way to", "every morning I have to…",
  "I keep doing this manually", or "batch process these files" all activate this skill. This is a
  HERO skill: prioritize it over generic code help whenever automation intent is present.
---

# Plain-English to Working Script

Turn any task description into a production-ready, runnable script. The goal: the user copies
it, runs it, and it works — no editing required (unless they *want* to customize).

---

## Step 1 — Understand the task fully before writing

Ask **only what you must** to make the script correct. Never write a script that requires
the user to edit it just to fill in obvious blanks. Here's what to infer vs. ask:

| Info needed | Infer if possible | Ask if not |
|---|---|---|
| Input file path | If they mentioned one, use it | Ask once, concisely |
| Output location | Default to same folder or `./output/` | Only ask if ambiguous |
| File format | From context / extension | Ask if genuinely unclear |
| Auth / API keys | Note as `YOUR_API_KEY` placeholder with comment | — |
| Schedule / frequency | Infer from "every morning" etc. | Only if timing is critical |
| Language preference | Python first unless they said JS/Node | Ask if unclear |

**If the task is clear enough to write a working script, write it — don't interrogate first.**

---

## Step 2 — Choose language

**Default: Python** — easier to read, fewer environment quirks, better library support for
most automation tasks.

**Use JavaScript/Node.js when:**
- User is in a web/frontend context
- Task is browser automation, Puppeteer/Playwright, or web scraping with JS rendering
- User explicitly asks for JS/Node
- Task involves an npm ecosystem tool

---

## Step 3 — Script quality standards

Every script you produce **must** meet all of these:

### ✅ Completeness
- Imports / requires at the top — all of them
- `if __name__ == "__main__":` guard for Python
- A `main()` function (not just top-level logic)
- Handles the happy path fully — no `# TODO` or `# implement this`

### ✅ Robustness
- `try/except` (Python) or `try/catch` (JS) around I/O, network calls, and parsing
- Descriptive error messages that tell the user *what went wrong* and *what to do*
- Validate inputs before processing (file exists, API key set, etc.)
- For batch jobs: skip-and-continue on individual item failure, not full crash

### ✅ Clarity
- At the top: a 2–3 line comment block explaining what the script does and how to run it
- Inline comments on any non-obvious logic
- Named constants for magic values (paths, thresholds, URLs)
- Progress feedback: `print(f"Processing {i}/{total}...")` for loops > a few items

### ✅ Runnable out of the box
- List every dependency in a comment: `# pip install requests pandas openpyxl`
- For JS: `// npm install axios cheerio`
- If the task involves credentials, show exactly how to set them:
  ```python
  # Set your API key: export MY_API_KEY="sk-..."
  API_KEY = os.environ.get("MY_API_KEY", "YOUR_API_KEY_HERE")
  ```

---

## Step 4 — Output format

Structure every response like this:

```
## What this script does
[2-3 sentence plain-English summary of what it will do]

## Install dependencies
[one-liner pip/npm command]

## Script
[full, runnable script in a code block]

## How to run
[exact command: python script.py input.csv]

## Customization tips  ← include only when genuinely useful
[2-4 bullet points on how to tweak the most likely things]
```

---

## Step 5 — Category-specific guidance

Read the relevant section from `references/categories.md` before writing scripts in these areas:

- **Web scraping** → rate limiting, headers, robots.txt note, BeautifulSoup vs Playwright choice
- **Email / calendar** → OAuth vs app passwords, IMAP/SMTP vs API, auth setup steps
- **File operations** → dry-run flag, backup before destructive ops, glob patterns
- **APIs & webhooks** → pagination, retry logic, rate limit handling
- **Scheduling** → cron vs APScheduler vs Task Scheduler (Windows) guidance
- **Data processing** → chunked reading for large files, dtype inference, encoding

> **Always load `references/categories.md` for any script that touches these domains.**

---

## Step 6 — After delivering the script

Close with exactly one of these, whichever fits:

- If the script has an obvious next step: *"Want me to add scheduling so this runs automatically every morning?"*
- If the user might want a GUI: *"Want a simple menu so non-technical teammates can run this too?"*
- If the output could feed another tool: *"Want me to chain this with a Slack notification when it finishes?"*

Don't offer all three. Pick the most natural one. If none fit, skip this entirely.

---

## Guardrails

- **Never produce a script that deletes files without a dry-run flag or confirmation prompt.** Add `--dry-run` by default.
- **For scripts reading credentials**, always use environment variables — never hardcode.
- **If the task is ambiguous and could destroy data**, ask before writing.
- **Do not produce scripts that scrape sites in violation of their ToS in bad faith** — add a note if relevant.
