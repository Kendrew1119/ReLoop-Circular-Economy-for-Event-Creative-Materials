# 📋 UCCD3223 Mobile App Development — Master Project Plan

> **Course:** UCCD3223 Mobile Applications Development (June 2026 Trimester)  
> **University:** Universiti Tunku Abdul Rahman (UTAR)  
> **Theme:** Circular Economy & Sustainable Consumption (UN SDG 12)  
> **Group Size:** 4 Members  
> **Timeline:** 14 Weeks (June 2026 – September 2026)

---

## 📌 Key Deadlines

| Milestone | Due Date | Weight |
|-----------|----------|--------|
| Part 1 — Proposal | **Week 5 Wed (15 July 2026)** before 5:00 PM | 10% of final |
| Part 2 — Working App + Report | **Week 12 Sat (5 Sept 2026)** before 5:00 PM | 20% of final |
| Presentation & Q&A | **Week 13** (during Practical session) | Included in Part 2 |

---

## 🏆 Marking Scheme Breakdown

### Part 1 — Proposal (100 marks → 10% of final)

| Criteria | Weight | Multiplier | Strategy |
|----------|--------|------------|----------|
| Creativity / Novelty / Usefulness | 40% | ×4 | **Highest priority** — AI scanner + marketplace + P2P lending is a unique 3-in-1 concept |
| Completeness of Idea | 30% | ×3 | Cover all 3 pillars: Scan → Recycle → Share |
| Overall Design (UI) | 20% | ×2 | Glassmorphism wireframes, iOS-style mockups |
| Neat Documentation | 10% | ×1 | Clean formatting, good structure |

### Part 2 — Working App + Report (100 marks → 20% of final)

| Criteria | Weight | Multiplier | Notes |
|----------|--------|------------|-------|
| Program completeness & functionality | 30% | ×3 | All 3 core modules must work end-to-end |
| Actual design & creativity | 10% | ×1 | Match or exceed proposal design |
| Potential for civil/commercial use | 5% | ×0.5 | Real-world applicability — Malaysia-focused |
| Tidiness of source code | 5% | ×0.5 | Clean, commented, modular code |
| Documentation (individual) | 20% | ×2 | Clear role labels, GitHub contributions |
| Presentation (individual) | 15% | ×1.5 | 10-min demo |
| Q&A (individual) | 15% | ×1.5 | Understand your own code deeply |
| **Bonus**: Published on Play Store / AppGallery | Extra | — | Register Huawei dev account early |

---

## 💡 The App Concept

### App Name Options (Pick One)

| # | Name | Tagline | Vibe |
|---|------|---------|------|
| 1 | **ReLoop** | *Scan. Recycle. Share. Repeat.* | Circular, action-oriented |
| 2 | **EcoCircle** | *Close the Loop, Open the Future* | Community-focused, aspirational |
| 3 | **GreenSwap** | *Every Item Has a Next Life* | Fresh, marketplace-forward |
| 4 | **CircleWise** | *Smart Choices for a Circular World* | AI-forward, intelligent |
| 5 | **ReKind** | *Be Kind to the Planet, One Item at a Time* | Emotional, human-centered |

> **Recommendation:** **ReLoop** — short, memorable, perfectly describes the circular flow (scan → recycle → share → repeat). Works well as an app icon (a looping arrow with a leaf).

---

### Core Concept — 3 Pillars

```
┌─────────────────────────────────────────────────────────────────┐
│                        ReLoop App                                │
│                                                                  │
│   🔍 SCAN          ♻️ RECYCLE           🤝 SHARE                │
│   AI Scanner       Marketplace          P2P Lending              │
│                                                                  │
│   • Photo scan     • Post waste         • Lend items             │
│   • AI identify    • Request pickup     • Borrow items           │
│   • Category       • Chat with          • Neighbourhood          │
│   • Recycle tips     recyclers            circles                │
│   • Reuse ideas    • Donate option      • Trust rating           │
│   • Eco impact     • Map drop-off       • Availability           │
│   • Drop points    • Location-based       calendar               │
└─────────────────────────────────────────────────────────────────┘
```

---

### SDG 12 Alignment & Design Components

| Assignment Requirement | How ReLoop Addresses It |
|----------------------|------------------------|
| **P2P Resource Optimisation** | ✅ P2P lending module — share tools, electronics, books between neighbours |
| **Behavioural Transformation** | ✅ AI scanner educates users on recycling; gamified eco-score and streaks |
| **Closing the Loop** | ✅ Recycling marketplace connects waste producers with recyclers/upcyclers |
| **Originality** | ✅ 3-in-1 approach (scan + marketplace + lending) is unique — no single app does all three |
| **Technological Integration** | ✅ Gemini AI (vision + text), Google Maps API, Open Food Facts API |
| **Feasibility** | ✅ Well-scoped features; all APIs have free tiers; buildable in 7 weeks |

---

## 🧠 AI System Architecture & Flow

### Overview

```
┌──────────────────────────────────────────────────────────────────┐
│                    AI PROCESSING PIPELINE                         │
│                                                                   │
│  ┌──────────┐    ┌──────────────┐    ┌───────────────────────┐   │
│  │  INPUT    │───▶│  PROCESSING  │───▶│  OUTPUT               │   │
│  │          │    │              │    │                       │   │
│  │ 📷 Camera │    │ Gemini 2.5   │    │ • Item name           │   │
│  │ 🖼 Gallery│    │ Flash Vision │    │ • Category            │   │
│  │ 📝 Text  │    │ API          │    │ • Material type       │   │
│  │ 📊 Barcode│    │              │    │ • Recycle instruction  │   │
│  └──────────┘    └──────────────┘    │ • Reuse suggestion     │   │
│                                      │ • Eco impact score     │   │
│                                      │ • Nearby drop-off pts  │   │
│                                      └───────────────────────┘   │
└──────────────────────────────────────────────────────────────────┘
```

