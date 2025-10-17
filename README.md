<h1 align="center"><b>Chrono Compiler</b></h1>

<p align="center">
  <a href="https://github.com/saptarshiroy39/Chrono-Compiler"><b>Chrono Compiler</b></a> is an intelligent email digest system built with <a href="https://n8n.io"><b>n8n</b></a> that automatically compiles and delivers personalized hourly updates straight to your inbox. Stay informed with real-time weather, entertainment, and AI-curated news—all in one beautifully formatted email.
</p>

---

## ✨ Features

* 🌦️ **Real-time Weather Updates** - Current conditions, temperature, humidity, and more (***OpenWeatherMap API***)
* 😂 **Hourly Humor** - A fresh random joke to brighten your hour (***icanhazdadjoke API***)
* 📰 **AI-Summarized Tech News** - Top 10 technology headlines intelligently summarized (***Google News RSS*** & ***Google Gemini Chat Model***)
* 📧 **Automated Email Delivery** - Sends a beautifully formatted HTML email every hour (***Gmail SMTP***)
* 📗 **Activity Logging** - Tracks all digest activities with timestamps in ***Google Sheets*** for monitoring and analytics

---

## 🤖 Workflow Overview

Here is a visual overview of the n8n workflow:

![Chrono Compiler Workflow](workflow-overview.png)

---

## ⚙️ Workflow Components

1. **Schedule Trigger** - Runs every hour automatically
2. **OpenWeatherMap** - Fetches current weather data for your location
3. **Get Joke** - Retrieves a random dad joke via HTTP request
4. **Get Google News** - Pulls latest tech news from Google News RSS feed
5. **Limit News Items** - Filters top 10 news articles
6. **Summarize News** - Uses Google Gemini to create an AI-powered summary
7. **Compose Email** - Formats all data into a clean HTML email
8. **Send Email** - Delivers the digest via Gmail SMTP
9. **Prepare Log Data** - Prepares activity log entry
10. **Add Data** - Logs the activity to Google Sheets

---

<p align="center">
  Made with <a href="https://n8n.io">n8n</a> by Saptarshi Roy
</p>