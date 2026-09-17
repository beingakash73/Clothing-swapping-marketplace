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

- **Frontend**: React 19, TypeScript, Tailwind CSS, Lucide React, Canvas Confetti, Vite 8
- **Backend**: Java 17+, Spring Boot 3 (`marketplace-backend`), Spring Data MongoDB
- **Database**: MongoDB Atlas
- **APIs**: RESTful endpoints on port `5000` with CORS & Vite reverse proxy support

---

## 📁 Repository Structure

```text
Clothing-swapping-marketplace/
├── frontend/                     # Vite + React TypeScript Frontend
│   ├── src/
│   │   ├── components/           # Reusable UI & feature components
│   │   ├── context/              # Global application state (AppContext)
│   │   ├── pages/                # Application view pages
│   │   ├── services/             # API client (connects to Spring Boot backend)
│   │   ├── types/                # TypeScript interfaces & domain models
│   │   └── utils/                # Valuation calculator, impact metrics, formatters
│   ├── package.json
│   └── vite.config.ts
│
├── backend/                      # Spring Boot REST API
│   ├── src/main/java/com/threadloop/marketplace/
│   │   ├── controller/           # REST Controllers (/api/items, /api/swaps, etc.)
│   │   ├── model/                # MongoDB Document Entities
│   │   ├── repository/           # Spring Data Repositories
│   │   ├── service/              # Business logic & Data seeder
│   │   └── util/                 # Eco & Fairness Calculators
│   ├── pom.xml                   # Maven dependencies
│   └── mvnw / mvnw.cmd
│
└── README.md
```

---

## 🚀 Getting Started

### 1. Run Backend (Spring Boot)

Navigate to the `backend` directory:
```bash
cd backend
./mvnw spring-boot:run
```
*(On Windows cmd/powershell, run `.\mvnw.cmd spring-boot:run`)*

The backend will start at `http://localhost:5000` and automatically seed initial items, users, swap proposals, and meetup hubs if the database is fresh.

### 2. Run Frontend (React + Vite)

In a separate terminal, navigate to the `frontend` directory:
```bash
cd frontend
npm install
npm run dev
```

The frontend will run at `http://localhost:5173`. Vite proxies `/api` requests directly to `http://localhost:5000`.

---

## 📜 Available Scripts

### Frontend (`frontend/`)
| Command | Description |
| :--- | :--- |
| `npm run dev` | Starts Vite client dev server at `http://localhost:5173` |
| `npm run build` | Compiles TypeScript and builds production client bundle |
| `npm run lint` | Runs fast code quality inspection with Oxlint |
| `npm run preview` | Previews production build locally |

### Backend (`backend/`)
| Command | Description |
| :--- | :--- |
| `./mvnw spring-boot:run` | Runs the Spring Boot backend application |
| `./mvnw clean test` | Runs the JUnit integration and unit tests |
| `./mvnw clean package` | Packages the application into an executable JAR |
