# 🌱 AGRIYA — AI-Powered Agricultural Advisory Platform

> **Empowering farmers with verified agricultural intelligence, multilingual advisory, and community collaboration in their native language.**

AGRIYA is a next-generation agricultural decision-support and farmer assistance platform built for rural communities. It unites verified conversational RAG AI, instant visual crop disease diagnostics, hyperlocal agro-meteorology, seamless government subsidy discovery, and a peer knowledge exchange to eliminate information barriers in farming.

---

## 📖 About the Project

### 🎯 Problem Statement
Smallholder and rural farmers face significant challenges in accessing timely, localized, and actionable agricultural advice. Fragmented extension services, language barriers, unpredictable microclimates, delayed crop disease identification, and complex bureaucratic procedures for government subsidies often lead to preventable crop losses and diminished livelihoods.

### 💡 The Solution
AGRIYA bridges this gap with an intuitive, mobile-first advisory platform designed for accessibility and trust. Farmers can converse naturally in their regional languages via voice or text with an AI grounded in verified agronomic research, capture leaf photos for instant diagnostic treatment plans, track weather conditions translated directly into field-level recommendations, and discover government welfare schemes without intermediaries.

### 🌟 Core Value Proposition
- **Democratized Agronomic Knowledge**: Instant, round-the-clock guidance powered by advanced LLM and RAG architecture grounded in certified agricultural sources.
- **Vernacular Accessibility**: Multilingual voice and text conversational interface supporting 12 Indian regional languages.
- **Actionable Hyperlocal Insights**: Weather forecasts converted into concrete farming advisories (irrigation timing, pesticide spraying windows, harvesting alerts).
- **Community-to-Officer Escalation**: Unresolved peer forum questions are automatically routed to verified Agriculture Extension Officers.

---

## ✨ Features

- 🤖 **Multilingual AI Chat Advisor** — Conversational AI powered by Groq (Llama 3.3 70B) with RAG over verified agricultural knowledge bases; supports regional voice input.
- 🔬 **Crop Disease Scanner** — Real-time leaf diagnostic scanner providing disease identification, confidence scores, and organic/chemical remedy recommendations.
- 👥 **Farmer Community Forum** — Peer-to-peer Q&A forum with community upvoting; unresolved questions automatically escalate to Agriculture Officers within 48 hours.
- 🌦️ **Hyperlocal Weather Advisories** — Live location-based weather tracking translated into actionable farming actions (spray, irrigate, sow, or harvest).
- 🏛️ **Government Scheme Discovery** — Filterable catalog of central and state agricultural subsidies, insurance schemes, and financial benefits.
- 🏆 **Farmer Rewards Program** — Gamified points engine rewarding helpful forum contributors and daily active farmers with redeemable input discounts.
- 🗺️ **Nearby Agriculture Center Locator** — Interactive Leaflet map locating local Krishi Vigyan Kendras (KVK), mandis, and agricultural offices.
- 🔒 **Role-Based Authentication** — Secure multi-role access control (Farmer, Agriculture Extension Officer, Admin) powered by Firebase Auth.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Frontend Framework** | React 19 + TypeScript + Vite |
| **Styling & UI** | Tailwind CSS v4, Framer Motion, Lucide React |
| **Routing & State** | React Router DOM v7, TanStack React Query v5 |
| **Backend & Database** | Firebase (Firestore, Authentication, Cloud Storage, Cloud Functions) |
| **AI / LLM Engine** | Groq API (Llama 3.3 70B Versatile) + RAG Knowledge Retriever |
| **Mapping & GIS** | Leaflet + React Leaflet |
| **Weather Telemetry** | Open-Meteo API |

---

## 📁 Folder Structure

```
Agriya/
├── functions/                  # Firebase Cloud Functions (backend AI proxy)
│   ├── src/
│   │   └── askAi.ts            # Secure server-side Groq LLM integration
│   └── package.json
├── public/                     # Static assets, web app manifest, icons
├── src/
│   ├── components/             # Reusable UI widgets, layout, chat bubbles
│   ├── context/                # AuthContext and ThemeContext providers
│   ├── data/                   # Schemes database and agricultural facilities
│   ├── hooks/                  # Speech recognition and custom React hooks
│   ├── pages/                  # Views (Landing, Dashboard, Chat, Forum, Weather, Schemes)
│   ├── services/               # Firebase collections, RAG retriever, Groq client
│   ├── types/                  # TypeScript domain models and interfaces
│   ├── App.tsx                 # Root application component & routes
│   └── main.tsx                # Application bootstrap
├── firebase.json               # Firebase deployment configuration
├── firestore.rules             # Cloud Firestore security rules
├── package.json                # Project dependencies and npm scripts
└── vite.config.ts              # Vite bundler configuration
```

---

## 🚀 How to Install and Run

### Prerequisites
- [Node.js](https://nodejs.org/) (v18+) & `npm`
- A Firebase project with Firestore and Authentication enabled

### 1. Clone the Repository
```bash
git clone https://github.com/karthiban3333-maker/Agriya.git
cd Agriya
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Configure Environment Variables
Copy `.env.example` to `.env`:
```bash
cp .env.example .env
```
Provide your Firebase and Groq API credentials.

### 4. Start Development Server
```bash
npm run dev
```
Open `http://localhost:5173` in your browser.

### 5. Build for Production
```bash
npm run build
npm run preview
```

---

## 📸 Screenshots

> _Add screenshots here._

---

## 📄 License

This project is private and proprietary. All rights reserved.

---

## 👨‍💻 Author

**Karthiban A** — [Kode Prime](https://github.com/karthiban3333-maker)
