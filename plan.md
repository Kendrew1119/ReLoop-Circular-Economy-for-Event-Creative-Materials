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
| Creativity / Novelty / Usefulness | 40% | ×4 | **Highest priority** — Event + Creative waste circular economy is a unique, untapped niche |
| Completeness of Idea | 30% | ×3 | Cover all 3 pillars: Scan → Marketplace → Share |
| Overall Design (UI) | 20% | ×2 | Glassmorphism wireframes, iOS-style mockups |
| Neat Documentation | 10% | ×1 | Clean formatting, good structure |

### Part 2 — Working App + Report (100 marks → 20% of final)

| Criteria | Weight | Multiplier | Notes |
|----------|--------|------------|-------|
| Program completeness & functionality | 30% | ×3 | All 3 core modules must work end-to-end |
| Actual design & creativity | 10% | ×1 | Match or exceed proposal design |
| Potential for civil/commercial use | 5% | ×0.5 | Real-world applicability — campus + commercial events |
| Tidiness of source code | 5% | ×0.5 | Clean, commented, modular code |
| Documentation (individual) | 20% | ×2 | Clear role labels, GitHub contributions |
| Presentation (individual) | 15% | ×1.5 | 10-min demo |
| Q&A (individual) | 15% | ×1.5 | Understand your own code deeply |
| **Bonus**: Published on Play Store / AppGallery | Extra | — | Register Huawei dev account early |

---

## 💡 The App Concept

### App Name: **EventLoop**

> **Tagline:** *Scan. Recycle. Share. Repeat.*  
> **Niche Focus:** Event & Creative Project Materials  

EventLoop is a circular economy mobile app focused on **event materials** and **creative project supplies**. It targets two user groups:

| User Group | Examples | Pain Point |
|-----------|---------|------------|
| **Campus Users** | Student societies, club committees, uni event organizers | Clubs waste banners, decorations, props after every event; no easy way to pass them to the next organizer |
| **Global Event Users** | Wedding planners, exhibition organizers, corporate event teams, cosplayers, DIY makers | Events generate massive one-time-use waste (lanyards, backdrops, foam boards); crafters need exactly those leftover materials |

### Why This Niche Works

1. **No existing competitor** — Riiicycle, EcoScan, Recircle all focus on general household recycling. No app targets event/creative materials specifically.
2. **Huge waste problem** — A single campus carnival generates 50+ kg of disposable banners, signage, and decorations. Corporate exhibitions are even worse.
3. **Natural circular loop** — One event's trash is the next event's treasure. A banner from UTAR Open Day can become a cosplayer's backdrop or a student society's orientation material.
4. **P2P lending is perfect** — Expensive equipment (PA systems, projectors, sewing machines, heat guns) is needed for days, not months.
5. **AI scanner is highly relevant** — Scan a PVC banner → AI tells you it's recyclable and suggests who nearby can upcycle it.

---

### Core Concept — 3 Pillars

```
┌─────────────────────────────────────────────────────────────────┐
│                     EventLoop App                                   │
│          Event & Creative Materials Circular Economy              │
│                                                                  │
│   🔍 SCAN            ♻️ MARKETPLACE       🤝 SHARE              │
│   AI Scanner         Material Exchange     Equipment Lending     │
│                                                                  │
│   • Photo scan       • Post leftover       • Lend equipment      │
│   • AI identify        event materials     • Borrow tools        │
│   • Material type    • Sell / Donate /     • Campus societies    │
│   • Recycle tips       Request pickup      • Availability        │
│   • Upcycle ideas    • Chat with buyer       calendar            │
│   • Eco impact       • Map view            • Trust rating        │
│   • Drop-off pts     • Category filter     • Return tracking     │
└─────────────────────────────────────────────────────────────────┘
```

---

### SDG 12 Alignment & Design Components

| Assignment Requirement | How EventLoop Addresses It |
|----------------------|------------------------|
| **P2P Resource Optimisation** | ✅ Equipment lending — share PA systems, projectors, craft tools between campus clubs & creators |
| **Behavioural Transformation** | ✅ AI scanner educates users on material recycling/upcycling; gamified eco-score nudges reuse habits |
| **Closing the Loop** | ✅ Marketplace connects event waste producers with crafters/next event organizers who need those materials |
| **Originality** | ✅ No existing app targets event + creative material waste — unique niche with 3-in-1 approach |
| **Technological Integration** | ✅ Gemini AI (vision + text), Google Maps API, Firebase real-time |
| **Feasibility** | ✅ Well-scoped; all APIs have free tiers; demo-able with real campus event materials |

---

## 📂 Category System

### Material Categories (for AI Scanner & Marketplace)

These are the categories the AI will classify scanned items into, and that users will select when posting to the marketplace:

