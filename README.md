# 🌱 AGRIYA

> **Answers a farmer can trust, in the language they speak.**

AGRIYA is an AI-powered agricultural assistant platform built for Bharat's farmers. It combines a multilingual AI chatbot grounded in verified agricultural knowledge, a peer community forum, hyperlocal weather forecasts, government scheme discovery, and a rewards engine — so no farming question ever goes unanswered.

Built for **Smart India Hackathon 2025 · SIH25076** by Team Regal Hackers.

---

## ✨ Features

- 🤖 **AI Chat Advisor** — WhatsApp-style conversational AI powered by Groq (Llama 3.3 70B) with RAG over verified agricultural sources; supports voice input and answers in 12 regional languages
- 🌾 **Crop Disease Scanner** — Identify pests and diseases from a leaf photo with confidence scores and treatment recommendations
- 👥 **Community Forum** — Farmer-powered Q&A with upvoting; unresolved questions are automatically escalated to Agriculture Officers within 48 hours
- 🌦️ **Hyperlocal Weather Forecasts** — Live, location-based forecasts (Open-Meteo) translated into actionable farming advice (spray, irrigate, sow, or wait)
- 🏛️ **Government Scheme Browser** — Search and filter subsidies by state, crop, and eligibility; apply without paperwork runarounds
- 🏆 **Rewards System** — Earn points for helpful answers and daily check-ins; redeem for seeds, fertilizer, and equipment discounts
- 🗺️ **Nearby Agriculture Offices** — Map view of the nearest official offices (Leaflet + React Leaflet)
- 🔐 **Firebase Auth** — Secure sign-up / login with Firestore user profiles and role-based access (farmer / agriculture officer / admin)
- 🌙 **Dark / Light Mode** — Full theme support across all pages
- ⚡ **Admin Dashboard** — Moderate posts, manage users, and monitor platform activity

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Framework** | React 19 + TypeScript 6 |
| **Build Tool** | Vite 8 |
| **Styling** | Tailwind CSS v4 |
| **Routing** | React Router DOM v7 |
| **State / Async** | TanStack Query v5 |
| **Animations** | Framer Motion |
| **Backend / DB** | Firebase (Auth, Firestore, Storage, Cloud Functions) |
| **AI / LLM** | Groq API — Llama 3.3 70B Versatile |
| **RAG** | Custom retriever in `src/services/rag/` |
| **Weather** | Open-Meteo (key-free) |
| **Maps** | Leaflet + React Leaflet |
| **Charts** | Recharts |
| **Forms** | React Hook Form |
| **Icons** | Lucide React |
| **Linting** | Oxlint |

---

## 📁 Folder Structure

```
Agriya/
├── functions/               # Firebase Cloud Functions (AI proxy)
│   └── src/
│       └── askAi.ts         # Groq API server-side proxy
├── public/                  # Static assets (icons, manifest)
├── src/
│   ├── components/
│   │   ├── chat/            # MessageBubble, Markdown renderer
│   │   ├── layout/          # AppLayout, ProtectedRoute
│   │   └── ui/              # Button, Card, Badge
│   ├── context/             # AuthContext, ThemeContext
│   ├── data/                # Static datasets (schemes, nearby offices)
│   ├── hooks/               # useSpeech (voice input)
│   ├── lib/                 # Utility helpers
│   ├── pages/               # Route-level page components
│   │   ├── admin/           # AdminDashboard
│   │   ├── Chat.tsx
│   │   ├── Dashboard.tsx
│   │   ├── Forum.tsx
│   │   ├── Schemes.tsx
│   │   ├── Weather.tsx
│   │   └── Rewards.tsx
│   ├── services/
│   │   ├── ai/              # Groq client, chat service
│   │   ├── firebase/        # Auth, Firestore collections, config
│   │   └── rag/             # Knowledge base & retriever
│   ├── types/               # Shared TypeScript types
│   ├── App.tsx              # Root router
│   └── main.tsx             # Entry point
├── .env.example             # Environment variable template
├── firebase.json            # Firebase project config
├── firestore.rules          # Firestore security rules
├── storage.rules            # Storage security rules
├── index.html
├── vite.config.ts
└── package.json
```

---

## 🚀 Installation & Running

### Prerequisites

- **Node.js** ≥ 18 and **npm** ≥ 9
- A **Firebase** project (Firestore, Auth, Storage enabled)
- A **Groq API key** from [console.groq.com](https://console.groq.com/keys)

### 1. Clone the repository

```bash
git clone https://github.com/karthiban3333-maker/Agriya.git
cd Agriya
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

```bash
cp .env.example .env
```

Open `.env` and fill in your credentials:

```env
VITE_FIREBASE_API_KEY=your_firebase_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
VITE_FIREBASE_PROJECT_ID=your_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
VITE_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
VITE_FIREBASE_APP_ID=your_app_id

VITE_GROQ_API_KEY=your_groq_api_key
VITE_GROQ_MODEL=llama-3.3-70b-versatile
```

> **⚠️ Security:** Never commit your `.env` file. For production, proxy Groq calls through the Firebase Cloud Function in `functions/src/askAi.ts` so the API key never reaches the client.

### 4. Start the development server

```bash
npm run dev
```

The app will be available at `http://localhost:5173`.

### 5. Build for production

```bash
npm run build
npm run preview
```

### 6. Deploy to Firebase Hosting (optional)

```bash
npm install -g firebase-tools
firebase login
firebase deploy
```

---

## 📸 Screenshots

> _Add screenshots here._

---

## 📄 License

This project is private and built for academic/hackathon purposes.

---

## 👨‍💻 Author

**Karthiban A** — [Kode Prime](https://github.com/karthiban3333-maker)
