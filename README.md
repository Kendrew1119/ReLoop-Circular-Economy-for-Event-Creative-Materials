# 🌿 EventLoop — Circular Economy for Event & Creative Materials

> **Course Project:** UCCD3223 Mobile Applications Development (June 2026 Trimester)  
> **University:** Universiti Tunku Abdul Rahman (UTAR)  
> **Theme:** Circular Economy & Sustainable Consumption (UN SDG 12)  
> **Niche:** Event Materials & Creative Project Supplies  
> **Group Size:** 4 Members  

EventLoop is a mobile application that closes the loop on **event and creative project waste**. Targeting campus event organizers, exhibition planners, cosplayers, and DIY makers, EventLoop uses **Gemini AI** to scan and identify materials, connects users through a **material marketplace** to sell or donate leftovers, and enables **peer-to-peer equipment lending** to reduce overconsumption — all wrapped in a sleek, glassmorphic iOS-style interface.

---

## ✨ Core Features (The 3 Pillars)

### 1. 🔍 AI Smart Scanner
*   **AI Image Recognition:** Capture or upload photos of event materials (banners, props, foam boards) for instant AI identification using Google Gemini 2.5 Flash.
*   **Material Intelligence:** Receive material type, recycling instructions, creative upcycling ideas for events/crafts, and environmental impact data.
*   **Auto-Fill Posting:** AI scan results automatically pre-fill marketplace or lending post forms — scan → post in seconds.
*   **Offline Cache:** SQLite caching layer saves scan results locally for offline access and reduces API calls.

### 2. ♻️ Material Marketplace
*   **Post Leftover Materials:** Sell, donate, or request pickup for unused event materials (PVC banners, decorations, fabric scraps, lanyards).
*   **Category Filtering:** Browse by material type — Banners, Decorations, Fabric, Stationery, Craft Supplies, Wood, Electronics, Packaging.
*   **Real-time Chat:** Message buyers/sellers directly in-app using Firebase Realtime Database.
*   **Map Integration:** View listings on a map and find nearby materials using Google Maps.

### 3. 🤝 Equipment Lending
*   **Share Expensive Tools:** Lend or borrow event and craft equipment — PA systems, projectors, sewing machines, heat guns, stage lights.
*   **Borrow Request System:** Request to borrow with specific dates; owners approve or decline.
*   **Trust Ratings:** Review-based rating system to maintain community trust.
*   **Map Discovery:** Find lendable equipment near you on an interactive map.

---

## 🛠 Tech Stack

| Component | Technology |
|---|---|
| **Frontend Framework** | React Native + Expo (SDK 53) |
| **Language** | TypeScript |
| **Routing** | Expo Router (File-based navigation) |
| **State Management** | Zustand |
| **Local Database** | expo-sqlite (SQLite) |
| **Cloud Backend** | Firebase (Firestore, Auth, Storage, Realtime Database) |
| **AI Integration** | Google Gemini 2.5 Flash API |
| **Maps** | Google Maps Platform (react-native-maps) |
| **Camera** | expo-camera + expo-image-picker |
| **Styling** | expo-blur + expo-linear-gradient (Glassmorphism) |
| **Icons** | @expo/vector-icons (Ionicons) |

---

## 🚀 Setup & Installation

### Prerequisites
*   [Node.js](https://nodejs.org/) (v20 LTS)
*   [Git](https://git-scm.com/)
*   Expo Go app on your phone OR Android Studio emulator

### Step 1: Clone the Repository
```bash
git clone https://github.com/Kendrew1119/EventLoop-Circular-Economy-Sustainable-Consumption-Mobile-App.git
cd mobileapp
```

### Step 2: Install Dependencies
```bash
npm install
```

### Step 3: Configure Environment Variables
Create a `.env` file in the root directory:
```env
EXPO_PUBLIC_GEMINI_API_KEY=your_gemini_api_key
EXPO_PUBLIC_FIREBASE_API_KEY=your_firebase_api_key
EXPO_PUBLIC_FIREBASE_AUTH_DOMAIN=your_firebase_auth_domain
EXPO_PUBLIC_FIREBASE_PROJECT_ID=your_firebase_project_id
EXPO_PUBLIC_FIREBASE_STORAGE_BUCKET=your_firebase_storage_bucket
EXPO_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_firebase_messaging_sender_id
EXPO_PUBLIC_FIREBASE_APP_ID=your_firebase_app_id
EXPO_PUBLIC_GOOGLE_MAPS_API_KEY=your_google_maps_api_key
```

### Step 4: Start the Development Server
```bash
npm run start
```

---

## 📂 Project Structure

```
├── app/                              # Expo Router pages
│   ├── _layout.tsx                   # Root layout (providers)
│   ├── index.tsx                     # Entry redirect
│   ├── auth/                         # Login & Register
│   ├── (tabs)/                       # Main tab navigator
│   │   ├── index.tsx                 # 🏠 Home Dashboard
│   │   ├── market.tsx                # ♻️ Material Marketplace
│   │   ├── scan.tsx                  # 📷 AI Scanner
│   │   ├── share.tsx                 # 🤝 Equipment Lending
│   │   └── profile.tsx              # 👤 Profile & Settings
│   ├── scan-result.tsx              # AI scan result detail
│   ├── market/                       # Marketplace sub-routes
│   ├── share/                        # Lending sub-routes
│   ├── chat/                         # Chat screens
│   └── dropoff.tsx                  # Drop-off points map
├── components/                       # Shared UI components
│   ├── ui/                           # Glassmorphism design system
│   ├── ScanResultCard.tsx
│   ├── ListingCard.tsx
│   ├── LendingCard.tsx
│   └── CategoryChips.tsx
├── services/                         # API wrappers
│   ├── firebase.ts
│   ├── gemini.ts
│   └── maps.ts
├── db/                               # SQLite schema
├── hooks/                            # Custom hooks
├── store/                            # Zustand state
└── types/                            # TypeScript definitions
```

---

## 👥 Team Roles

*   **Member A (Team Lead / Full-Stack):** Navigation, Auth, Maps integration, Profile.
*   **Member B (Frontend / UI Dev):** Glassmorphism components, Dashboard, all screen styling, App Icon.
*   **Member C (AI / Core Logic Dev):** Gemini API integration, Camera, Scan result flow, SQLite.
*   **Member D (Backend / Marketplace Dev):** Firestore CRUD, Chat, Marketplace & Lending backend, AppGallery deployment.

---

## ⚖️ License
This project is developed for academic evaluation under UTAR Course **UCCD3223 Mobile Applications Development**. All rights reserved by the project group members.
