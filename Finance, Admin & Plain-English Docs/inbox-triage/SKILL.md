---
name: inbox-triage
description: >
  Triage a messy inbox and produce prioritized, ready-to-send reply drafts — no copy-editing
  needed. Trigger this skill immediately whenever the user shares emails, pastes email threads,
  mentions inbox overload, or asks for help responding to messages. Also trigger for phrases like
  "help me clear my inbox", "draft replies to these", "what do I need to respond to", "I have X
  unread emails", "here are some emails I need to deal with", or "can you go through my emails".
  Works with raw pasted email text, forwarded threads, Gmail/Outlook connected tools, or even
  rough descriptions of what's in the inbox. Produces: a priority-sorted triage table, a
  recommended action per email (Reply / Action / Archive / Delegate / Snooze), and a ready-to-send
  draft for every email that needs a response. This is a HERO skill: use it any time inbox
  management, email replies, or message drafting is the primary task.
---

# Inbox Triage & Reply Drafts

The goal: user hands over their inbox (pasted threads, a dump, a connected Gmail/Outlook tool),
and gets back a prioritized action plan + ready-to-send drafts. They should be able to go from
overwhelmed to done in one sitting.

---

## Step 0 — Detect input mode and gather what you need

**Connected email tool available (Gmail / Outlook MCP):**
→ Fetch the inbox directly. Grab the 20–30 most recent unread messages. Summarize subject +
  sender + first 2 lines. Don't ask the user to paste anything.

**Emails pasted or uploaded:**
→ Parse each email from the text. Treat each `From:` / `Subject:` block as a new message.
  Handle messy formatting — people copy-paste sloppily.

**Rough description only ("I have emails from my landlord, a client named Sara, and HR"):**
→ Draft based on the described context; flag that drafts may need light editing since you
  don't have the actual text.

**What to infer vs. ask:**

| Needed | Infer | Ask |
|---|---|---|
| User's name / sign-off | From emails if visible, else skip | Only if drafts feel off without it |
| User's role / company | From email context | Only if needed to sound right |
| Tone preference | Match the thread's existing tone | Only if wildly mixed signals |
| Urgency | From subject, deadlines, sender type | — |
| Language | Match the thread's language | — |

**Never interrogate before starting.** If you have enough to produce useful output, do it.

---

## Step 1 — Triage: classify every email

For each email, assign:

**Priority tier:**
- 🔴 **Urgent** — deadline today/tomorrow, waiting on you to unblock someone, escalation
- 🟡 **Soon** — needs response within a few days, project-relevant, relationship-important
- 🟢 **Low** — FYI, newsletters, automated notifications, can wait a week+

**Action:**
- **Reply** — needs a written response from the user
- **Action** — requires the user to *do* something (book a meeting, send a file, fill a form)
- **Delegate** — should go to someone else; note who
- **Archive** — no response needed, safe to dismiss
- **Snooze** — relevant later but not now; note when

**Time to handle:** estimated minutes (reply drafting doesn't count — that's done for them)

---

## Step 2 — Output the triage table

Always lead with the triage table before any drafts. Format:

```
## 📥 Inbox Triage — [N] emails

| # | From | Subject | Priority | Action | Est. |
|---|------|---------|----------|--------|------|
| 1 | Sara Chen | Re: contract review | 🔴 Urgent | Reply | 2 min |
| 2 | IT Helpdesk | Password reset | 🟢 Low | Archive | — |
...

**Total action time (excl. drafts): ~12 min**
```

Then a one-line triage note for each that needs context:
> "1. Sara is waiting on your sign-off before she can proceed — draft below."
> "3. This can be safely ignored; it's an automated Jira notification."

---

## Step 3 — Draft every Reply email

For **every email marked Reply**, produce a draft immediately below the triage table.
Don't make the user ask. Don't say "I can write this if you want."

### Draft format

```
---
### ✉️ Reply to: [Name] — "[Subject]"
**Send when:** [Now / After you check X / Once you confirm Y]

[Draft body]

[Sign-off],
[User's name or "Your name"]
---
```

### Draft quality standards

**Tone matching** — read the email carefully and mirror it:
- Casual internal message → conversational, no formalities
- Client / external professional → polished but warm
- Tense or escalatory thread → calm, neutral, de-escalating
- Technical colleague → direct and specific, skip pleasantries

**Length** — match the situation:
- Simple acknowledgment / confirmation → 2–4 lines
- Answering a question → as long as needed, no fluff
- Declining / delivering bad news → brief, warm, clear
- Complex negotiation → structured, with clear asks

**Always include:**
- Direct answer to whatever they asked (don't hedge around it)
- Any explicit next steps or what you need from them
- A clear close — no dangling "let me know" without saying what to let you know

**Never include:**
- "I hope this email finds you well" — skip all filler openers
- Restating what they said back to them
- Apologies for response time unless the delay was genuinely significant
- Overlong sign-offs

**If information is missing to give a real answer**, write the best draft you can and add a
`[YOUR NOTE: …]` placeholder for the specific gap. Never write a draft that's just
placeholders.

---

## Step 4 — Handle Action / Delegate items

After drafts, add a short **Action Items** section:

```
## ✅ Action Items

- [ ] **[Email #]** [What to do] — [by when if known]
- [ ] **[Email #]** Forward to [Name] with: "[suggested message]"
```

Keep this tight — it's a checklist, not a summary.

---

## Step 5 — Closing line

After all drafts, add exactly one line:

> *"All [N] replies drafted. Review, tweak names/details in `[brackets]`, and send."*

If there were no reply-needed emails:
> *"Nothing urgent needs a reply — [N] items archived/snoozed."*

Don't add anything else after this. No "let me know if you need changes."

---

## Tone & style defaults by context

Load `references/tone-patterns.md` when:
- The thread involves conflict, complaints, or sensitive HR/legal language
- The user is drafting to a senior executive or board-level contact
- The email is in a language other than English
- The user mentions a specific tone ("be firm", "keep it warm", "don't sound annoyed")

---

## Guardrails

- **Never send or modify emails directly** unless the user explicitly says "send this". Draft only.
- **Don't summarize emails you haven't read** — if you don't have the content, say so and ask.
- **Don't fabricate context** — if you don't know a deadline or a name, use `[date]` / `[their name]` and flag it.
- **Sensitive threads** (legal, HR, medical, financial): draft conservatively, add a note
  like: *"⚠️ Suggest reviewing with [legal/HR/your advisor] before sending."*
- **If the inbox is connected via MCP**: confirm before reading — "I can access your Gmail.
  Should I pull recent unread messages?"