| Category ID | Icon | Label | Example Items |
|-------------|------|-------|---------------|
| `banner` | 🏳️ | Banners & Signage | PVC banners, vinyl backdrops, foam boards, coroplast signs, roll-up standees |
| `decoration` | 🎨 | Decorations & Props | Paper flowers, balloon arches, stage props, photo booth frames, fairy lights |
| `fabric` | 🧵 | Fabric & Textile | Tablecloths, skirting, curtains, cosplay fabric offcuts, satin, tulle |
| `stationery` | 📦 | Stationery & Print | Lanyards, name tags, pamphlets, leftover printed flyers, certificates |
| `craft` | ✂️ | Craft Supplies | EVA foam, spray paint, hot glue sticks, acrylic paint, wire, clay |
| `wood` | 🪵 | Wood & Structural | Plywood offcuts, wooden frames, booth structures, pallets |
| `electronic` | ⚡ | Event Electronics | LED strips, extension cables, used batteries, broken speakers |
| `packaging` | 📦 | Packaging & Containers | Bubble wrap, styrofoam boxes, plastic containers, cardboard boxes |
| `other` | 🔄 | Other | Anything that doesn't fit the above |

### Equipment Categories (for P2P Lending)

| Category ID | Icon | Label | Example Items |
|-------------|------|-------|---------------|
| `av` | 🎤 | Audio / Visual | PA systems, speakers, microphones, projectors, screens |
| `tools` | 🔧 | Tools & Hardware | Drill, heat gun, Dremel, jigsaw, soldering iron, staple gun |
| `sewing` | 🪡 | Sewing & Craft Tools | Sewing machines, overlock machines, cutting mats, rotary cutters |
| `lighting` | 💡 | Lighting & Decor | Stage lights, ring lights, fairy light sets, spotlight stands |
| `furniture` | 🪑 | Event Furniture | Folding tables, chairs, canopy tents, exhibition stands |
| `transport` | 🚐 | Transport & Logistics | Trolleys, hand trucks, cargo straps, roof racks |

---

## 🧠 AI System Architecture & Flow

### Complete AI Pipeline

```
┌──────────────────────────────────────────────────────────────────┐
│                    AI PROCESSING PIPELINE                         │
│                                                                   │
│  ┌──────────────┐   ┌──────────────┐   ┌─────────────────────┐  │
│  │   INPUT       │──▶│  PROCESSING  │──▶│   OUTPUT             │  │
│  │              │   │              │   │                     │  │
│  │ 📷 Camera    │   │ Gemini 2.5   │   │ • item_name         │  │
│  │ 🖼 Gallery   │   │ Flash Vision │   │ • category (enum)   │  │
│  │ 📝 Text     │   │ API          │   │ • material_type     │  │
│  │              │   │              │   │ • recyclable (bool) │  │
│  └──────────────┘   └──────────────┘   │ • recycle_steps[]   │  │
│                                         │ • upcycle_ideas[]   │  │
│                                         │ • eco_impact {}     │  │
│                                         │ • confidence (0-1)  │  │
│                                         └─────────────────────┘  │
└──────────────────────────────────────────────────────────────────┘
```

### Scan Mode 1: Image Scan (Primary)

```
User opens camera / selects from gallery
       │
       ▼
Image preprocessed (compress to 1024px, convert to base64)
       │
       ▼
Send to Gemini 2.5 Flash Vision API
┌──────────────────────────────────────────────────────────────┐
│  System Prompt:                                               │
│  "You are EventLoop AI, an expert in event materials, creative   │
│   supplies, and circular economy. You specialise in           │
│   identifying materials commonly used in events, exhibitions, │
│   cosplay, and DIY projects. Provide practical recycling and  │
│   upcycling advice specific to Malaysia. Always return valid  │
│   JSON."                                                      │
│                                                               │
│  User Prompt:                                                 │
│  "Identify this item. Return JSON:                            │
│   {                                                           │
│     item_name: string,                                        │
│     category: enum(banner|decoration|fabric|stationery|       │
│               craft|wood|electronic|packaging|other),          │
│     material_type: string (e.g. 'PVC', 'EVA foam', 'Plywood')│
│     recyclable: boolean,                                      │
│     recycle_steps: string[] (step-by-step instructions),      │
│     upcycle_ideas: string[] (3 creative reuse ideas for       │
│                     events or crafts),                         │
│     eco_impact: {                                             │
│       co2_saved_kg: number,                                   │
│       decomposition_time: string,                             │
│       landfill_diversion: string                              │
│     },                                                        │
│     confidence: number (0.0 to 1.0)                           │
│   }"                                                          │
└──────────────────────────────────────────────────────────────┘
       │
       ▼
Parse JSON response
       │
       ▼
Display result card (glassmorphism UI)
       │
       ├──▶ [🗺 Drop-off]  → Google Maps: nearby recycling centres
       ├──▶ [♻️ Sell]       → Pre-fill marketplace post with AI data
       ├──▶ [🎁 Donate]    → Pre-fill marketplace post (price = 0)
       ├──▶ [🤝 Lend]      → Pre-fill lending post with AI data
       └──▶ [📋 Save]      → Save to local scan history (SQLite)
```

