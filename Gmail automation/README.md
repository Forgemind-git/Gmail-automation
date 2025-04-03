# 📧 Gmail Automation with n8n

This n8n workflow automates sending personalized reminder emails via Gmail, based on data updates in a connected Google Sheet.

---

## 🔧 Features

- 🔘 Manually trigger emails or auto-send on new Google Sheets rows.
- 📊 Fetch recipient details and personalize messages using Google Sheets.
- ✉️ Send customized Gmail messages encouraging digital decluttering.

---

## 🛠 Workflow Overview

### 1. Manual Trigger
- **Node**: `When clicking 'Test workflow'`
- Manually initiates the workflow for testing.

### 2. Google Sheets
- **Node**: `Google Sheets`
- Fetches data from the following sheet:
  - Automation Mail Details
  - Sheet name: `Sheet1`
- Retrieves values like `Name` and `Mail IDs`.

### 3. Gmail
- **Node**: `Gmail`
- Sends a personalized text email to each recipient.
- Message content promotes digital organization and productivity.

### 4. Google Sheets Trigger *(Optional)*
- **Node**: `Google Sheets Trigger`
- Listens for new row additions every minute.
- Automatically triggers the email workflow.

---

## 📩 Email Template

Subject: Quick Reminder: Take a Moment for Digital Declutter

Hi {{ Name }},

Just a friendly reminder to take a few minutes today to do a quick digital declutter!
Clearing out old emails, organizing files, and updating passwords can make a big difference in productivity and peace of mind.

Here are a few simple steps to consider:
Archive or delete emails you no longer need
Unsubscribe from newsletters you don’t read
Organize files into folders for quick access
Clear out your downloads folder
Update passwords if it’s been a while

It doesn’t have to be perfect—just a small effort today can make tomorrow smoother.

Feel free to forward this reminder to your team, friends, or anyone who might find it helpful!

Stay organized,
Forgemind Automation


---

## 🔐 Required Credentials

Make sure to configure the following credentials in your n8n instance:
- `Google Sheets OAuth2`
- `Gmail OAuth2`

---

## 📎 Notes

- This automation is ideal for productivity tips, newsletters, or gentle nudges to your audience or team.
- You can extend it with filters, logging, or email tracking features as needed.

