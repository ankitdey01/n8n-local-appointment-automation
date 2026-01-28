# 🤖 n8n Local Appointment Automation

An automated appointment booking system built with **n8n** that works through **WhatsApp or Telegram**.  
Users can request appointments via chat, and the system instantly checks availability from **Google Sheets**, confirms bookings, or notifies when a slot is unavailable — all automatically.

---

## 📸 Workflow Overview

![n8n Appointment Automation Workflow](working-proto/workflow.png) 

> This image shows the complete n8n automation flow used for message parsing, availability checking, conflict detection, and confirmation replies.

---

## 🚀 What This Project Does

This automation eliminates manual appointment scheduling by handling everything through chat messages.

When someone sends a message requesting an appointment:
- The system extracts date, time, phone number, and purpose
- Checks existing appointments stored in Google Sheets
- Confirms the booking **or** informs the user that the slot is unavailable
- Records confirmed appointments instantly

---

## 🔄 How It Works

1. 📩 Receives appointment requests via **WhatsApp or Telegram**
2. 🧠 Extracts date, time, phone number, and optional purpose from natural language messages
3. 📊 Checks availability against existing records in **Google Sheets**
4. ⚡ Responds instantly with confirmation or unavailability
5. 📝 Saves confirmed appointments directly into Google Sheets

---

## ✨ Key Features

- 🧠 **Smart conflict detection**  
  Stops checking as soon as the first scheduling conflict is found

- 🤖 **Automatic data extraction**  
  Parses natural language messages into structured data

- 🔄 **Real-time updates**  
  Appointments are added immediately after confirmation

- 💬 **Two-way communication**  
  Sends confirmation or rejection messages back to the user

- 🛑 **No double booking**  
  Ensures only one booking per slot

---

## 💡 Why This Is Important

- ⏱️ **Saves time**  
  No manual back-and-forth for scheduling

- 🔒 **Prevents double booking**  
  Automatically validates availability

- 🌐 **24/7 availability**  
  Users can book anytime, even outside business hours

- ❌ **Reduces errors**  
  Automated data entry minimizes human mistakes

- ⭐ **Professional experience**  
  Instant replies improve customer trust and satisfaction

---

## 🏥 Use Cases

Perfect for:

- Medical clinics and dental offices  
- Salons and spas  
- Consulting services  
- Tutoring and coaching  
- Any service-based business with time-slot scheduling

---

## 📋 Google Sheets Structure

Your Google Sheet should follow this structure:

```markdown
| Phone Number | Date       | Time     | Purpose                     |
|--------------|------------|----------|-----------------------------|
| 123456789    | 2026-02-25 | 14:00:00 | dd party                    |
| 6969696969   | 2026-02-08 | 18:00:00 | some dd party discussions   |