### Scan Mode 2: Text/Keyword Search

```
User types item name (e.g., "PVC banner" or "EVA foam sheet")
       │
       ▼
Send to Gemini 2.5 Flash Text API (same system prompt + schema)
       │
       ▼
Same result card UI as image scan
```

### AI Response Caching (SQLite)

```
Scan result received from Gemini API
       │
       ▼
Hash (item_name + category) → cache_key
       │
       ▼
Store in local SQLite: scan_cache table
       │
       ▼
On next scan of same/similar item:
  → Check cache first (if < 7 days old) → skip API call
  → Saves API quota (free tier: 15 RPM)
```

### AI → Marketplace/Lending Flow (Auto-Fill)

```
User scans an item (e.g., "Used PVC Banner")
       │
       ▼
AI returns: { item_name, category: "banner", material_type: "PVC", ... }
       │
       ├── User taps [♻️ Sell] or [🎁 Donate]
       │       │
       │       ▼
       │   Pre-fill marketplace post form:
       │     title      = AI item_name ("PVC Banner 3x5ft")
       │     category   = AI category ("banner")
       │     condition   = user selects
       │     image       = scanned photo auto-attached
       │     description = AI upcycle_ideas as suggestion
       │     → User adds price, location → Submit
       │
       └── User taps [🤝 Lend]
               │
               ▼
           Pre-fill lending post form:
             title    = AI item_name
             category = mapped to equipment category if applicable
             image    = scanned photo auto-attached
             → User adds availability dates → Submit
```

---

## 🗺 Google Maps Integration

### Map Usage Across the App

| Screen | Map Feature | Data Source | API Used |
|--------|------------|-------------|----------|
| **Scan Result → Drop-off** | Show nearby recycling centres/kitar semula on map | Google Places (type: recycling) | Places API + Maps SDK |
| **Marketplace → Map View** | Pins showing all marketplace listings near user | Firestore GeoPoint data | Maps SDK |
| **Marketplace → Listing Detail** | Single pin for the listing; show distance from user | Firestore GeoPoint | Maps SDK + Geocoding |
| **Lending → Map View** | Pins showing all lendable items near user | Firestore GeoPoint data | Maps SDK |
| **Post Listing / Post Item** | User picks location on map or auto-detects GPS | expo-location | Maps SDK + Geocoding |
| **Chat → Share Location** | Share meeting point for pickup/return | Manual pin drop | Maps SDK |

### Map Data Flow

```
User opens Map View (Marketplace or Lending)
       │
       ▼
expo-location: get user's current GPS coordinates
       │
       ▼
Firestore query: get all listings/items within X km radius
  (using GeoPoint field + Geohash for efficient geo-queries)
       │
       ▼
Render markers on react-native-maps MapView
  → Each marker = one listing/item
  → Tap marker → show preview card (glass card overlay)
  → Tap card → navigate to detail screen
```

### Drop-off Point Flow (from Scan Result)

```
User taps [🗺 Drop-off] on scan result
       │
       ▼
Get user's current location (expo-location)
       │
       ▼
Google Places API: nearbySearch
  → type: "recycling_center" OR keyword: "kitar semula"
  → radius: 10km from user
       │
       ▼
Display results on map + as list below
  → Each result shows: name, distance, open/closed, rating
  → Tap → open Google Maps for navigation
```

---

## 📱 App Feature Breakdown

### Module 1: 🔍 AI Smart Scanner

| Feature | Description | API / Tech |
|---------|-------------|------------|
| **Camera Scan** | Capture photo of event material → AI identification | expo-camera → Gemini Vision |
| **Gallery Upload** | Pick existing photo for scanning | expo-image-picker → Gemini Vision |
| **Text Search** | Type material name for recycling/upcycle info | Gemini Text |
| **Result Card** | Glassmorphism card: item name, category, material, recycle steps, upcycle ideas, eco impact | Custom UI |
| **Action Buttons** | Drop-off / Sell / Donate / Lend / Save | Navigation actions |
| **Auto-Fill Post** | AI data pre-fills marketplace or lending post form | Zustand state transfer |
| **Scan History** | Past scans saved locally with timestamps | expo-sqlite |

### Module 2: ♻️ Material Marketplace

