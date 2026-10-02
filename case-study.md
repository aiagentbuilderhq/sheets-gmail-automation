# Case Study: Google Sheets → Gmail Automation

**Client Type:** Small business tracking leads in Google Sheets
**Timeline:** 30 minutes
**Tools:** Make.com, Google Sheets, Gmail
**Cost to Run:** $0/month (free tiers)

### Problem
A founder used a Google Sheet to track incoming leads from a landing page. The team checked the sheet manually 3-4 times per day. Hot leads waited hours. One lead per week was missed entirely because no one refreshed the sheet.

**Time wasted:** ~30 min/day checking + 1 lost lead/week.

### Solution
Built a 2-module automation:
1. **Trigger:** Google Sheets "Watch New Rows" — fires instantly when new row appears
2. **Delivery:** Gmail "Send an Email" — formatted alert with lead details sent to founder + sales Slack (optional)

**Workflow:**
New Row Added → Make.com Detects → Email: "📩 New Lead: John Doe (john@company.com) - Needs automation help"

**Key Design Choices:**
- No coding, visual builder — client team can understand it in 60 seconds
- Email includes all row fields, so no need to open Sheet for triage
- Runs every 15 min on free tier (upgrade to instant on paid, but free is enough to start)

### Results
- **Response Time:** Hours → Under 2 minutes
- **Missed Leads:** 1/week → 0
- **Time Saved:** 2.5 hrs/week
- **Client Feedback:** "I didn't know this could be done in 30 minutes. This alone is worth it."

### Tools & Setup
- Make.com Free Tier
- Google Sheets API (via Make.com connection)
- Gmail API (via Make.com connection)
- No extra software to learn — uses tools client already has

### What Client Gets
- Working Make.com scenario (shared via blueprint)
- 15-min Loom walkthrough video
- 1-page documentation (how to edit, how to add more recipients)
- 7 days support — if it breaks, fixed free within 24h

### Why This Matters (Retainer Angle)
"The tools are free, yes — the upkeep isn't. Connections expire, sheets change, new team members need adding. Monthly plan means I'm watching it, updating it as your business changes, and fixing it within 24 hours when something breaks."

---
*Demo Video: [Add Unlisted YouTube Link] | Portfolio: github.com/aiagentbuilderhq/automation-portfolio*