### Scan Mode 1: Image Scan (Primary)

```
User opens camera
       │
       ▼
  Capture photo / Select from gallery
       │
       ▼
  Image preprocessed (compress, resize to 1024px)
       │
       ▼
  Send to Gemini 2.5 Flash Vision API
  ┌─────────────────────────────────────────────┐
  │  Prompt:                                     │
  │  "Identify this item. Return JSON with:      │
  │   - item_name                                │
  │   - category (plastic/glass/metal/paper/     │
  │     electronic/textile/organic/other)         │
  │   - material_type                            │
  │   - recyclable (true/false)                  │
  │   - recycling_instructions (step by step)    │
  │   - reuse_suggestions (3 creative ideas)     │
  │   - environmental_impact                     │
  │   - estimated_decomposition_time             │
  │   - carbon_footprint_saved_if_recycled       │
  │   - confidence_score (0-100)"                │
  └─────────────────────────────────────────────┘
       │
       ▼
  Parse JSON response
       │
       ▼
  Display result card (glassmorphism UI)
       │
       ├──▶ [♻️ Recycle] → Show nearby drop-off (Google Maps API)
       ├──▶ [🛒 Sell/Donate] → Post to Recycling Marketplace
       ├──▶ [🤝 Lend] → Post to P2P Lending
       └──▶ [📋 Save] → Save to scan history (local storage)
```

### Scan Mode 2: Text/Keyword Search

```
User types item name (e.g., "plastic bottle")
       │
       ▼
  Send to Gemini 2.5 Flash Text API
  ┌─────────────────────────────────────────────┐
  │  Prompt:                                     │
  │  "Provide recycling information for:         │
  │   [user input]. Return JSON with same        │
  │   schema as image scan."                     │
  └─────────────────────────────────────────────┘
       │
       ▼
  Same result card UI as image scan
```

### Scan Mode 3: Barcode/Product Lookup

```
User scans barcode
       │
       ▼
  Extract barcode number
       │
       ▼
  Query Open Food Facts API (for food items)
  ┌─────────────────────────────────────────────┐
  │  GET https://world.openfoodfacts.org/api/    │
  │      v2/product/{barcode}                    │
  │                                              │
  │  Returns: product name, packaging material,  │
  │  ingredients, eco-score, nutriscore          │
  └─────────────────────────────────────────────┘
       │
       ├── If found → Enrich with Gemini API for recycling tips
       │                specific to the packaging material
       │
       └── If not found → Fall back to Gemini text scan
              with barcode number as context
       │
       ▼
  Display enriched result card
```

### AI Prompt Engineering Strategy

```
System Prompt (prepended to all AI calls):
┌─────────────────────────────────────────────────────────────────┐
│  "You are ReLoop AI, an expert in waste management, recycling,  │
│   and circular economy. You are specifically knowledgeable      │
│   about recycling practices in Malaysia. Always provide         │
│   practical, actionable advice. Format responses as valid JSON. │
│   Include Malaysia-specific drop-off categories when relevant   │
│   (e.g., e-waste collection by DOE, kitar semula centres)."     │
└─────────────────────────────────────────────────────────────────┘
```

### AI Response Caching Strategy

```
Scan result received from Gemini API
       │
       ▼
  Hash the item_name + category as cache key
       │
       ▼
  Store in local SQLite database
  ┌──────────────────────────────┐
  │  Table: scan_cache           │
  │  - id (PK)                   │
  │  - cache_key (hash)          │
  │  - response_json             │
  │  - created_at                │
  │  - expires_at (7 days)       │
  └──────────────────────────────┘
       │
       ▼
  Next time same/similar item scanned:
  → Check cache first → Skip API call if fresh
  → Saves API quota (free tier: 15 req/min)
```

---

## 📱 App Feature Breakdown

### Module 1: 🔍 AI Smart Scanner

| Feature | Description | API Used |
|---------|-------------|----------|
| **Camera Scan** | Real-time photo capture → AI identification | Gemini 2.5 Flash Vision |
| **Gallery Upload** | Pick existing photo for scanning | Gemini 2.5 Flash Vision |
| **Text Search** | Type item name for recycling info | Gemini 2.5 Flash Text |
| **Barcode Scan** | Scan product barcode for packaging info | Open Food Facts + Gemini |
| **Result Card** | Beautiful glassmorphism card showing all info | — |
| **Action Buttons** | Recycle / Sell / Donate / Lend / Save | — |
| **Scan History** | Past scans saved locally with timestamps | SQLite |
| **Nearby Drop-offs** | Map showing recycling centres near user | Google Maps API |

### Module 2: ♻️ Recycling Marketplace