| Feature | Description | Tech |
|---------|-------------|------|
| **Post Listing** | Upload leftover event material with photo, description, category, condition, price | Firestore + Firebase Storage |
| **Listing Types** | Sell (set price in RM) / Donate (free) / Request Pickup | Firestore field: `listingType` |
| **Browse** | Scrollable list of cards with photo, title, price, distance | FlatList + Firestore |
| **Search** | Keyword search across title and description | Firestore query |
| **Category Filter** | Filter by material category (Banner, Decoration, Fabric, etc.) | Firestore `where` clause |
| **Map View** | Toggle between list view and map view | react-native-maps |
| **Listing Detail** | Full details, seller info, location on map | Detail screen |
| **In-App Chat** | Real-time messaging between poster & buyer | Firebase Realtime DB |
| **Request Pickup** | Buyer/recycler requests to pick up the material | Firestore status update |
| **Listing Status** | Available → Reserved → Collected/Sold | Firestore update |

### Module 3: 🤝 Equipment Lending

| Feature | Description | Tech |
|---------|-------------|------|
| **Post Item to Lend** | List equipment (PA system, heat gun, sewing machine, etc.) | Firestore + Firebase Storage |
| **Browse** | Scrollable list with category chips (AV, Tools, Sewing, etc.) | FlatList + Firestore |
| **Search** | Keyword search across title and description | Firestore query |
| **Category Filter** | Filter by equipment category (AV, Tools, Sewing, Lighting, etc.) | Firestore `where` clause |
| **Map View** | See lendable items on map near you | react-native-maps |
| **Borrow Request** | Send request to owner with needed dates + message | Firestore sub-document |
| **Availability Calendar** | Visual date picker showing when item is free / booked | Date picker component |
| **In-App Chat** | Coordinate pickup & return between lender & borrower | Firebase Realtime DB |
| **Return Tracking** | Mark item as returned; rate the experience | Firestore update |
| **Trust Score** | Reputation built from completed shares + ratings | Calculated field |

### Module 4: 🏠 Home Dashboard

| Feature | Description |
|---------|-------------|
| **Eco Score** | Personal sustainability score — +10 per item recycled/shared |
| **Quick Scan Button** | Large CTA to open scanner instantly |
| **Recent Activity** | Latest scans, marketplace posts, lending activity |
| **Community Stats** | Total materials diverted, items shared, CO₂ saved |
| **Daily Tip** | AI-generated sustainability tip for event organizers (Gemini) |

### Module 5: 👤 Profile & Settings

| Feature | Description |
|---------|-------------|
| **User Profile** | Name, photo, location, eco-score badge, user type (organizer/crafter/both) |
| **My Listings** | All my marketplace posts |
| **My Lent Items** | All my equipment lending posts |
| **My Scan History** | All past AI scans |
| **Achievements** | Badges: First Scan, 10 Items Listed, 5 Items Shared, etc. |
| **Settings** | Dark/light mode toggle, notification preferences, location |

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
│       ├── userType: string (organizer|crafter|both)
│       ├── location: GeoPoint
│       ├── locationName: string
│       ├── ecoScore: number
│       ├── totalRecycled: number
│       ├── totalShared: number
│       ├── trustScore: number
│       ├── totalRatings: number
│       ├── achievements: string[]
│       └── createdAt: Timestamp
│
├── marketplace_listings/
│   └── {listingId}
│       ├── userId: string (ref → users)
│       ├── title: string
│       ├── description: string
│       ├── imageURLs: string[]
│       ├── category: string (banner|decoration|fabric|stationery|craft|wood|electronic|packaging|other)
│       ├── materialType: string (e.g. "PVC", "EVA foam")
│       ├── listingType: string (sell|donate|pickup)
│       ├── price: number (0 for donate)
│       ├── condition: string (new|good|fair|poor)
│       ├── location: GeoPoint
│       ├── locationName: string
│       ├── status: string (available|reserved|collected)
│       ├── interestedUsers: string[]
│       ├── aiGenerated: boolean (true if auto-filled from scan)
│       └── createdAt: Timestamp
│
├── lending_items/
│   └── {itemId}
│       ├── ownerId: string (ref → users)
│       ├── title: string
│       ├── description: string
│       ├── imageURLs: string[]
│       ├── category: string (av|tools|sewing|lighting|furniture|transport)
│       ├── available: boolean
│       ├── borrowedBy: string | null
│       ├── borrowedUntil: Timestamp | null
│       ├── location: GeoPoint
│       ├── locationName: string
│       ├── totalShares: number
│       ├── rating: number
│       ├── totalRatings: number
│       └── createdAt: Timestamp
│
├── borrow_requests/
│   └── {requestId}
│       ├── itemId: string (ref → lending_items)
│       ├── borrowerId: string (ref → users)
│       ├── ownerId: string (ref → users)
│       ├── startDate: Timestamp
│       ├── endDate: Timestamp
│       ├── status: string (pending|approved|rejected|active|returned)
│       ├── message: string
│       └── createdAt: Timestamp
│
├── chats/
│   └── {chatId}
│       ├── participants: string[] (2 userIds)
│       ├── relatedListingId: string | null
│       ├── relatedItemId: string | null
│       ├── lastMessage: string
│       ├── lastMessageAt: Timestamp
│       └── messages/ (sub-collection)
│           └── {messageId}
│               ├── senderId: string
│               ├── text: string
│               └── sentAt: Timestamp
│
└── scan_history/ (also stored in local SQLite for offline)
    └── {scanId}
        ├── userId: string
        ├── imageURL: string
        ├── itemName: string
        ├── category: string
        ├── materialType: string
        ├── recyclable: boolean
        ├── aiResponse: map (full parsed JSON)
        ├── actionTaken: string (recycled|sold|donated|lent|saved|none)
        └── scannedAt: Timestamp
