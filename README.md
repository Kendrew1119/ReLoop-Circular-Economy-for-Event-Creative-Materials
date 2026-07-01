# 🌿 ReLoop — Circular Economy & Sustainable Consumption Mobile App

> **Course Project:** UCCD3223 Mobile Applications Development (June 2026 Trimester)  
> **University:** Universiti Tunku Abdul Rahman (UTAR)  
> **Theme:** Circular Economy & Sustainable Consumption (UN SDG 12)  
> **Group Size:** 4 Members  

ReLoop is an innovative, modern mobile application designed to drive sustainable consumer behavior and close the loop on waste generation. Leveraging **Gemini AI**, **Google Maps**, and **Open Food Facts API**, ReLoop features an AI-driven smart scanner, a localized recycling marketplace, and a P2P resource sharing platform, all wrapped in a sleek, glassmorphic iOS-style interface.

---

## ✨ Core Features (The 3 Pillars)

### 1. 🔍 AI Smart Scanner
*   **AI Image Recognition:** Capture or upload images to identify items using the Google Gemini 2.5 Flash API.
*   **Recycling & Reuse Assistance:** Automatically receive item categories, specific recycling instructions, creative upcycling/reuse ideas, and estimated decomposition time.
*   **Barcode Scanner:** Scans product barcodes, pulls packing material details from the Open Food Facts API, and runs them through Gemini AI to get specialized disposal instructions.
*   **Text Search:** Search for items via text query if camera/barcode scan is not preferred.
*   **Offline Cache:** SQLite caching layer saves local API calls and keeps history accessible offline.

### 2. ♻️ Localized Recycling Marketplace
*   **Waste-to-Value Marketplace:** Post recyclable waste or items to sell, donate (free), or request pickup.
*   **Real-time Communication:** Chat directly in-app with interested recyclers or neighbours using Firebase Realtime Database.
*   **Map Integration:** Pins list location or drop-off centers onto an interactive map using the Google Maps API.

### 3. 🤝 P2P Sharing & Lending
*   **Collaborative Consumption:** Rent, lend, or borrow household tools (e.g., drills, ladders), electronics, or textbooks to reduce overconsumption.
*   **Availability Calendar:** Track active bookings and return dates.
*   **Trust Ratings:** Review-based rating system to maintain reliability and community trust.

---

## 🛠 Tech Stack

| Component | Technology |
|---|---|
| **Frontend Framework** | React Native + Expo (SDK 53) |
| **Language** | TypeScript |
| **Routing** | Expo Router (File-based navigation) |
| **State Management** | Zustand |
| **Local Database** | expo-sqlite (SQLite) |
| **Cloud Database / BaaS** | Firebase (Firestore, Auth, Storage, Realtime Database) |
| **AI Integration** | Google Gemini 2.5 Flash API |
| **External API** | Open Food Facts API, Google Maps Platform |
| **Styling** | Expo Blur (for glassmorphism) + Expo Linear Gradient |
| **Icons** | Expo Vector Icons (Ionicons) |

---

## 🚀 Setup & Installation

### Prerequisites
Before running this application, make sure you have the following installed:
*   [Node.js](https://nodejs.org/) (v20 LTS recommended)
*   [Git](https://git-scm.com/)
*   Expo Go app on your physical mobile device (Android/iOS) OR an Emulator set up in Android Studio/Xcode.

### Step 1: Clone the Repository
```bash
git clone <your-github-repo-url>
cd mobileapp
```

### Step 2: Install Dependencies
```bash
npm install
```

### Step 3: Configure Environment Variables
Create a `.env` file in the root directory and configure the following:
```env
# Gemini API Key (from Google AI Studio)
EXPO_PUBLIC_GEMINI_API_KEY=your_gemini_api_key

# Firebase Credentials
EXPO_PUBLIC_FIREBASE_API_KEY=your_firebase_api_key
EXPO_PUBLIC_FIREBASE_AUTH_DOMAIN=your_firebase_auth_domain
EXPO_PUBLIC_FIREBASE_PROJECT_ID=your_firebase_project_id
EXPO_PUBLIC_FIREBASE_STORAGE_BUCKET=your_firebase_storage_bucket
EXPO_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_firebase_messaging_sender_id
EXPO_PUBLIC_FIREBASE_APP_ID=your_firebase_app_id

# Google Maps API Key
EXPO_PUBLIC_GOOGLE_MAPS_API_KEY=your_google_maps_api_key
```

### Step 4: Start the Expo Development Server
```bash
npm run start
```
*   Scan the QR code displayed in the terminal with your **Expo Go** app to run on a physical device.
*   Press `a` to run on Android Emulator.
*   Press `i` to run on iOS Simulator (macOS only).

---

## 📂 Project Structure

```
├── assets/                  # Launcher icon, splash screens, and images
├── app/                     # Expo Router pages (File-based navigation)
│   ├── _layout.tsx          # Root layout with providers (Zustand, Theme)
│   ├── (tabs)/              # Main App Shell
│   │   ├── index.tsx        # Home screen (Dashboard / Eco Score)
│   │   ├── scan.tsx         # AI Scanner screen
│   │   ├── market.tsx       # Recycling Marketplace screen
│   │   ├── share.tsx        # P2P Lending screen
│   │   └── profile.tsx      # User profile, history, achievements
│   ├── auth/                # Authentication screens (Login/Register)
│   └── scan-result.tsx      # AI Scan detailed result popup screen
├── components/              # Shared reusable UI elements
│   ├── ui/                  # Custom Glassmorphic styled components
│   │   ├── GlassCard.tsx
│   │   ├── GlassButton.tsx
│   │   └── GlassInput.tsx
│   └── CameraView.tsx       # Camera scanner component
├── db/                      # SQLite configuration and schema queries
├── hooks/                   # Custom React hooks (e.g., useSQLite, useLocation)
├── services/                # API service wrappers (Gemini, Open Food Facts, Firebase)
├── store/                   # State management logic (Zustand)
└── types/                   # TypeScript definitions
```

---

## 👥 Team & Responsibilities

Refer to [plan.md](file:///c:/Users/B2B/Desktop/mobileapp/plan.md) for the detailed 14-week schedule and documentation division. Below is a quick overview of development roles:

*   **Member A (Team Lead / Full-Stack):** Tab Routing, App Shell, Firebase Auth, Google Maps, Location Services.
*   **Member B (Frontend / UI Developer):** Custom UI Glassmorphism components, Dashboard, Screen Styling, App Icon & branding.
*   **Member C (AI / Core Logic Developer):** Google Gemini integration, Barcode lookup, Open Food Facts setup, Local SQLite caching.
*   **Member D (Backend / Marketplace Developer):** Firestore listings, Real-time Chat, Booking System database logic, AppGallery deployment.

---

## ⚖️ License
This project is developed for academic evaluation under UTAR Course **UCCD3223 Mobile Applications Development**. All rights reserved by the project group members.
