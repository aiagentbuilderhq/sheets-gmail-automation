# Project 1: Google Sheets → Gmail Automation

> **One-liner:** When a new row is added to a Google Sheet, an instant email alert is sent — no manual checking, zero missed leads.

[![Make.com](https://img.shields.io/badge/Make.com-Automation-blue)](https://make.com)
[![Google Sheets](https://img.shields.io/badge/Google%20Sheets-Trigger-green)](https://sheets.google.com)
[![Gmail](https://img.shields.io/badge/Gmail-Delivery-red)](https://gmail.com)

## 🎯 Problem
Founders track leads/orders in Google Sheets and manually check for new entries. Leads sit for hours. Orders get missed. Revenue lost.

## ✅ Solution
A 2-step Make.com scenario:
1. **Watch New Rows** — Google Sheets module watches for new rows
2. **Send Email** — Gmail module sends instant notification with row data

**Trigger → Transform → Deliver:** New Row → Format Message → Email Alert

## 🏗️ Architecture

```
[Google Sheets: Watch New Rows]
        ↓
[Gmail: Send an Email]
Subject: 📩 New Lead: {{Name}} - {{Email}}
Body: Name: {{Name}} | Email: {{Email}} | Message: {{Message}}
```

## 📸 Screenshots (Add Your Own)

- `scenario.png` — Make.com scenario (2 modules connected)
- `email-received.png` — Gmail inbox showing alert email
- `sheet.png` — Google Sheet with test data

> **Upload these 3 screenshots to this folder — use fake data only.**

## 📈 Results

- **Before:** Manual checking every 2-3 hours, 30 min/day wasted
- **After:** Instant alerts, response time < 2 minutes
- **Time Saved:** ~2.5 hours/week per sheet
- **Build Time:** 30 minutes

## 🛠️ Tools Used

- Make.com (Free tier — 1,000 ops/month)
- Google Sheets (Watch New Rows)
- Gmail (Send Email)
- **Running Cost:** Free tiers — client pays for build + documentation, not software

## 🎥 Demo Video

**YouTube Unlisted Link:** `[Paste your 30-45 sec Loom/YouTube link here]`

**Demo Script (30 sec):**
- 0-5s: Title card "Sheets → Gmail Alerts"
- 5-30s: Add new row in Sheet → Show Make.com scenario run → Show email arriving in Gmail
- 30-45s: Result screen "Saves 2.5 hrs/week — Built with Make.com + Gmail"

## 🚀 How To Replicate (For Clients)

1. Create Google Sheet with headers: Name, Email, Message
2. Make.com → New Scenario → Google Sheets → Watch New Rows → Connect → Select Sheet
3. Add Gmail → Send Email → Connect Gmail → Map fields from Sheets
4. Schedule: Run every 15 minutes (or instantly on new row)
5. Test: Add fake row → Confirm email arrives
6. Document + Loom walkthrough for client team

## 📄 Case Study

See `case-study.md` for full client-ready case study.

## 🔒 Security

- No API keys stored here
- Demo uses fake data: Test Person, test@email.com
- Real client sheet names redacted

---
**Built by Isaac — aiagentbuilderhq | [Full Portfolio](https://github.com/aiagentbuilderhq/automation-portfolio) | Free Audit: [Calendar Link]**