```

### Local SQLite Schema (Offline-First)

```sql
-- Cached AI scan results (avoid repeat API calls)
CREATE TABLE scan_cache (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    cache_key TEXT UNIQUE,
    response_json TEXT,
    created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
    expires_at DATETIME
);

-- User's scan history (available offline)
CREATE TABLE scan_history (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    image_uri TEXT,
    item_name TEXT,
    category TEXT,
    material_type TEXT,
    recyclable INTEGER,
    ai_response TEXT,
    action_taken TEXT,
    synced INTEGER DEFAULT 0,
    scanned_at DATETIME DEFAULT CURRENT_TIMESTAMP
);

-- Offline drafts for marketplace/lending posts
CREATE TABLE draft_posts (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    post_type TEXT,
    title TEXT,
    description TEXT,
    image_uris TEXT,
    category TEXT,
    listing_type TEXT,
    price REAL,
    synced INTEGER DEFAULT 0,
    created_at DATETIME DEFAULT CURRENT_TIMESTAMP
);
```

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
| **Camera** | **expo-camera** + **expo-image-picker** | Photo capture + gallery selection |
| **Location** | **expo-location** | GPS for user position, distance calculation |
| **Blur/Glass** | **expo-blur** + **expo-linear-gradient** | Glassmorphism UI effects |
| **Charts** | **react-native-chart-kit** | Eco-score dashboard, impact stats |
| **Icons** | **@expo/vector-icons** (Ionicons) | iOS-like icon set |
| **Fonts** | **Inter** (Google Fonts) | Clean, modern, readable |
| **Version Control** | **GitHub** | Required for contribution tracking |
| **Publishing** | **Huawei AppGallery** (free) | Register ASAP — approval takes days |

### External APIs Summary

| API | Purpose | Free Tier | Usage in App |
|-----|---------|-----------|-------------|
| **Gemini 2.5 Flash** | Image recognition, text generation, recycling/upcycling info | 15 RPM free | AI Scanner (image + text modes) |
| **Google Maps Platform** | Map display, geocoding, places search, directions | $200/month credit | Drop-off locator, marketplace map, lending map |
| **Firebase** | Auth, Firestore, Storage, Realtime DB | Spark plan (free) | All backend services |

---

## 📁 File Structure & Routing

```
mobileapp/
├── app/                              # Expo Router (file-based navigation)
│   ├── _layout.tsx                   # Root layout: providers (Auth, Zustand, Theme)
│   ├── index.tsx                     # Entry redirect: → auth or (tabs)
│   │
│   ├── auth/                         # Auth Stack
│   │   ├── _layout.tsx               # Auth stack layout
│   │   ├── login.tsx                 # Login screen
│   │   └── register.tsx              # Register screen
│   │
│   ├── (tabs)/                       # Main Tab Navigator
│   │   ├── _layout.tsx               # Tab bar config (5 tabs)
│   │   ├── index.tsx                 # 🏠 Home Dashboard
│   │   ├── market.tsx                # ♻️ Material Marketplace (list view)
│   │   ├── scan.tsx                  # 📷 AI Scanner (camera + text input)
│   │   ├── share.tsx                 # 🤝 Equipment Lending (list view)
│   │   └── profile.tsx              # 👤 Profile & Settings
│   │
│   ├── scan-result.tsx              # AI scan result detail (push from scan)
│   ├── market/
│   │   ├── [id].tsx                  # Marketplace listing detail
│   │   ├── post.tsx                  # Post new marketplace listing
│   │   └── map.tsx                   # Marketplace map view
│   ├── share/
│   │   ├── [id].tsx                  # Lending item detail
│   │   ├── post.tsx                  # Post new lending item
│   │   └── map.tsx                   # Lending map view
│   ├── chat/
│   │   ├── index.tsx                 # Chat list (all conversations)
│   │   └── [chatId].tsx             # Individual chat thread
│   └── dropoff.tsx                  # Drop-off points map (from scan result)
│
├── components/
│   ├── ui/                           # Glassmorphism design system
│   │   ├── GlassCard.tsx             # Frosted glass card container
│   │   ├── GlassButton.tsx           # Frosted glass button
│   │   └── GlassInput.tsx            # Frosted glass text input
│   ├── ScanResultCard.tsx            # AI result display card
│   ├── ListingCard.tsx               # Marketplace listing card
│   ├── LendingCard.tsx               # Lending item card
│   ├── CategoryChips.tsx             # Horizontal scrolling category filter
│   ├── MapMarker.tsx                 # Custom map marker component
│   └── CameraView.tsx               # Camera capture component
│
├── services/
│   ├── firebase.ts                   # Firebase init + config
│   ├── gemini.ts                     # Gemini API wrapper (image scan + text scan)
│   └── maps.ts                       # Google Maps helpers (nearby search, geocoding)
│
├── db/
│   └── schema.sql                    # SQLite table definitions
│
├── hooks/
│   ├── useSQLite.ts                  # SQLite CRUD hook (scan cache, history, drafts)
│   └── useLocation.ts                # GPS location hook
│
├── store/
│   └── useAppStore.ts                # Zustand global state (auth, theme, scan data)
│
├── types/
│   └── index.ts                      # TypeScript types & interfaces
│
├── assets/                           # App icon, splash, images
├── .env                              # API keys (gitignored)
├── .gitignore
├── README.md
└── plan.md                           # This file
```

### Navigation Flow Diagram

```
App Launch
    │
    ├── Not authenticated → auth/login.tsx
    │                           │
    │                           ├── Login → (tabs)/index.tsx (Home)
    │                           └── Register → auth/register.tsx → (tabs)/index.tsx
    │
    └── Authenticated → (tabs)/
            │
            ├── 🏠 Home (index.tsx)
            │     ├── Tap "Scan" CTA → (tabs)/scan.tsx
            │     └── Tap activity item → market/[id].tsx or share/[id].tsx
            │
            ├── ♻️ Market (market.tsx)
            │     ├── Tap listing → market/[id].tsx
            │     │                    └── Tap "Chat" → chat/[chatId].tsx
            │     ├── Tap 🗺 icon → market/map.tsx
            │     └── Tap ➕ FAB → market/post.tsx
            │
            ├── 📷 Scan (scan.tsx)
            │     ├── Camera capture → scan-result.tsx
            │     │                       ├── [♻️ Sell] → market/post.tsx (pre-filled)
            │     │                       ├── [🎁 Donate] → market/post.tsx (price=0)
            │     │                       ├── [🤝 Lend] → share/post.tsx (pre-filled)
            │     │                       ├── [🗺 Drop-off] → dropoff.tsx
            │     │                       └── [📋 Save] → SQLite scan_history
            │     └── Text search → scan-result.tsx (same flow)
            │
            ├── 🤝 Share (share.tsx)
            │     ├── Tap item → share/[id].tsx
            │     │                  └── Tap "Chat" → chat/[chatId].tsx
            │     ├── Tap 🗺 icon → share/map.tsx
            │     └── Tap ➕ FAB → share/post.tsx
            │
            └── 👤 Profile (profile.tsx)
                  ├── My Listings → market.tsx (filtered)
                  ├── My Lent Items → share.tsx (filtered)
                  ├── Scan History → list of past scans
                  └── Settings → theme toggle, notifications
