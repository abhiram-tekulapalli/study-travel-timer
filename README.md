# StudyTravel Simulator

<p align="center">
  <img src="https://raw.githubusercontent.com/abhiram-tekulapalli/project_readme_assets/main/header.svg" alt="StudyTravel Simulator" width="100%" />
</p>

<p align="center">
  <a href="https://nodejs.org/"><img src="https://img.shields.io/badge/Node.js-18+-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js"></a>
  <a href="https://vitejs.dev/"><img src="https://img.shields.io/badge/Vite-5.4+-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite"></a>
  <a href="https://firebase.google.com/"><img src="https://img.shields.io/badge/Firebase-Backend-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" alt="Firebase"></a>
  <a href="https://ai.google.dev/"><img src="https://img.shields.io/badge/Gemini%20API-AI-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Gemini API"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge" alt="License"></a>
</p>

---

## 🎯 Overview

A **gamified flight-simulator focus timer** that transforms study sessions into immersive journeys. Track progress, visualize your "flight path," and stay motivated with interactive sky visualizations and session analytics.

**Created by:** Tekulapalli Abhiram (@pokephantom98765)

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| ✈️ **Flight Simulator Theme** | Study sessions become journeys — take off, cruise, land |
| 📊 **Journey Tracking** | Persistent analytics: duration, distance, sessions, streaks |
| 🌌 **Interactive Sky Visualization** | Dynamic sky with clouds, stars, weather based on session state |
| 💬 **Session Feedback** | Post-flight debrief with insights and motivation |
| 🔥 **Firebase Backend** | Real-time sync, auth, security rules, offline support |
| 🤖 **AI-Powered Insights** | Gemini API for personalized session summaries |

---

## 🚀 Quick Start

### Prerequisites

- **Node.js** 18+
- **npm** / **bun** / **pnpm**
- **Firebase Project** (for backend)
- **Gemini API Key** (for AI features)

### Installation

```bash
# Clone repository
git clone https://github.com/abhiram-tekulapalli/study-travel-timer.git
cd study-travel-timer

# Install dependencies
npm install

# Configure environment
cp .env.example .env.local
```

Edit `.env.local`:
```env
# Firebase Configuration
VITE_FIREBASE_API_KEY=your_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
VITE_FIREBASE_PROJECT_ID=your_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
VITE_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
VITE_FIREBASE_APP_ID=your_app_id

# Gemini API (for AI features)
GEMINI_API_KEY=your_gemini_api_key
```

### Development

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173)

### Production Preview

```bash
npm run build
npm run preview
```

---

## 🏗️ Project Structure

```
study travel timer/
├── public/                 # Static assets
├── src/
│   ├── components/         # React components (Timer, Sky, Journey, Feedback)
│   ├── hooks/              # Custom hooks (useTimer, useJourney, useAuth)
│   ├── services/           # Firebase, Gemini API clients
│   ├── contexts/           # React context providers
│   ├── utils/              # Helpers, formatters, constants
│   ├── styles/             # CSS/Tailwind styles
│   ├── App.jsx             # Main app component
│   └── main.jsx            # Entry point
├── .env.example            # Environment template
├── firebase.json           # Firebase hosting config
├── firestore.rules         # Security rules
├── firestore.indexes.json  # Firestore indexes
├── vite.config.js          # Vite configuration
├── package.json
└── README.md
```

---

## 🔥 Firebase Setup

1. Create a Firebase project at [console.firebase.google.com](https://console.firebase.google.com)
2. Enable **Authentication** (Email/Password or Google)
3. Enable **Firestore Database** (Native mode)
4. Enable **Hosting** (for production deploy)
5. Copy config to `.env.local` (see above)
6. Deploy rules & indexes:
   ```bash
   firebase deploy --only firestore:rules,firestore:indexes
   ```

### Security Rules

- Users can only read/write their own journeys
- Journeys validated server-side (duration, distance limits)
- Admin access via custom claims

---

## 🎮 How It Works

| Phase | Action | Visual |
|-------|--------|--------|
| **Pre-Flight** | Set goal, choose duration, select route | Airport terminal UI |
| **Takeoff** | Timer starts, plane ascends | Animated ascent |
| **Cruise** | Focus mode, sky visualization | Interactive sky, clouds, progress ring |
| **Descent** | Final minutes, wrap-up prompt | Gradual descent |
| **Landing** | Session complete, feedback form | Touchdown animation |
| **Debrief** | AI summary, stats, streak update | Journey log entry |

---

## 🛠️ Tech Stack

<div align="center">

| Category | Tools |
|----------|-------|
| **Frontend** | React 18, Vite, Tailwind CSS |
| **Backend** | Firebase Auth, Firestore, Functions |
| **AI** | Google Gemini API |
| **Charts** | Recharts / Chart.js |
| **Animations** | Framer Motion |
| **Deployment** | Firebase Hosting |

</div>

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

## 👨‍💻 Author

**Tekulapalli Abhiram**  
[@abhiram-tekulapalli](https://github.com/abhiram-tekulapalli) · [@pokephantom98765](https://github.com/pokephantom98765)

---

<p align="center">
  <img src="https://raw.githubusercontent.com/abhiram-tekulapalli/project_readme_assets/main/footer.svg" alt="Footer" width="100%" />
</p>