| Feature | Description | Backend |
|---------|-------------|---------|
| **Post Listing** | Upload waste item with photo, description, condition | Firebase Firestore + Storage |
| **Listing Types** | Sell (set price) / Donate (free) / Request Pickup | Firestore document field |
| **Browse/Search** | Filter by category, location, type (sell/donate) | Firestore queries |
| **Location** | Show item location on map; distance from user | Google Maps API |
| **In-App Chat** | Real-time messaging between poster & interested party | Firebase Realtime DB |
| **Request Pickup** | Recycler/collector can request to pick up waste | Firestore + push notification |
| **Listing Status** | Available → Reserved → Collected/Sold | Firestore update |
| **User Ratings** | Rate buyers/sellers after transaction | Firestore sub-collection |

### Module 3: 🤝 P2P Sharing & Lending

| Feature | Description | Backend |
|---------|-------------|---------|
| **Post Item to Lend** | List reusable items (tools, electronics, books) | Firebase Firestore + Storage |
| **Browse Lendable Items** | Search/filter by category, distance, availability | Firestore queries |
| **Borrow Request** | Send request to item owner with dates needed | Firestore + notification |
| **Availability Calendar** | Show when item is free / borrowed | Date picker + Firestore |
| **In-App Chat** | Coordinate pickup/return between lender & borrower | Firebase Realtime DB |
| **Trust Score** | Build reputation through successful shares | Calculated from ratings |
| **Categories** | Tools 🔧, Electronics 📱, Books 📚, Kitchen 🍳, Sports ⚽, Garden 🌱 | Firestore enum |
| **Return Tracking** | Mark item as returned; rate the experience | Firestore update |

### Module 4: 🏠 Home Dashboard

| Feature | Description |
|---------|-------------|
| **Eco Score** | Personal sustainability score (gamified) |
| **Quick Scan Button** | One-tap to open scanner |
| **Recent Activity** | Latest scans, marketplace posts, lending activity |
| **Community Stats** | Total items recycled, items shared, CO₂ saved by community |
| **Sustainability Tips** | AI-generated daily tip (Gemini API) |

### Module 5: 👤 Profile & Settings

| Feature | Description |
|---------|-------------|
| **User Profile** | Name, photo, location, eco-score badge |
| **My Listings** | All marketplace posts + lending posts |
| **My Scan History** | All past AI scans |
| **Achievements** | Gamification badges (First Scan, 10 Items Shared, etc.) |
| **Settings** | Dark/light mode, notifications, location preferences |

### Module 6: 🗺 Map & Discovery

| Feature | Description | API |
|---------|-------------|-----|
| **Nearby Drop-offs** | Recycling centres, e-waste collection, kitar semula | Google Maps API |
| **Marketplace Map View** | See waste listings on map | Google Maps API |
| **Lending Map View** | See lendable items nearby | Google Maps API |
| **Directions** | Navigate to drop-off or item location | Google Maps Directions |

---

## 🛠 Tech Stack

| Layer | Technology | Reason |
|-------|-----------|--------|
| **Framework** | **React Native + Expo (SDK 53)** | Cross-platform, fast dev, Expo Go for instant preview |
| **Language** | **TypeScript** | Type safety, cleaner code, marks for tidiness |
| **Navigation** | **Expo Router (file-based)** | Modern routing, similar to Next.js |
| **State Management** | **Zustand** | Lightweight, simple, no boilerplate |
| **Local Storage** | **expo-sqlite** | Meets requirement: store/update/retrieve data locally |
| **Backend** | **Firebase** | Firestore (database), Auth (login), Storage (images), Realtime DB (chat) |
| **AI API** | **Google Gemini 2.5 Flash** | Free tier, vision + text, fast inference |
| **Maps** | **Google Maps API** (`react-native-maps`) | Drop-off locations, marketplace/lending map views |
| **Product Data** | **Open Food Facts API** | Free, open-source product database for barcode scanning |
| **Camera** | **expo-camera** + **expo-image-picker** | Photo capture + gallery selection |
| **Barcode** | **expo-barcode-scanner** | Scan product barcodes |
| **Blur/Glass** | **expo-blur** + **expo-linear-gradient** | Glassmorphism UI effects |
| **Charts** | **react-native-chart-kit** | Eco-score dashboard, impact stats |
| **Icons** | **@expo/vector-icons** (Ionicons) | iOS-like icon set |
| **Fonts** | **Inter** (Google Fonts) | Clean, modern, readable |
| **Version Control** | **GitHub** | Required for contribution tracking |
| **Publishing** | **Huawei AppGallery** (free) | Register ASAP — approval takes days |

### External APIs Summary

| API | Purpose | Free Tier | Endpoint Example |
|-----|---------|-----------|-----------------|
| **Gemini 2.5 Flash** | Image recognition, text generation, recycling info | 15 RPM free | `generativelanguage.googleapis.com` |
| **Google Maps Platform** | Map display, geocoding, directions, places | $200/month credit | `maps.googleapis.com` |
| **Open Food Facts** | Product info from barcode (food items) | Unlimited, open-source | `world.openfoodfacts.org/api/v2/product/{barcode}` |
| **Firebase** | Auth, Firestore, Storage, Realtime DB | Spark plan (free) | `firestore.googleapis.com` |

---

## 🎨 UI Design Direction

### Design Philosophy: Glassmorphism + iOS Aesthetic

| Principle | Implementation |
|-----------|---------------|
| **Glassmorphism** | Frosted glass cards with `blur(20px)`, semi-transparent backgrounds, subtle light borders |
| **iOS-like** | Large titles, bottom tab bar, rounded corners (16-20px), system-native feel |
| **Clean & Spacious** | Generous padding (24-32px), breathing room, max 2-3 elements per section |
| **Icons > Words** | Ionicons for navigation and actions; minimal text labels |
| **Themed Colors** | All colours derived from app theme; consistent throughout |
| **Micro-animations** | Smooth transitions (300ms), haptic feedback, parallax scroll |

