# Project 1: Google Sheets → Gmail Automation (Make.com + n8n + APIs)

> **One-liner:** When a new row is added to a Google Sheet, an instant email alert is sent — no manual checking, zero missed leads. Built for both Make.com and n8n.

[![Make.com](https://img.shields.io/badge/Make.com-Automation-blue)](https://make.com)
[![n8n](https://img.shields.io/badge/n8n-Workflow-red)](https://n8n.io)
[![Google Sheets API](https://img.shields.io/badge/Google%20Sheets%20API-Trigger-green)](https://developers.google.com/sheets/api)
[![Gmail API](https://img.shields.io/badge/Gmail%20API-Delivery-red)](https://developers.google.com/gmail/api)
[![Webhooks](https://img.shields.io/badge/Webhooks-Enabled-orange)](https://en.wikipedia.org/wiki/Webhook)

**Live Hub:** [automation-portfolio](https://github.com/aiagentbuilderhq/automation-portfolio) | **Other Projects:** [Weather Bot](https://github.com/aiagentbuilderhq/weather-telegram-bot) · [Form → Slack](https://github.com/aiagentbuilderhq/form-slack-leads) · [AI Inbox Assistant](https://github.com/aiagentbuilderhq/ai-inbox-assistant) · [Lead Scoring](https://github.com/aiagentbuilderhq/ai-lead-scoring)

## 🎯 Problem
Founders track leads/orders in Google Sheets and manually check for new entries. Leads sit for hours. Orders get missed. Revenue lost.

## ✅ Solution — Works on Make.com AND n8n (Client Chooses Stack)

**Make.com Version (2 steps):**
1. **Google Sheets → Watch New Rows** — API trigger
2. **Gmail → Send Email** — Instant notification with row data

**n8n Version (2 nodes):**
1. **Google Sheets Trigger** — Watches new rows via Sheets API + Webhook
2. **Gmail Node** — Sends formatted alert via Gmail API

**Trigger → Transform → Deliver:** New Row (Sheets API/Webhook) → Format Message → Email Alert (Gmail API)

## 🏗️ Architecture

```
[Google Sheets: Watch New Rows — Sheets API / Webhook]
        ↓
[Router / Filter — Optional: Only if Score > X]
        ↓
[Gmail: Send an Email — Gmail API]
Subject: 📩 New Lead: {{Name}} - {{Email}}
Body: Name: {{Name}} | Email: {{Email}} | Message: {{Message}}
```

**n8n Alternative:**
```
[Sheets Trigger] → [Set Node: Format Message] → [Gmail Node: Send Email] → [Slack Node: Optional Alert]
```

## 📸 Screenshots (Add Your Own)

- `scenario-make.png` — Make.com scenario (2 modules)
- `scenario-n8n.png` — n8n workflow (2 nodes)
- `email-received.png` — Gmail inbox showing alert
- `sheet.png` — Google Sheet with test data

## 📈 Results

- **Before:** Manual checking every 2-3 hours, 30 min/day wasted
- **After:** Instant alerts, response time < 2 minutes
- **Time Saved:** ~2.5 hours/week per sheet
- **Build Time:** 30 minutes (both Make.com and n8n versions)

## 🛠️ Tools Used — Founder-Searched Skills

- **Automation:** Make.com (Free tier) · n8n (self-host free / cloud) · Webhooks · Scheduling
- **APIs:** Google Sheets API · Gmail API · HTTP / JSON
- **Patterns:** Error Handling, Router, Filters, Data Mapping
- **Running Cost:** Free tiers — client pays for build + documentation, not software
- **Why Both Make.com + n8n?** If client already uses n8n, I build in n8n. If Make.com, I build there. No new tool to learn.

## 🎥 Demo Video

**YouTube Unlisted Link:** `[Paste your 30-45 sec Loom/YouTube link here]`

**Demo Script (30 sec):**
- 0-5s: Title card "Sheets → Gmail Alerts — Make.com + n8n"
- 5-30s: Add new row in Sheet → Show Make.com scenario run → Show email arriving in Gmail → Show n8n version too
- 30-45s: Result screen "Saves 2.5 hrs/week — Built with Make.com + n8n + Gmail/Sheets APIs"

## 🚀 How To Replicate (For Clients — Works on Both Platforms)

**Make.com:**
1. Create Google Sheet with headers: Name, Email, Message
2. Make.com → New Scenario → Google Sheets → Watch New Rows → Connect → Select Sheet (Sheets API)
3. Add Gmail → Send Email → Connect Gmail (Gmail API) → Map fields
4. Schedule: Every 15 min (free) or instant via webhook
5. Test: Add fake row → Confirm email arrives

**n8n:**
1. n8n → New Workflow → Google Sheets Trigger → Select Sheet
2. Add Gmail node → Send Email → Connect → Map fields
3. Add Webhook for instant trigger (optional)
4. Activate workflow → Test

## 💼 Client Use Cases

- E-commerce: New order row → Slack #orders + Gmail confirmation
- Coaching: Discovery form → Sheets → Gmail alert + Calendar invite
- Agency: Lead Sheet → Gmail + Slack + HubSpot via API
- Any API: Same pattern works for Shopify API → Gmail, Stripe API → Sheets, etc.

## 🔒 Security

- No API keys stored here
- Demo uses fake data: Test Person, test@email.com
- Real client sheet names redacted

## 📄 Case Study

See `case-study.md` for full client-ready case study.

---
**Built by Isaac — aiagentbuilderhq | [Full Portfolio Hub](https://github.com/aiagentbuilderhq/automation-portfolio) | Tech: Make.com + n8n + Gmail/Sheets APIs + Webhooks | Free Audit: [Calendar Link]**