```

---

## 🎨 UI Design Direction

### Design Philosophy: Glassmorphism + iOS Aesthetic

| Principle | Implementation |
|-----------|---------------|
| **Glassmorphism** | Frosted glass cards with `blur(20px)`, semi-transparent backgrounds, subtle light borders |
| **iOS-like** | Large titles, bottom tab bar, rounded corners (16-20px), system-native feel |
| **Clean & Spacious** | Generous padding (24-32px), breathing room, max 2-3 elements per section |
| **Icons > Words** | Ionicons for navigation and actions; minimal text labels |
| **Themed Colors** | All colours derived from the green theme; consistent throughout |
| **Micro-animations** | Smooth transitions (300ms), haptic feedback, parallax scroll |

### Color Palette — EventLoop (Nature Green) 🟢

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

### Screen Layout (Tab Structure)

```
Tab Bar (5 tabs):
  🏠 Home       — Dashboard, eco-score, quick scan, activity
  ♻️ Market     — Material marketplace (list + map toggle)
  📷 Scan       — AI scanner (center tab, larger icon)
  🤝 Share      — Equipment lending (list + map toggle)
  👤 Profile    — User profile, listings, history, settings
```

---

## 👥 Team Role Distribution (4 Members)

### Role Assignments

| Role | Member | Primary Ownership | Secondary |
|------|--------|-------------------|-----------|
| **Team Lead / Full-Stack** | Member A | App architecture, navigation, auth, maps integration | Project management, Firebase setup |
| **Frontend / UI Dev** | Member B | All UI screens, glassmorphism components, animations, launcher icon | Wireframes for proposal |
| **AI / Core Logic Dev** | Member C | AI scanner (Gemini API), camera, scan result, auto-fill flow | Data models, search |
| **Backend / Marketplace Dev** | Member D | Firebase CRUD, chat system, marketplace & lending backend, QA | Huawei AppGallery publishing |

### Development Task Ownership

| Screen / Feature | Developer | Depends On |
|-----------------|-----------|------------|
| **app/_layout.tsx** (Root providers) | Member A | — |
| **auth/login.tsx, register.tsx** | Member A | Firebase Auth |
| **(tabs)/_layout.tsx** (Tab bar) | Member A | Expo Router |
| **(tabs)/index.tsx** (Home) | Member B | Zustand store |
| **(tabs)/scan.tsx** (Camera + text input) | Member C | expo-camera |
| **scan-result.tsx** (AI result card) | Member C + B | Gemini API |
| **(tabs)/market.tsx** (Marketplace list) | Member D | Firestore |
| **market/[id].tsx** (Detail) | Member D | Firestore |
| **market/post.tsx** (Post listing) | Member D | Firebase Storage |
| **market/map.tsx** (Map view) | Member A | react-native-maps |
| **(tabs)/share.tsx** (Lending list) | Member D | Firestore |
| **share/[id].tsx** (Detail) | Member D | Firestore |
| **share/post.tsx** (Post item) | Member D | Firebase Storage |
| **share/map.tsx** (Map view) | Member A | react-native-maps |
| **chat/index.tsx, [chatId].tsx** | Member D | Firebase Realtime DB |
| **dropoff.tsx** (Drop-off map) | Member A | Google Places API |
| **(tabs)/profile.tsx** (Profile + settings) | Member A | Firestore user doc |
| **components/ui/*** (Glass library) | Member B | expo-blur |
| **components/CategoryChips.tsx** | Member B | — |
| **components/ListingCard.tsx** | Member B | — |
| **components/LendingCard.tsx** | Member B | — |
| **services/gemini.ts** | Member C | API key |
| **services/firebase.ts** | Member D | Firebase config |
| **services/maps.ts** | Member A | Maps API key |
| **db/schema.sql + hooks/useSQLite.ts** | Member C | expo-sqlite |
| **hooks/useLocation.ts** | Member A | expo-location |
| **store/useAppStore.ts** | Member A | Zustand |
| **types/index.ts** | Member C | — |
| **Custom Launcher Icon** | Member B | — |

### Report Writing Distribution

#### Part 1 — Proposal (4–10 pages, due Week 5)

| Section | Writer | Est. Pages |
|---------|--------|------------|
| Cover Page + Table of Contents | Member D | 1 |
| Introduction + Problem Statement + SDG 12 | Member A | 1.5 |
| Proposed Solution + 3 Pillars + Feature List + Use Cases | Member C | 2.5 |
| UI/UX Design — Wireframes + Mockups + User Flow | Member B | 3 |
| Technical Architecture + Tech Stack + AI Flow + Conclusion | Member D | 2 |
| **Review, proofread, format** | **All** | — |

#### Part 2 — Final Report (≤10 pages + Appendix, due Week 12)

| Section | Writer | Est. Pages |
|---------|--------|------------|
| Introduction + App Overview + System Architecture | Member A | 2 |
| UI Screenshots + Design Rationale | Member B | 2 |
| AI Scanner Deep-Dive + API Integration + Challenges | Member C | 2.5 |
| Marketplace & Lending + Testing + Deployment + Contribution Log | Member D | 2.5 |
| Unimplemented Features / Future Work | Member A | 1 |
| Appendix: Key Source Code Excerpts | All (own code) | As needed |
| **Review, proofread, format** | **All** | — |

### Presentation Speaking Roles (Week 13, 10 min)

| Speaker | Duration | Topic |
|---------|----------|-------|
| Member A | 2.5 min | Introduction, architecture overview, maps integration |
| Member B | 2.5 min | UI/UX walkthrough, glassmorphism demo, live app tour |
| Member C | 2.5 min | Live AI scanning demo (scan a banner, foam board, etc.) |
| Member D | 2.5 min | Marketplace demo, chat, lending flow, publishing |

---

## 📅 14-Week Schedule

### Phase 1: Planning & Proposal (Weeks 1–5)

---

#### Week 1 — Project Kickoff & Setup
| Task | Owner | Deliverable |
|------|-------|-------------|
| Read & understand assignment requirements | All | Shared understanding |
| Confirm app name (EventLoop) and niche (Event + Creative) | All | Decision locked |
| Create GitHub repository + invite all members | Member A | Repo URL |
| Register Huawei Developer account | Member D | Account created |
| Set up Expo project with TypeScript boilerplate | Member A | `npx create-expo-app` done |
| Get Google AI Studio API key (Gemini) | Member C | API key ready |
| Set up Firebase project (Auth + Firestore) | Member D | Firebase console ready |

---

#### Week 2 — Requirements & Design
| Task | Owner | Deliverable |
|------|-------|-------------|
| Define all user stories per module | All | User story list |
| Create low-fidelity wireframes (all screens) | Member B | Paper/Figma wireframes |
| Design data schema (Firestore + SQLite) | Member D | Schema document |
| Test Gemini Vision API with sample event material photos | Member C | Working API call proof |
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
| Peer review all sections | All | Feedback notes |
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
| Complete Firebase Auth (login/register/logout) | Member A | Auth flow complete |
| Build glassmorphism component library | Member B | GlassCard, GlassButton, GlassInput |
| Implement camera capture + gallery picker | Member C | Image capture working |
| Set up Firestore collections + CRUD helpers | Member D | Data layer ready |
| Implement SQLite local storage (scan cache + history) | Member C | Local DB ready |
| Build Home dashboard screen | Member B | Dashboard UI done |

---

#### Week 7 — AI Scanner Sprint
| Task | Owner | Deliverable |
|------|-------|-------------|
| Integrate Gemini Vision API — image scan | Member C | AI scanning working |
| Integrate Gemini Text API — text search | Member C | Text search working |
| Build scan result card UI (ScanResultCard.tsx) | Member B | Result screen polished |
| Build scan history screen | Member C | History screen done |
| Implement AI → auto-fill marketplace/lending post flow | Member C | Auto-fill working |
| Integrate Google Maps — drop-off points | Member A | Drop-off map working |

---

#### Week 8 — Marketplace Sprint
| Task | Owner | Deliverable |
|------|-------|-------------|
| Build marketplace browse/search screen | Member D | Listings screen done |
| Build marketplace post listing flow | Member D | Post flow working |
| Build marketplace listing detail screen | Member D | Detail screen done |
| Build CategoryChips component | Member B | Category filter working |
| Implement in-app chat (Firebase Realtime DB) | Member D | Chat working |
| Build marketplace map view | Member A | Map view done |

---

#### Week 9 — Lending Sprint + Integration
| Task | Owner | Deliverable |
|------|-------|-------------|
| Build lending browse/search screen | Member D | Lending screen done |
| Build lending post item flow | Member D | Post flow working |
| Build borrow request + approval flow | Member D | Request flow done |
| Build profile screen + eco-score | Member A | Profile done |
| Build settings screen (theme toggle) | Member A | Settings done |
| Design & create custom launcher icon | Member B | App icon ready |
| Polish all animations & transitions | Member B | Smooth UX |
| **FEATURE FREEZE** — no new features after this | All | Scope locked |

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
| Edge case testing (no network, empty states, errors) | Member D | Error states handled |
| Test both scan modes (image, text) with event materials | Member C | All modes verified |

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

---

### Phase 4: Presentation (Weeks 13–14)

---

#### Week 13 — ⚠️ Presentation (During Practical Session)
| Task | Owner | Deliverable |
|------|-------|-------------|
| Prepare slide deck (10 min presentation) | All | Slides ready |
| Rehearse demo flow on real device | All | Smooth demo rehearsed |
| Bring sample event materials for live scanning demo | Member C | Demo items ready |
| Prepare Q&A — each member studies their own code | All | Q&A ready |
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
| Custom launcher icon | Designed by Member B, green looping arrow with leaf motif | ⬜ |
| Store, update & retrieve data from device storage | expo-sqlite: scan_cache, scan_history, draft_posts tables | ⬜ |
| Connect to external endpoint (REST API / SDK) | Firebase (Firestore, Auth, Storage, Realtime DB) + Gemini API + Google Maps | ⬜ |

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
| Team member unavailability | Medium | High | Clear ownership; no single points of failure; weekly sync |
| Feature creep beyond Week 9 | High | Medium | Strict feature freeze; polish only after Week 9 |
| Huawei AppGallery approval delay | Medium | Low | Register Week 1; submit Week 11 for buffer |
| Chat system complexity | Medium | Medium | Keep it simple: text only, no images/voice in chat |
| Performance on low-end Android | Low | Medium | Compress images before upload; lazy load lists |