### Color Palette Options (Based on App Name)

#### Option 1 — ReLoop (Nature Green) 🟢 *(Recommended)*
| Token | Color | Usage |
|-------|-------|-------|
| Primary | `#2D6A4F` (Forest Green) | Headers, CTAs, active tab |
| Secondary | `#95D5B2` (Mint) | Cards, highlights, success states |
| Accent | `#D4A373` (Warm Gold) | Badges, achievements, notifications |
| Danger | `#E63946` (Red) | Delete, warnings |
| Background Light | `#F8F9FA` (Snow) | Light mode background |
| Background Dark | `#0D1B14` (Deep Forest) | Dark mode background |
| Glass Fill | `rgba(45, 106, 79, 0.08)` | Glassmorphism card fill |
| Glass Border | `rgba(255, 255, 255, 0.18)` | Glassmorphism card border |
| Text Primary | `#1A1A2E` / `#F8F9FA` | Light / Dark mode text |
| Text Secondary | `#6B7280` / `#9CA3AF` | Subtitle, captions |

#### Option 2 — EcoCircle (Ocean Teal) 🔵
| Token | Color | Usage |
|-------|-------|-------|
| Primary | `#0D9488` (Teal) | Headers, CTAs |
| Secondary | `#5EEAD4` (Aqua) | Cards, highlights |
| Accent | `#F59E0B` (Amber) | Badges, streaks |
| Background Light | `#F0FDFA` (Mint Cream) | Light mode |
| Background Dark | `#0F1A1A` (Deep Teal) | Dark mode |

#### Option 3 — GreenSwap (Fresh Lime) 🍃
| Token | Color | Usage |
|-------|-------|-------|
| Primary | `#16A34A` (Vibrant Green) | Headers, CTAs |
| Secondary | `#86EFAC` (Light Green) | Cards, highlights |
| Accent | `#7C3AED` (Purple) | Special items, premium |
| Background Light | `#F7FEE7` (Lime Cream) | Light mode |
| Background Dark | `#0A1A0F` (Deep Green) | Dark mode |

### Screen Layout (Tab Structure)

```
┌────────────────────────────────────────┐
│  ╭─ Status Bar ──────────────────────╮ │
│  │         9:41           📶 🔋      │ │
│  ╰───────────────────────────────────╯ │
│                                        │
│  Large Title: Home                     │
│                                        │
│  ╭──── Eco Score Card (Glass) ───────╮ │
│  │  🌿 Your Eco Score: 847           │ │
│  │  ████████████░░░  Level 5         │ │
│  │  12 items recycled this month     │ │
│  ╰───────────────────────────────────╯ │
│                                        │
│       ╭──────────────────────╮         │
│       │   📷 SCAN ITEM       │         │
│       │  (Large CTA Button)  │         │
│       ╰──────────────────────╯         │
│                                        │
│  ╭──── Recent Activity (Glass) ──────╮ │
│  │  📷 Plastic Bottle    → Recycled  │ │
│  │  🤝 Power Drill       → Lent     │ │
│  │  ♻️ Old Clothes       → Donated   │ │
│  ╰───────────────────────────────────╯ │
│                                        │
│  ╭──── Community Impact (Glass) ─────╮ │
│  │  🌍 234 kg CO₂ saved             │ │
│  │  ♻️ 1,247 items recycled          │ │
│  │  🤝 89 items shared              │ │
│  ╰───────────────────────────────────╯ │
│                                        │
│ ┌──────────────────────────────────────┐│
│ │  🏠    ♻️     📷     🤝     👤     ││
│ │ Home  Market  Scan  Share  Profile  ││
│ └──────────────────────────────────────┘│
└────────────────────────────────────────┘

Tab Bar:
  🏠 Home       — Dashboard, eco-score, activity
  ♻️ Market     — Recycling marketplace
  📷 Scan       — AI scanner (center, larger)
  🤝 Share      — P2P lending/borrowing
  👤 Profile    — User profile, settings
```

### Key Screen Wireframes

