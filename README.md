# 🚰 Switchee — Energy-on-Tap for the Informal City

[![Hackathon Ready](https://img.shields.io/badge/hackathon-ready-ff6f61)]() 
[![Status](https://img.shields.io/badge/status-live-brightgreen)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.10-blue)]()
[![React](https://img.shields.io/badge/react-18-blueviolet)]()

---

> Switchee is Energy-on-Tap — a solar + DC microgrid platform that delivers safe, prepaid, IoT-controlled electricity to informal urban communities.  
> **Pay for power, not the panel.**

---

## 🔗 Live App & Demo

🚀 **Live App:** https://switchee-energy-flow.lovable.app/  
🎥 **Demo Video:** https://youtu.be/0N7e8OpcKZ0  

---

## 🔦 Highlights
- ⚡ **Switchee Hub** — Containerized solar + battery, rapid deployment  
- 🔌 **IoT Smart Plug** — Enforced power limits + real-time usage  
- 🔐 **Energy Tokens** — Blockchain-backed, prepaid, secure  
- 📱 **USSD + Lightweight App** — Works for low-connectivity communities  
- 🔄 **Scalable Hubs** — Microservices for DISCOM & VPP integration

---

## 📌 Table of Contents
- [Problem](#problem)  
- [Solution](#solution)  
- [Architecture](#architecture)  
- [Live Demo & Screenshots](#live-demo--screenshots)  
- [Quick Start (Docker)](#quick-start-docker)  
- [Local Setup](#local-setup)  
- [API Examples](#api-examples)  
- [Roadmap](#roadmap)  
- [Contributing](#contributing)  
- [Team](#team)  
- [License](#license)

---

## ❗ Problem
Millions living in informal settlements face:
- Frequent power outages  
- Hazardous wiring  
- High costs for unreliable alternatives  

This hinders education, home businesses, safety, and economic mobility.

---

## ✅ Solution
Switchee brings **safe, reliable, prepaid clean energy** using:
- Solar Hubs with battery storage  
- DC microgrids for low-power, safe distribution  
- Smart metering via IoT  
- Tokenized prepaid billing  
- Simple user access via USSD & web app  

---

## 🏗 Architecture (High-Level)

[Switchee Hub (Solar + Battery)]
|
+--> DC Microgrid --> [Smart Plug @ Homes]
|
+--> IoT Gateway --> Edge Services --> Cloud API
|
Blockchain (Energy Tokens)
|
Mobile App • USSD • Admin Dashboard

yaml
Copy code

---

## 🎬 Live Demo & Screenshots

- 🌐 **Live App (Frontend):** https://switchee-energy-flow.lovable.app/  
- 🎥 **Full Demo Video:** https://youtu.be/0N7e8OpcKZ0  
- 📁 Screenshots available in `/assets/screenshots/`

---

## ⚡ Quick Start (Docker)

```bash
git clone https://github.com/<your-org>/switchee.git
cd switchee

cp .env.example .env

docker compose up --build
Services
Frontend → http://localhost:3000

API docs (Swagger) → http://localhost:8000/docs

Admin dashboard → http://localhost:3001


🛠 Local Setup
Backend (FastAPI)
bash
Copy code
cd api
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env 
alembic upgrade head
uvicorn app.main:app --reload --port 8000
Frontend (React)
bash
Copy code
cd web
npm install
npm start
IoT Device Simulator
bash
Copy code
cd sim/iot
python simulate_devices.py --count 10 --hub http://localhost:8000
🧭 API Examples
Get Hub Status
bash
Copy code
curl http://localhost:8000/hubs/1/status
Mint Energy Tokens
bash
Copy code
curl -X POST http://localhost:8000/tokens/mint \
  -H "Content-Type: application/json" \
  -d '{"user_id": "user_01", "amount_kwh": 2.5}'
Check Balance (Simulated USSD)
bash
Copy code
curl -X POST http://localhost:8000/ussd \
  -H "Content-Type: application/json" \
  -d '{"phone":"+91XXXXXXXXXX", "text":"*123#"}'

🚀 Roadmap
Hackathon MVP
Smart Plug simulator
Prepaid tokenization
Simple USSD menu
Microgrid model
Near Term
Real IoT integration
Offline-first mobile app


Maintenance analytics

Future
Virtual Power Plant (VPP)
DISCOM integration
Community energy marketplaces


🤝 Contributing
Fork the repo


Create a feature branch:
bash
Copy code
git checkout -b feat/your-feature
Make changes + add tests


Submit a Pull Request 🎉
See CONTRIBUTING.md for more.


👥 Team
Sudarshanam Yessasvini — Founder & Product Lead
📧 yessasvini.s@gmail.com


🧾 License
This project is licensed under the MIT License.


If you enjoy the project, please ⭐ the repo and share feedback!
Let’s bring Energy-on-Tap to communities that need it most. ⚡🌍

yaml
Copy code
