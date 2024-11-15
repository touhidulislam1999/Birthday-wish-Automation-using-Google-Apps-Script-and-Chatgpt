# 🎉 Birthday Wish Automation using Google Apps Script and ChatGPT 🎂

![Birthday Automation](https://github.com/touhidulislam1999/Birthday-wish-Automation-using-Google-Apps-Script-and-Chatgpt/assets/97190512/480b13cb-6a9d-4c31-9fd9-91553be8fa1c)

## 📜 **Description**
This project automates birthday wishes by integrating **Google Apps Script**, **Google Sheets**, and **ChatGPT API**. It fetches contact details from the user's Google Contacts and sends personalized birthday greetings via email. 🎁 The wishes are randomized using ChatGPT, ensuring every wish feels unique and heartfelt.

---

## 📂 **Key Files and Features**

### 📜 **`Fetcher.gs`**  
![Fetcher](https://github.com/touhidulislam1999/Birthday-wish-Automation-using-Google-Apps-Script-and-Chatgpt/assets/97190512/eef9cdb9-9127-4b41-9262-2310b3eb8e0c)

**Purpose:** Automatically imports and updates the contact details into Google Sheets.

**Features:**
1. Fetches data (name, email, birthdate) from the user's Google Contacts.
2. Ensures only contacts with both email and birthdate are included.
3. Sets missing birth years to `1900` (if not provided) to focus on day and month.
4. Automates sheet updates daily between **11:00 PM and 12:00 AM** using a time-driven trigger.

---

### 📜 **`Sender.gs`**  
![Sender](https://github.com/touhidulislam1999/Birthday-wish-Automation-using-Google-Apps-Script-and-Chatgpt/assets/97190512/a14014a4-4265-4faf-a683-60e9ba1dda64)

**Purpose:** Sends personalized birthday greetings via email on the recipient's special day. 🎈

**Features:**
1. Automatically matches the current date with the contact's birthday.
2. Uses the **OpenAI GPT-3.5-turbo API** to generate unique and personalized birthday messages.
3. Sends emails with styled HTML content for a professional look.
4. Operates seamlessly through a time-driven trigger daily between **12:00 AM and 1:00 AM**.
5. Option for static birthday wishes (commented-out code for fallback).

---

## 💡 **How It Works**
1. The script fetches contacts from Google Contacts and stores them in Google Sheets.
2. Contacts with missing data are skipped to maintain accuracy.
3. At midnight, the script checks for birthdays matching the current date.
4. If a match is found:
   - An API-generated or static birthday wish is prepared.
   - The email is sent with a personalized message.
5. Everything runs automatically, making it hassle-free for users!

---

## ✨ **Key Highlights**
- **Google Sheets Integration**: Acts as a backend to store and manage contact data.
- **OpenAI API**: Ensures creative and unique birthday messages.
- **Fully Automated Workflow**: From fetching contacts to sending greetings.
- **Time-Driven Triggers**: Keeps the script running without manual intervention.

---

## 🎯 **How to Use**
1. Clone the repository:
   ```bash
   git clone https://github.com/touhidulislam1999/Birthday-wish-Automation-using-Google-Apps-Script-and-Chatgpt.git
