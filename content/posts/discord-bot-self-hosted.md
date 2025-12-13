---
title: "Building a CI/CD-Enabled Discord Bot on Raspberry Pi 5"
date: 2025-06-08
draft: false
author: "Jeyaprakash S"
tags:
  - Raspberry Pi
  - Discord Bot
  - CI/CD
  - DevOps
  - Self-Hosted
categories:
  - Projects
  - Tech
summary: "How I built and deployed a fully automated Discord bot on Raspberry Pi 5 with a CI/CD-driven deployment pipeline — always up-to-date with zero manual intervention."
---

Over the past few weeks, I built and deployed a **fully automated Discord bot** — running 24/7 on a **Raspberry Pi 5** — to manage my server and stream music using YouTube links. [oai_citation:1‡LinkedIn](https://www.linkedin.com/pulse/building-cicd-enabled-discord-bot-raspberry-pi-5-senguttuvan-cowoc/?trackingId=ywlgFEyjpoWOVPOpOg6oKQ%3D%3D)

### 🚀 What It Does

This project includes:

- 🎵 **Music playback** using YouTube links (via `yt-dlp`)  
- 🛠️ **Server moderation** features (kick, ban, purge, etc.)  
- 🔁 **CI/CD-driven deployment** with:
  - ✅ Auto-redeploy on every push  
  - Zero downtime  
  - No manual intervention  [oai_citation:2‡LinkedIn](https://www.linkedin.com/pulse/building-cicd-enabled-discord-bot-raspberry-pi-5-senguttuvan-cowoc/?trackingId=ywlgFEyjpoWOVPOpOg6oKQ%3D%3D)

### 🧰 Tech Stack

- **Python** with `discord.py`  
- **yt-dlp** for YouTube audio extraction  
- **Raspberry Pi 5 (8GB + SSD)** as host  
- **GitHub Actions** with a **self-hosted runner**  
- Environment variables via `.env`  [oai_citation:3‡LinkedIn](https://www.linkedin.com/pulse/building-cicd-enabled-discord-bot-raspberry-pi-5-senguttuvan-cowoc/?trackingId=ywlgFEyjpoWOVPOpOg6oKQ%3D%3D)

### 💡 Why This Project Is Cool

- ⚡ **No cloud server cost** — your Pi hosts everything  
- 🤖 Full DevOps lifecycle on a small SBC  
- 🧩 Modular bot design for easy extension  
- 🔄 Seamless updates via CI/CD pipeline  [oai_citation:4‡LinkedIn](https://www.linkedin.com/pulse/building-cicd-enabled-discord-bot-raspberry-pi-5-senguttuvan-cowoc/?trackingId=ywlgFEyjpoWOVPOpOg6oKQ%3D%3D)

### 📈 CI/CD Highlights

Using GitHub Actions with a self-hosted runner on the Pi means:

- Push your code → bot automatically updates  
- Test and hotfix workflows with **main** and **dev** branches  
- Persistent bot sessions with graceful recovery  [oai_citation:5‡LinkedIn](https://www.linkedin.com/pulse/building-cicd-enabled-discord-bot-raspberry-pi-5-senguttuvan-cowoc/?trackingId=ywlgFEyjpoWOVPOpOg6oKQ%3D%3D)

---

### 🔭 What’s Next?

Future enhancements I’m exploring:

- 🤖 Voice activity detection for smarter interactions  
- 🤖 LLM integration for contextual replies  
- 📊 Companion dashboard UI (Streamlit/Next.js) for bot control  [oai_citation:6‡LinkedIn](https://www.linkedin.com/pulse/building-cicd-enabled-discord-bot-raspberry-pi-5-senguttuvan-cowoc/?trackingId=ywlgFEyjpoWOVPOpOg6oKQ%3D%3D)

---

If you’re into **self-hosted bots**, **Raspberry Pi automation**, or **DevOps workflows**, I’d love to connect and chat more! 🚀 #DiscordBot #SelfHosted #RaspberryPi5 #CICD #DevOps #GitHubActions #PythonDev  [oai_citation:7‡LinkedIn](https://www.linkedin.com/pulse/building-cicd-enabled-discord-bot-raspberry-pi-5-senguttuvan-cowoc/?trackingId=ywlgFEyjpoWOVPOpOg6oKQ%3D%3D)