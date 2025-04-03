# 🤖 Gmail AI Automation with n8n & Google Gemini

This n8n workflow automates the generation and sending of personalized email reminders using **AI-powered language models**. It fetches user data from Google Sheets, generates email content based on personality traits, and sends it through Gmail — all without manual writing.

---

## 🚀 Features

- 🔁 Automatically triggered on new rows added to a Google Sheet.
- ✍️ Email content is dynamically generated based on the recipient's name and personality type.
- 🤖 Uses Google Gemini (via LangChain) for language generation.
- 📧 Sends the final email using Gmail.
- 🧠 Fully integrated AI agent experience — from prompt to inbox.

---

## 🧩 Workflow Components

### 1. **Google Sheets Trigger**
- Watches for new rows in:
  - AI Agent Mail Details Sheet
  - Sheet: `Sheet1`
- Trigger: `rowAdded` (every minute)

### 2. **Google Sheets**
- Pulls in user data:
  - `Name`
  - `Mail IDs`
  - `Personality`

### 3. **LangChain LLM Chain**
- Node: `Basic LLM Chain`
- Prompt instructs the LLM to generate a short, personality-based email with 90–100 words, without a subject line.
- Mail topic: **"Take a Moment for Digital Declutter"**

### 4. **Google Gemini Chat Model**
- Model: `gemini-2.0-flash`
- Integrated with LangChain to process the email generation task.

### 5. **Gmail**
- Sends the AI-generated message to the email address fetched from the sheet.

### 6. **Manual Trigger**
- For testing the flow manually without waiting for new sheet rows.

---

## 📩 Sample Prompt Structure

To name: John  
Personality: Friendly

Generate a professional yet friendly email body without subject. The tone and style of the email should reflect the personality type. The content should be on "Take a Moment for Digital Declutter". Create a short mail content with 90-100 words.

The mail is addressed to "To name".

Sign the mail as Forgemind AI

---

## 🧠 Tech Stack

- **n8n** (Workflow Automation)
- **Google Sheets** (Input source)
- **LangChain** (LLM prompt engine)
- **Google Gemini (via PaLM)** (AI model for generation)
- **Gmail API** (Email delivery)

---

## 🔐 Credentials Needed

- `Google Sheets OAuth2`
- `Gmail OAuth2`
- `Google Gemini (PaLM) API Key`

---

## 📎 Notes

- You can customize the prompt, model, and email subject easily.
- Make sure the Google Sheet includes `Name`, `Personality`, and `Mail IDs` columns.
- Gemini model can be swapped for other providers supported by LangChain.

---

## 🎥 Created for [ForgeMindAI](https://youtube.com/@ForgeMindAI)

Feel free to remix this for custom AI agent workflows!

