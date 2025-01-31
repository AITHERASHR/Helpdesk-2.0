📌 Project Overview: HR Helpdesk - Ticket Management System
This HR Helpdesk Web App is designed to help HR teams manage employee support tickets efficiently. It provides a simple, web-based interface to view, respond to, and track helpdesk tickets submitted by employees. The system integrates Google Apps Script, Google Sheets, and Gmail to automate communication and ticket management.

🎯 Core Functionality & Features
1️⃣ Web App Interface (index.html)
Displays a list of open tickets fetched from Google Sheets.
Tickets include:
Employee name, contact details, and issue description.
A color-coded priority indicator (🔴 High, 🟡 Medium, 🟢 Low).
Messaging Box: Each ticket has a text box where HR can type a response and send it via email.
2️⃣ Backend - Google Apps Script (Webapp.gs & Messaging.gs)
Fetches ticket data from Google Sheets (getOpenTickets()).
Handles sending messages using Gmail (sendTicketMessage()).
Stores email conversation threads (thread ID is saved in Google Sheets to track replies).
Ensures secure & structured API calls for ticket retrieval and messaging.
3️⃣ Ticket Management in Google Sheets
Stores all tickets in a Google Sheet ("Open Tickets").
Includes columns for tracking messages, priority, and resolution status.
Updates thread IDs when a message is sent to maintain conversation history.
4️⃣ Email Integration via Gmail
HR responses are sent via Gmail directly from the web app.
If a previous email thread exists, it replies to the same thread for continuity.
Otherwise, a new email thread is created, and its ID is stored in Sheets.
5️⃣ Secure Deployment & Access
Hosted as a Google Apps Script Web App.
Can be restricted to internal company use or shared publicly for broader access.
Uses google.script.run to avoid CORS issues and enhance security.
🌟 Why This is Useful
✅ Centralized HR Support – All employee concerns are logged in one place.
✅ Faster Response Times – HR can quickly respond to tickets via the web app.
✅ Automated Email Tracking – No need to manually track conversations.
✅ Seamless Google Workspace Integration – Uses Google Sheets & Gmail natively.

🚀 How It Works (Step-by-Step)
HR opens the web app → The system loads open tickets from Google Sheets.
HR selects a ticket & types a response in the message box.
Clicks "Send" → The system automatically:
Sends an email via Gmail.
Saves the email thread ID (if new).
Logs the message in Google Sheets.
The employee receives an email and can reply back (tracked in Gmail).