```
┌──── SCAN RESULT SCREEN ──────────────┐
│                                       │
│  ← Back               💾 Save        │
│                                       │
│  ╭──── Item Photo ──────────────────╮ │
│  │        [Scanned Image]           │ │
│  ╰──────────────────────────────────╯ │
│                                       │
│  ╭──── AI Result (Glass Card) ──────╮ │
│  │  🏷 Plastic Bottle (PET)         │ │
│  │  📂 Category: Plastic             │ │
│  │  ✅ Recyclable: Yes               │ │
│  │  🌍 Eco Impact: Saves 0.04kg CO₂ │ │
│  │  ⏳ Decomposition: 450 years      │ │
│  │  🎯 Confidence: 94%              │ │
│  ╰──────────────────────────────────╯ │
│                                       │
│  ╭──── Recycling Instructions ──────╮ │
│  │  1. Rinse the bottle             │ │
│  │  2. Remove cap and label         │ │
│  │  3. Crush to save space          │ │
│  │  4. Place in recycling bin       │ │
│  ╰──────────────────────────────────╯ │
│                                       │
│  ╭──── Reuse Suggestions ───────────╮ │
│  │  💡 Plant pot for seedlings       │ │
│  │  💡 DIY bird feeder               │ │
│  │  💡 Storage container             │ │
│  ╰──────────────────────────────────╯ │
│                                       │
│  ╭──── Actions ─────────────────────╮ │
│  │  [🗺 Drop-off] [♻️ Sell] [🎁 Donate] │
│  │  [🤝 Lend]   [📋 Save]           │ │
│  ╰──────────────────────────────────╯ │
│                                       │
└───────────────────────────────────────┘

┌──── MARKETPLACE SCREEN ──────────────┐
│                                       │
│  Recycling Market         🗺 📍      │
│                                       │
│  ╭──── Search Bar ──────────────────╮ │
│  │  🔍 Search items...      ⚙ Filter│ │
│  ╰──────────────────────────────────╯ │
│                                       │
│  [All] [Sell] [Donate] [Pickup]      │
│                                       │
│  ╭──── Listing Card (Glass) ────────╮ │
│  │ [📷 img]  Old Laptop             │ │
│  │           💰 RM 50               │ │
│  │           📍 2.3 km away         │ │
│  │           ⭐ 4.8 (seller)        │ │
│  ╰──────────────────────────────────╯ │
│                                       │
│  ╭──── Listing Card (Glass) ────────╮ │
│  │ [📷 img]  Cardboard Boxes        │ │
│  │           🎁 Free (Donate)       │ │
│  │           📍 1.1 km away         │ │
│  │           ⭐ 4.5 (seller)        │ │
│  ╰──────────────────────────────────╯ │
│                                       │
│           ╭──────────╮               │
│           │ + Post   │               │
│           ╰──────────╯               │
│                                       │
│ ┌──────────────────────────────────┐  │
│ │ 🏠    ♻️     📷     🤝    👤   │  │
│ └──────────────────────────────────┘  │
└───────────────────────────────────────┘

┌──── P2P LENDING SCREEN ──────────────┐
│                                       │
│  Neighbourhood Share      🗺 📍      │
│                                       │
│  ╭──── Search Bar ──────────────────╮ │
│  │  🔍 Search items...      ⚙ Filter│ │
│  ╰──────────────────────────────────╯ │
│                                       │
│  [🔧Tools] [📱Tech] [📚Books]       │
│  [🍳Kitchen] [⚽Sports] [🌱Garden]  │
│                                       │
│  ╭──── Item Card (Glass) ───────────╮ │
│  │ [📷 img]  Power Drill            │ │
│  │           🔧 Tools               │ │
│  │           📍 0.5 km  ✅ Available │ │
│  │           ⭐ 4.9 (12 shares)     │ │
│  │           [📩 Borrow Request]    │ │
│  ╰──────────────────────────────────╯ │
│                                       │
│  ╭──── Item Card (Glass) ───────────╮ │
│  │ [📷 img]  Calculus Textbook      │ │
│  │           📚 Books               │ │
│  │           📍 1.2 km  ✅ Available │ │
│  │           ⭐ 4.7 (5 shares)      │ │
│  │           [📩 Borrow Request]    │ │
│  ╰──────────────────────────────────╯ │
│                                       │
│           ╭──────────╮               │
│           │ + Lend   │               │
│           ╰──────────╯               │
│                                       │
│ ┌──────────────────────────────────┐  │
│ │ 🏠    ♻️     📷     🤝    👤   │  │
│ └──────────────────────────────────┘  │
└───────────────────────────────────────┘
```

---

## 🗂 Firebase Data Schema

```
Firestore Collections:
│
├── users/
│   └── {userId}
│       ├── displayName: string
│       ├── email: string
│       ├── photoURL: string
│       ├── location: GeoPoint
│       ├── ecoScore: number
│       ├── totalRecycled: number
│       ├── totalShared: number
│       ├── trustScore: number
│       ├── achievements: string[]
│       └── createdAt: Timestamp
│
├── marketplace_listings/
│   └── {listingId}
│       ├── userId: string (ref → users)
│       ├── title: string
│       ├── description: string
│       ├── imageURLs: string[]
│       ├── category: string (plastic|glass|metal|paper|electronic|textile|organic|other)
│       ├── listingType: string (sell|donate|pickup)
│       ├── price: number (0 for donate)
│       ├── condition: string (new|good|fair|poor)
│       ├── location: GeoPoint
│       ├── locationName: string
│       ├── status: string (available|reserved|collected)
│       ├── interestedUsers: string[]
│       └── createdAt: Timestamp
│
├── lending_items/
│   └── {itemId}
│       ├── ownerId: string (ref → users)
│       ├── title: string
│       ├── description: string
│       ├── imageURLs: string[]
│       ├── category: string (tools|electronics|books|kitchen|sports|garden)
│       ├── available: boolean
│       ├── borrowedBy: string | null
│       ├── borrowedUntil: Timestamp | null
│       ├── location: GeoPoint
│       ├── locationName: string
│       ├── totalShares: number
│       ├── rating: number
│       └── createdAt: Timestamp
│
├── borrow_requests/
│   └── {requestId}
│       ├── itemId: string (ref → lending_items)
│       ├── borrowerId: string (ref → users)
│       ├── ownerId: string (ref → users)
│       ├── startDate: Timestamp
│       ├── endDate: Timestamp
│       ├── status: string (pending|approved|rejected|returned)
│       ├── message: string
│       └── createdAt: Timestamp
│
├── chats/
│   └── {chatId}
│       ├── participants: string[] (2 userIds)
│       ├── lastMessage: string
│       ├── lastMessageAt: Timestamp
│       └── messages/ (sub-collection)
│           └── {messageId}
│               ├── senderId: string
│               ├── text: string
│               ├── imageURL: string | null
│               └── sentAt: Timestamp
│
└── scan_history/ (also stored in local SQLite for offline)
    └── {scanId}
        ├── userId: string
        ├── imageURL: string
        ├── itemName: string
        ├── category: string
        ├── recyclable: boolean
        ├── aiResponse: JSON
        ├── actionTaken: string (recycled|sold|donated|lent|saved)
        └── scannedAt: Timestamp
```

