# 🫀 CityPulse Enterprise: Real-Time Municipal Data Fusion Platform

*"Single-pane-of-glass operational visibility across city infrastructure, transit telemetry, and incident response."*

---

## 🌟 Overview

**CityPulse Enterprise** is a real-time data fusion, telemetry analytics, and multi-stream normalization platform engineered for smart-city operations centers.

Municipal data typically lives in disconnected silos—GTFS transit streams, weather alerts, 311 citizen incident logs, and utility power grid telemetry operate on different schedules and schemas. **CityPulse** ingests these heterogeneous streams, normalizes them into a unified data model (`CityPulseDataModel_v2.4`), detects cross-feed correlations, and presents a 10-second glanceable municipal health index alongside dynamic action mitigation playbooks and geospatial vector mapping.

---

## 🚀 Enterprise Features

1. **Google Maps JS API & Vector Geospatial Map**:
   - Native **Google Maps JavaScript API** integration with dark vector map styling (`darkMapStyle`), custom interactive markers, and InfoWindows.
   - Built-in graceful vector tile fallback if an external Google Maps API key is omitted.
2. **Multi-Stream Ingestion Engine**:
   - Normalizes 4 streams: **Weather API**, **GTFS Transit**, **Utility Grid**, and **311 Incident Log**.
3. **Cross-Domain Correlation Rules Engine**:
   - Identifies pattern clusters (e.g., Heavy Rain + Substation Outage + Underpass Flooding) with confidence percentage scores.
4. **10-Second Glanceable Command Center**:
   - Radial SVG health score dial, sector risk indicators, and operational situation brief.
5. **Mitigation Action Playbook**:
   - Recommends actionable emergency responses (*"Dispatch Municipal Drain Crew to Central Underpass"*, *"Reroute GTFS Bus Route 14"*).
6. **Voice Dispatcher Announcer (SpeechSynthesis API)**:
   - Audio dispatcher reading out live situation briefs hands-free.
7. **Real-Time Analytics & Time-Series Graphs**:
   - Powered by Chart.js for tracking citywide health index vs. critical risk sectors over sliding 15-minute windows.
8. **Historical Replay & Threshold Guardrails**:
   - Scrub backward through multi-day historical telemetry datasets to re-evaluate correlation triggers.
9. **JSON Telemetry Log Exporter**:
   - One-click incident log report export for municipal engineering teams.

---

## 📂 Codebase Structure

```
citypulse-dashboard/
├── index.html     # Main application UI with Google Maps JS API script tag & Tailwind CSS
├── styles.css     # Production glassmorphic design system, glow effects, and map styling
├── app.js         # Core Engine: Data normalizer, Google Maps API engine, correlation logic, chart engine
└── README.md      # Platform documentation & setup guide
```

---

## 💻 How to Run

1. Open `index.html` directly in any modern browser:
   `C:\Users\BHARTI\.gemini\antigravity\scratch\citypulse-dashboard\index.html`
2. *(Optional)* Replace `YOUR_API_KEY` in `index.html` with your Google Maps JavaScript API key:
   ```html
   <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_ACTUAL_GOOGLE_MAPS_API_KEY&callback=initMapEngine" async defer></script>
   ```
3. Or serve locally via any HTTP server:
   ```bash
   npx serve .
   ```
