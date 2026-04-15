# Lead Conversion Engine (n8n)

A rule-based lead qualification and conversion system built with n8n, JavaScript logic, and automation.

## 🚀 What It Does

This workflow automates the entire lead handling process:

- Captures leads via webhook
- Normalizes incoming data
- Scores leads using rule-based logic
- Creates contacts and deals in HubSpot
- Sends automated email follow-ups
- Logs high-quality and low-quality leads separately
- Tracks errors and failures automatically

---

## 🧠 Core Logic

Leads are scored based on:

- Budget level
- Message intent (keywords like automation, CRM, urgent)
- Company presence
- Data completeness

Score range: 1–10

- High-quality leads (≥7) → Follow-up email + success log
- Low-quality leads (<7) → Logged separately

---

## 🛠 Tech Stack

- n8n (workflow automation)
- JavaScript (custom scoring logic)
- HubSpot API (CRM)
- Gmail API (follow-up automation)
- Google Sheets (logging system)

---

## 📊 Workflow Features

- Real-time lead scoring
- Automated CRM entry (contact + deal)
- Conditional follow-up emails
- Structured logging system
- Error tracking + alerting

---

## 📂 Files

- `AI Lead Conversion Engine.json` → n8n workflow export

---

## ⚙️ Setup

1. Import JSON into n8n
2. Add credentials:
   - HubSpot
   - Gmail
   - Google Sheets
3. Update spreadsheet IDs
4. Activate workflow
5. Send POST request to webhook

---

## 🧪 Example Input

```json
{
  "name": "Mike Brown",
  "email": "mike.brown@gmail.com",
  "company": "Acme",
  "budget": 300,
  "message": "Need help with CRM automation",
  "status": "new_lead"
}