### Local SQLite Schema (Offline-First)

```sql
-- Cached AI scan results (avoid repeat API calls)
CREATE TABLE scan_cache (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    cache_key TEXT UNIQUE,        -- hash of item_name + category
    response_json TEXT,           -- full Gemini API response
    created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
    expires_at DATETIME           -- 7 days from creation
);

-- User's scan history (available offline)
CREATE TABLE scan_history (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    image_uri TEXT,
    item_name TEXT,
    category TEXT,
    recyclable INTEGER,           -- 0 or 1
    ai_response TEXT,             -- full JSON response
    action_taken TEXT,            -- recycled/sold/donated/lent/saved
    synced INTEGER DEFAULT 0,    -- 0 = not synced to Firebase
    scanned_at DATETIME DEFAULT CURRENT_TIMESTAMP
);

-- Offline drafts for marketplace/lending posts
CREATE TABLE draft_posts (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    post_type TEXT,               -- marketplace or lending
    title TEXT,
    description TEXT,
    image_uris TEXT,             -- JSON array of local URIs
    category TEXT,
    listing_type TEXT,
    price REAL,
    synced INTEGER DEFAULT 0,
    created_at DATETIME DEFAULT CURRENT_TIMESTAMP
);
```

---

## 👥 Team Role Distribution (4 Members)

### Role Assignments

| Role | Member | Primary Ownership | Secondary |
|------|--------|-------------------|-----------|
| **Team Lead / Full-Stack** | Member A | App architecture, navigation, auth, integration | Project management, Firebase setup |
| **Frontend / UI Dev** | Member B | All UI screens, glassmorphism components, animations, launcher icon | Wireframes for proposal |
| **AI / Core Logic Dev** | Member C | AI scanner (Gemini API), camera, barcode, Open Food Facts, scan results | Data models, search |
| **Backend / Marketplace Dev** | Member D | Firebase CRUD, chat system, marketplace & lending backend, maps, QA | Huawei AppGallery publishing |

### Development Task Ownership

| Screen / Feature | Developer | Depends On |
|-----------------|-----------|------------|
| **Splash Screen + Onboarding** | Member B | — |
| **Auth (Login / Register / Logout)** | Member A | Firebase Auth |
| **Tab Navigation Shell** | Member A | Expo Router |
| **Home Dashboard** | Member B | Zustand store |
| **AI Scanner — Camera Capture** | Member C | expo-camera |
| **AI Scanner — Gemini API Call** | Member C | API key setup |
| **AI Scanner — Result Card UI** | Member B + C | AI response format |
| **AI Scanner — Barcode + Open Food Facts** | Member C | expo-barcode-scanner |
| **Scan History Screen** | Member C | SQLite |
| **Marketplace — Browse/Search** | Member D | Firestore queries |
| **Marketplace — Post Listing** | Member D | Firebase Storage |
| **Marketplace — Detail + Chat** | Member D | Firebase Realtime DB |
| **P2P Lending — Browse/Search** | Member D | Firestore queries |
| **P2P Lending — Post Item** | Member D | Firebase Storage |
| **P2P Lending — Borrow Request** | Member D | Firestore |
| **Map View (all modules)** | Member A | Google Maps API |
| **Nearby Drop-off Points** | Member A | Maps + Places API |
| **Profile Screen** | Member A | Firestore user doc |
| **Settings (Theme toggle, etc.)** | Member A | Zustand store |
| **Gamification (Eco-score, badges)** | Member D | Firestore |
| **Glassmorphism Component Library** | Member B | expo-blur |
| **Custom Launcher Icon** | Member B | — |

### Report Writing Distribution

#### Part 1 — Proposal (4–10 pages, due Week 5)

| Section | Writer | Est. Pages |
|---------|--------|------------|
| Cover Page + Table of Contents | Member D | 1 |
| Introduction + Problem Statement + SDG 12 | Member A | 1.5 |
| Proposed Solution + 3 Pillars + Feature List + Use Cases | Member C | 2.5 |
| UI/UX Design — Wireframes + Mockups + User Flow Diagram | Member B | 3 |
| Technical Architecture + Tech Stack + AI Flow + Conclusion | Member D | 2 |
| **Review, proofread, format** | **All** | — |

#### Part 2 — Final Report (≤10 pages + Appendix, due Week 12)

| Section | Writer | Est. Pages |
|---------|--------|------------|
| Introduction + App Overview + System Architecture | Member A | 2 |
| UI Screenshots + Design Rationale | Member B | 2 |
| AI Scanner Deep-Dive + API Integration + Challenges | Member C | 2.5 |
| Marketplace & Lending Features + Testing + Deployment + Contribution Log | Member D | 2.5 |
| Unimplemented Features / Future Work | Member A | 1 |
| Appendix: Key Source Code Excerpts | All (own code) | As needed |
| **Review, proofread, format** | **All** | — |

