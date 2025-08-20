# 🚀 Telegram Daily Poster Bot

An **automated LinkedIn posting bot** built using **n8n**, **Google Sheets**, **Google Gemini AI**, and **Telegram** for seamless daily content distribution.

This workflow helps you:

* Pull topics from **Google Sheets**
* Auto-generate **engaging LinkedIn posts** using **Google Gemini AI**
* Attach images to posts
* Post directly to **LinkedIn**
* Update Google Sheets with status (**Completed/Failed**)
* Send real-time success/failure notifications via **Telegram**

## 📌 Features

* ⏰ **Scheduled Posting** – Runs automatically every day at 10 AM
* 📝 **Content Generation** – Uses Google Gemini AI to create short, human-like LinkedIn posts with emojis & hashtags
* 📷 **Image Support** – Fetches images from external URLs and attaches them to posts
* 📊 **Google Sheets Integration** – Manages topics and tracks posting status
* 🔗 **LinkedIn Integration** – Publishes posts directly to your account/page
* 📱 **Telegram Notifications** – Alerts you whether posting was successful or failed

## 🛠️ Tech Stack

* [n8n](https://n8n.io/) – Automation workflow engine
* [Google Sheets](https://www.google.com/sheets/about/) – Topic & status database
* [Google Gemini AI](https://ai.google/) – Post content generator
* [LinkedIn API](https://learn.microsoft.com/en-us/linkedin/) – Automated posting
* [Telegram Bot API](https://core.telegram.org/bots/api) – Notifications

## ⚙️ Workflow Overview

1. **Schedule Trigger** → Starts the workflow every day at 10 AM
2. **Google Sheets Node** → Fetches the next pending topic
3. **Gemini AI Node** → Generates an engaging LinkedIn post
4. **HTTP Request Node** → Downloads any attached image
5. **LinkedIn Node** → Creates the LinkedIn post
6. **Google Sheets Update** → Marks status as "Completed" or "Failed"
7. **Telegram Notification** → Sends a message with the posting result

## 📂 Setup Instructions

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/telegram-daily-poster-bot.git
   ```
2. Import the workflow JSON into **n8n**
3. Configure the following credentials:

   * **Google Sheets API**
   * **Google Gemini API**
   * **LinkedIn OAuth2 API**
   * **Telegram Bot API**
4. Update your **Google Sheet** with the following columns:

   * `Topic` → The post topic
   * `Status` → Leave empty or set as "pending"
   * `ImageURL` → (Optional) image link for the post
5. Deploy the workflow and enjoy automated posting 🚀

## 📸 Example Workflow Preview

![Workflow Preview](https://n8n.io/workflows/n8n-workflow-preview.png)
*(Replace with your own screenshot)*

## ✅ Future Enhancements

* Add support for **multi-language posts**
* Schedule **different posting times**
* Advanced error logging & retry mechanism

## 👨‍💻 Author

Developed by **[Your Name](https://github.com/your-username)**

Would you like me to also create a **badges section** at the top (GitHub stars, n8n, LinkedIn, Telegram, Google Sheets) to make it look more professional?
