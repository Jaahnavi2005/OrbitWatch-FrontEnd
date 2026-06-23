# 🛰️ OrbitWatch — Frontend
### Mapping Earth's invisible threat, one orbit at a time.

> Built for **Student Hackpad 2026** | Space Debris Monitoring Dashboard

---

## 🌍 What is OrbitWatch?

OrbitWatch is a real-time space debris monitoring dashboard that visualizes thousands of tracked objects orbiting Earth. With over **27,000 debris objects** traveling at speeds up to 28,000 km/h, space is becoming increasingly dangerous for satellites, the ISS, and future missions.

This repository contains the **frontend** — the interactive 3D globe, dashboard UI, charts, and all client-side logic. It connects to the [OrbitWatch Backend](#) for live orbital data.

---

## ✨ Features

- 🌐 **Interactive 3D Globe** — Real Earth visualization powered by CesiumJS
- 🛰️ **Real-Time Positions** — SGP4 orbital propagation via `satellite.js`, updated every second
- 🔴 **Color-coded Risk Levels** — Red (High) / Yellow (Medium) / Green (Low)
- 🖱️ **Hover Tooltips & Click Details** — Instantly see object info on the globe
- 📊 **Debris Growth Chart** — Historical timeline of major debris-creating events
- 💥 **Close Approach Monitor** — Detects objects passing near each other
- 🌌 **Orbital Shell Breakdown** — LEO / MEO / GEO / HEO zone counts
- 🔍 **Search, Filter & Sort** — By name, NORAD ID, risk level, or altitude range
- 📥 **CSV Export** — Download the current debris dataset
- 🌗 **Dark / Light Theme Toggle**
- 🕐 **Live UTC Clock**
- 📱 **Responsive Design** — Works on desktop, tablet, and mobile

---

## 🚀 How to Run

### Prerequisites
- The [OrbitWatch Backend](#) running locally or deployed
- A modern browser (Chrome recommended)
- VS Code with Live Server extension (for local development)

### Steps
```bash
git clone https://github.com/Jaahnavi2005/orbitwatch-frontend.git
cd orbitwatch-frontend
```

Open `index.html` with **Live Server** in VS Code, or visit the deployed link.

> ⚠️ **Note:** If the backend isn't reachable, the app automatically falls back to 20 sample debris objects (with real orbital elements) so it never looks broken — positions are still computed live via SGP4.

---

## 🗂️ Project Structure

```
orbitwatch-frontend/
│
├── index.html    → Main page structure and layout
├── style.css     → Dark/light theme styling, responsive design
├── data.js       → Fetches TLE data, runs SGP4 propagation
├── globe.js      → 3D globe visualization and controls (CesiumJS)
├── app.js        → Main controller — table, filters, charts, UI logic
└── README.md     → You are here!
```

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML / CSS / JavaScript | Core frontend |
| CesiumJS | 3D interactive globe |
| satellite.js | SGP4 orbital propagation |
| Chart.js | Debris growth visualization |
| CelesTrak API | Real TLE orbital data (via backend) |

---

## 🔗 Related Repository

Backend (Node.js + Express API): **[OrbitWatch Backend](#)**

---

## 🌌 Why This Matters

**Kessler Syndrome** — A chain reaction where debris collisions create more debris, potentially making low Earth orbit unusable for generations.

Even a **1cm piece of debris** traveling at 28,000 km/h can destroy a functioning satellite worth hundreds of millions of dollars. OrbitWatch exists to make this invisible crisis visible.

---

## 👩‍💻 Built By

**Jaahnavi** — Student Developer
Built with ❤️ for Space Hackpad 2026