### Presentation Speaking Roles (Week 13, 10 min)

| Speaker | Duration | Topic |
|---------|----------|-------|
| Member A | 2.5 min | Introduction, architecture overview, maps integration |
| Member B | 2.5 min | UI/UX walkthrough, glassmorphism demo, live app tour |
| Member C | 2.5 min | Live AI scanning demo, barcode scan, Open Food Facts |
| Member D | 2.5 min | Marketplace demo, chat, lending flow, publishing |

---

## 📅 14-Week Schedule

### Phase 1: Planning & Proposal (Weeks 1–5)

---

#### Week 1 — Project Kickoff & Setup
| Task | Owner | Deliverable |
|------|-------|-------------|
| Read & understand assignment requirements | All | Shared understanding |
| Finalise app name and concept | All | App name decided |
| Create GitHub repository + invite all members | Member A | Repo URL |
| Register Huawei Developer account | Member D | Account created |
| Set up Expo project with TypeScript boilerplate | Member A | `npx create-expo-app` done |
| Get Google AI Studio API key (Gemini) | Member C | API key ready |
| Set up Firebase project (Auth + Firestore) | Member D | Firebase console ready |
| Research Open Food Facts API endpoints | Member C | API docs reviewed |

---

#### Week 2 — Requirements & Design
| Task | Owner | Deliverable |
|------|-------|-------------|
| Define all user stories per module | All | User story list |
| Create low-fidelity wireframes (all screens) | Member B | Paper/Figma wireframes |
| Design data schema (Firestore + SQLite) | Member D | Schema document |
| Test Gemini Vision API with sample images | Member C | Working API call proof |
| Test Open Food Facts API with sample barcodes | Member C | Working API call proof |
| Start glassmorphism design system (tokens, components) | Member B | Style guide draft |

---

#### Week 3 — Proposal Writing Phase 1
| Task | Owner | Deliverable |
|------|-------|-------------|
| Write Introduction + Problem Statement | Member A | Draft (1.5 pages) |
| Write Proposed Solution + Features + Use Cases | Member C | Draft (2.5 pages) |
| Create high-fidelity UI mockups in Figma | Member B | Polished mockups |
| Write Technical Architecture + AI Flow | Member D | Draft (2 pages) |
| Begin coding: Expo Router tab navigation | Member A | Working skeleton |

---

#### Week 4 — Proposal Writing Phase 2
| Task | Owner | Deliverable |
|------|-------|-------------|
| Compile all proposal sections into single document | Member A | Full draft |
| Add UI mockups & screenshots to proposal | Member B | Embedded visuals |
| Peer review all sections (everyone reads everything) | All | Feedback notes |
| Format document (cover page, headers, page numbers) | Member D | Polished layout |
| Continue coding: Auth flow (login/register screens) | Member A | Auth UI ready |

---

#### Week 5 — ⚠️ Proposal Due (Wed 15 July, 5 PM)
| Task | Owner | Deliverable |
|------|-------|-------------|
| Final proofread and formatting check | All | Final document |
| **Submit Part 1 proposal via Google Form** | **Member A** | **✅ SUBMITTED** |
| Begin: Tab navigation + Home dashboard UI | Member B | Home screen started |
| Begin: Camera capture integration | Member C | Camera working |
| Begin: Firestore CRUD operations | Member D | Database connected |

---

### Phase 2: Core Development (Weeks 6–9)

---

#### Week 6 — Foundation Sprint
| Task | Owner | Deliverable |
|------|-------|-------------|
| Complete Firebase Auth (login/register/logout/forgot) | Member A | Auth flow complete |
| Build glassmorphism component library (GlassCard, GlassButton, GlassInput, GlassModal) | Member B | Component library |
| Implement camera capture + gallery picker | Member C | Image capture working |
| Set up Firestore collections + CRUD helpers | Member D | Data layer ready |
| Implement SQLite local storage (scan cache + history) | Member D | Local DB ready |
| Build Home dashboard screen | Member B | Dashboard UI done |

---

#### Week 7 — AI Scanner Sprint
| Task | Owner | Deliverable |
|------|-------|-------------|
| Integrate Gemini Vision API — image scan | Member C | AI scanning working |
| Integrate Gemini Text API — text/keyword search | Member C | Text search working |
| Integrate barcode scanner + Open Food Facts API | Member C | Barcode scan working |
| Build scan result card UI | Member B | Result screen polished |
| Build scan history screen (local SQLite) | Member C | History screen done |
| Integrate Google Maps — nearby drop-off points | Member A | Map view working |

---

#### Week 8 — Marketplace Sprint
| Task | Owner | Deliverable |
|------|-------|-------------|
| Build marketplace browse/search screen | Member D | Listings screen done |
| Build marketplace post listing flow | Member D | Post flow working |
| Build marketplace detail screen | Member D | Detail screen done |
| Implement in-app chat (Firebase Realtime DB) | Member D | Chat working |
| Build marketplace map view | Member A | Map view done |
| Polish scanner → marketplace flow (from scan result → post) | Member C | Flow connected |

---

#### Week 9 — P2P Lending Sprint + Integration
| Task | Owner | Deliverable |
|------|-------|-------------|
| Build P2P lending browse/search screen | Member D | Lending screen done |
| Build P2P lending post item flow | Member D | Post flow working |
| Build borrow request + approval flow | Member D | Request flow done |
| Build profile screen + eco-score | Member A | Profile done |
| Build settings screen (theme toggle, notifications) | Member A | Settings done |
| Implement gamification (badges, streaks) | Member D | Gamification working |
| Design & create custom launcher icon | Member B | App icon ready |
| Polish all animations & transitions | Member B | Smooth UX |
| **FEATURE FREEZE** — no new features after this week | All | Scope locked |

