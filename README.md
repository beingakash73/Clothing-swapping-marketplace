# 🔄 ThreadLoop — Sustainable Clothing Exchange & Direct Swapping Marketplace

ThreadLoop is a circular fashion marketplace designed for 1-to-1 and multi-item direct garment exchanges without monetary transactions. It features an automated Fair Swap Value calculator, geolocation proximity matching, escrow-like double confirmation flows, in-app negotiation chat, and environmental impact metrics.

---

## 🌟 Key Features

- **Direct Garment Swapping**: Propose and negotiate 1-to-1 or multi-item garment trades.
- **Fair Swap Calculator**: Computes equivalent trading value based on brand tier, age, condition, and original retail price with fairness scoring.
- **Location & Proximity Radar**: Filter nearby items and coordinate safe local meetups at verified public hubs or courier shipping.
- **Real-Time Negotiation Chat**: In-app messaging with interactive offer adjustment, counter-offers, and status cards.
- **Eco-Impact Dashboard**: Tracks real-time liters of water saved, kilograms of CO₂ avoided, and waste diverted from landfills.
- **Dispute Resolution & Admin Center**: Comprehensive moderation tools for dispute management, swap monitoring, and user trust score management.

---

## 🛠️ Tech Stack

- **Frontend**: React 19, TypeScript, Tailwind CSS, Lucide React, Canvas Confetti
- **Build Tool**: Vite 8
- **Backend API**: Spring Boot (`marketplace-backend`) on port `5000`
- **Database**: MongoDB Atlas
- **Code Quality**: Oxlint, TypeScript Compiler (`tsc`)

---

## 🚀 Quick Start

### 1. Install Dependencies
```bash
npm install
```

### 2. Start Backend & Frontend
1. Ensure your Spring Boot backend (`marketplace-backend`) is running on `http://localhost:5000` connected to MongoDB.
2. Run the Vite frontend development server:
```bash
npm run dev
```
The frontend will launch at `http://localhost:5173` and proxy `/api` requests to `http://localhost:5000`.

---

## 📁 Project Structure

```text
├── src/
│   ├── components/          # Reusable UI & feature components
│   ├── context/             # Global application state (AppContext)
│   ├── data/                # Initial seeds and PRD specification
│   ├── pages/               # Application view pages
│   ├── services/            # API client service layer (connects to Spring Boot backend)
│   ├── types/               # TypeScript interfaces & domain models
│   └── utils/               # Valuation calculator, impact metrics, formatters
├── public/                  # Static assets
└── index.html               # Main HTML entry point
```

---

## 📜 Available Scripts

| Command | Description |
| :--- | :--- |
| `npm run dev` | Starts Vite client dev server at `http://localhost:5173` |
| `npm run build` | Compiles TypeScript and builds production client bundle |
| `npm run lint` | Runs fast code quality inspection with Oxlint |
| `npm run preview` | Previews production build locally |

