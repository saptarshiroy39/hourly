<h1 align="center"><b>Chrono Compiler</b></h1>

<p align="center">
  <a href="https://github.com/saptarshiroy39/Chrono-Compiler"><b>Chrono Compiler</b></a> is an intelligent email digest system built with <a href="https://n8n.io"><b>n8n</b></a> that automatically compiles and delivers personalized hourly updates straight to your inbox. Stay informed with real-time weather, entertainment, and AI-curated news—all in one beautifully formatted email.
</p>

---

## ✨ Features

| FEATUREs                          | DESCRIPTION                                          | TECHNOLOGY                                    |
|-----------------------------------|------------------------------------------------------|-----------------------------------------------|
| 🌦️ **Real-time Weather Updates** | Current conditions, temperature, humidity, and more  | ***OpenWeatherMap API***                      |
| 😂 **Hourly Humor**              | A fresh random joke to brighten your hour            | ***icanhazdadjoke API***                      |
| 📰 **AI-Summarized Tech News**   | Top 10 technology headlines intelligently summarized | ***Google News RSS***, ***Gemini 2.5 Flash*** |
| 📧 **Automated Email Delivery**  | Sends a beautifully formatted HTML email every hour  | ***Gmail SMTP***                              |
| 📗 **Activity Logging**          | Tracks all digest activities with timestamps         | ***Google Sheets***                           |

---

## 🤖 Workflow Overview

Here is a visual overview of the n8n workflow:

![Chrono Compiler Workflow](Chrono-Compiler.png)

---

## ⚙️ Workflow Components

| #   | COMPONENTs           | DESCRIPTION                                        | NODEs                      |
|-----|----------------------|----------------------------------------------------|----------------------------|
| 1️⃣ | **Schedule Trigger** | Runs every hour automatically                      | ***n8n Schedule Trigger*** |
| 2️⃣ | **OpenWeatherMap**   | Fetches current weather data for your location     | ***OpenWeatherMap API***   |
| 3️⃣ | **Get Joke**         | Retrieves a random dad joke via HTTP request       | ***icanhazdadjoke API***   |
| 4️⃣ | **Get Google News**  | Pulls latest tech news from Google News feed       | ***Google News RSS***      |
| 5️⃣ | **Limit News Items** | Filters top 10 news articles                       | ***JavaScript Code***      |
| 6️⃣ | **Summarize News**   | Uses Google Gemini to create an AI-powered summary | ***Google Gemini***        |
| 7️⃣ | **Compose Email**    | Formats all data into a clean HTML email           | ***n8n Set Node***         |
| 8️⃣ | **Send Email**       | Delivers the digest via Gmail SMTP                 | ***Gmail SMTP***           |
| 9️⃣ | **Prepare Log Data** | Prepares activity log entry                        | ***n8n Set Node***         |
| 🔟 | **Add Data**         | Logs the activity to Google Sheets                 | ***Google Sheets API***    |

---

<p align="center">
  Made with <a href="https://n8n.io">n8n</a> by Saptarshi Roy
</p>