---

### Phase 3: Polish & Documentation (Weeks 10–12)

---

#### Week 10 — Testing & Bug Fixing
| Task | Owner | Deliverable |
|------|-------|-------------|
| End-to-end testing on physical Android devices | All | Bug list created |
| Fix critical bugs in own modules | All (own areas) | Bugs resolved |
| Performance optimisation (image compression, lazy loading) | Member A | Faster app |
| UI consistency pass (spacing, fonts, colours, icon sizes) | Member B | Pixel-perfect |
| Edge case testing (no network, empty states, error handling) | Member D | Error states handled |
| Test all 3 scan modes (image, text, barcode) | Member C | All modes verified |

---

#### Week 11 — Report Writing + Build
| Task | Owner | Deliverable |
|------|-------|-------------|
| Write Part 2: Introduction + Architecture | Member A | Draft sections |
| Screenshot all screens + annotate for report | Member B | Screenshot set |
| Write Part 2: AI Scanner deep-dive | Member C | Draft sections |
| Write Part 2: Marketplace + Lending + Testing | Member D | Draft sections |
| **Build APK via EAS Build** | Member A | Installable APK file |
| Submit APK to Huawei AppGallery | Member D | Submission started |

---

#### Week 12 — ⚠️ Final Submission (Sat 5 Sept, 5 PM)
| Task | Owner | Deliverable |
|------|-------|-------------|
| Compile & format complete final report | Member A | Full report document |
| Peer review all report sections | All | Final corrections done |
| Ensure all GitHub commits properly attributed | All | Clean git log |
| **Submit Part 2 via Google Form** | **Member A** | **✅ SUBMITTED** |
| Check Huawei AppGallery review status | Member D | Follow up if needed |
| Last-minute bug fixes only if critical | All | Stable build |

---

### Phase 4: Presentation (Weeks 13–14)

---

#### Week 13 — ⚠️ Presentation (During Practical Session)
| Task | Owner | Deliverable |
|------|-------|-------------|
| Prepare slide deck (10 min presentation) | All | Slides ready |
| Rehearse demo flow on real device | All | Smooth demo rehearsed |
| Prepare sample items for live scanning demo | Member C | Demo items ready |
| Prepare Q&A — each member studies their own code deeply | All | Q&A ready |
| **Present & demonstrate the app** | **All** | **✅ PRESENTED** |

---

#### Week 14 — Wrap-Up
| Task | Owner | Deliverable |
|------|-------|-------------|
| Reflect on presentation feedback | All | Lessons learned |
| Final code cleanup + README on GitHub | All | Clean repo |
| Archive all project files | Member A | Backed up |

---

## ✅ Minimum Requirements Checklist

| Requirement | How We Meet It | Status |
|-------------|---------------|--------|
| Custom launcher icon | Designed by Member B, themed to chosen app name | ⬜ |
| Store, update & retrieve data from device storage | expo-sqlite: scan_cache, scan_history, draft_posts tables | ⬜ |
| Connect to external endpoint (REST API / SDK) | Firebase (Firestore, Auth, Storage, Realtime DB) + Gemini API + Google Maps + Open Food Facts | ⬜ |

---

## 🔧 Development Environment Setup

```
Required Tools:
├── Node.js (v20 LTS)
├── npm or yarn
├── Expo CLI (npx expo)
├── VS Code + Extensions:
│   ├── ESLint
│   ├── Prettier
│   ├── React Native Tools
│   └── TypeScript
├── Git + GitHub account
├── Android Studio (emulator) OR Expo Go on physical phone
├── Firebase Console account (Google account)
├── Google AI Studio account (Gemini API key)
├── Google Cloud Console (Maps API key)
└── Huawei Developer account (register Week 1!)
```

---

## ⚠️ Risk Management

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| Gemini API rate limit (15 RPM free) | Medium | High | Cache results in SQLite (7-day TTL); debounce scans |
| Google Maps API cost | Low | Medium | $200/month free credit; limit map loads |
| Open Food Facts missing products | Medium | Low | Fallback to Gemini text scan for unknown barcodes |
| Team member unavailability | Medium | High | Clear ownership; no single points of failure; weekly sync |
| Feature creep beyond Week 9 | High | Medium | Strict feature freeze; polish only after Week 9 |
| Huawei AppGallery approval delay | Medium | Low | Register Week 1; submit Week 11 for buffer |
| Chat system complexity | Medium | Medium | Keep it simple: text only, no images/voice in chat |
| Performance on low-end Android | Low | Medium | Compress images before upload; lazy load lists |

---

## 📝 Decisions Needed From You

1. **App name?** — ReLoop / EcoCircle / GreenSwap / CircleWise / ReKind (or your own idea)
2. **Color palette?** — Nature Green 🟢 / Ocean Teal 🔵 / Fresh Lime 🍃 (or custom)
3. **Dark mode + Light mode, or just one?** (Recommend: both with toggle)
4. **Chat feature priority?** — Full chat or simplified (just contact buttons)?
5. **Any team member experienced with React Native / JavaScript / Firebase?**

---

> **Once you confirm these decisions, I'll scaffold the full Expo project with your chosen theme and start building!**
