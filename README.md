# Schools Air Quality Observatory 🌍

A custom **ArcGIS Experience Builder** widget that shows **real‑time air quality** for schools in **Greece** and **Cyprus**, using the European Air Quality Index (EAQI).

> **🔗 Live app:** **https://schools-air-quality.netlify.app/**
>
> **🔗 ArcGIS Experience:** https://experience.arcgis.com/experience/dd77a1cc983b413188bb81022aa504ea

Built by **Alexandros Pantazis** as part of the **ADONIS TICKET** competition, organized in memory of the founder of **Marathon Data Systems**, Adonis Kontos — https://marathondata.gr/

---

## What it does

The app is a side‑panel widget bound to a Map widget. Schools are displayed as points on two feature layers (Greece & Cyprus) with **clustering** enabled.

- **🗺️ Tap a school** on the map → a docked panel opens with live air‑quality data for that exact location.
- **🔍 Tap a cluster** → the map smoothly **zooms into the area** the cluster covers, breaking it apart so you can pick an individual school.
- **📊 Live EAQI score** with a color‑coded level (Good → Extremely Poor) and a health‑advice tip tailored to the level.
- **🧪 Current pollutant concentrations:** PM2.5, PM10, NO₂, O₃ (μg/m³), plus a reference table of EAQI limits.
- **📈 5‑day history & 5‑day forecast** charts (daily maximum EAQI).
- **🖨️ Export to PDF**, **📋 copy report**, and **🔗 share** (native share / Facebook fallback).
- **🌐 Bilingual UI:** Greek 🇬🇷 / English 🇬🇧, switchable in‑app.
- **📱 Works on touch & desktop:** reliable one‑tap selection and cluster zoom on phones and tablets.

## How it works

1. **Select a school** on the map.
2. **View** the current air quality, pollutants, and the history/forecast charts.
3. **Export** the report to PDF or share it.

## Data sources

- **Air quality:** [Open‑Meteo Air Quality API](https://open-meteo.com/) — hourly EAQI, PM2.5, PM10, NO₂, O₃.
- **Underlying model:** the European [Copernicus Atmosphere Monitoring Service (CAMS)](https://atmosphere.copernicus.eu/air-quality).

> The **European Air Quality Index (EAQI)** gives a quick assessment of the air we breathe. It is computed hourly from a combination of measurements and forecast data from Copernicus (CAMS).

### EAQI scale

| Level | EAQI | Color |
|-------|------|-------|
| Good | 0–20 | 🟦 `#50F0E6` |
| Fair | 21–40 | 🟩 `#50CCAA` |
| Moderate | 41–60 | 🟨 `#F0E641` |
| Poor | 61–80 | 🟥 `#FF5050` |
| Very Poor | 81–100 | 🟪 `#960032` |
| Extremely Poor | >100 | 🟣 `#7D2181` |

## Tech stack

- **ArcGIS Experience Builder** 1.19
- **React + TypeScript**, on `jimu-core` / `jimu-arcgis`
- **ArcGIS Maps SDK for JavaScript** (`@arcgis/core`)

## Project structure

```
schools-aqi/
├── manifest.json              # Widget definition
├── src/
│   ├── config.ts              # Widget config interface
│   ├── runtime/
│   │   └── widget.tsx         # Main widget (UI + map interaction + data)
│   └── setting/
│       └── setting.tsx        # Builder settings panel
└── README.md
```

---

## Ελληνικά 🇬🇷

**Παρατηρητήριο Ποιότητας Αέρα Σχολείων** — ένα custom widget για το **ArcGIS Experience Builder** που δείχνει την **ποιότητα του αέρα σε πραγματικό χρόνο** για σχολεία στην **Ελλάδα** και την **Κύπρο**, με βάση τον Ευρωπαϊκό Δείκτη Ποιότητας Αέρα (EAQI).

**🔗 Εφαρμογή σε λειτουργία:** **https://schools-air-quality.netlify.app/**

### Τι κάνει

- **Πάτα ένα σχολείο** στον χάρτη → ανοίγει πλαϊνό panel με ζωντανά δεδομένα ποιότητας αέρα.
- **Πάτα ένα cluster** → ο χάρτης κάνει ομαλό **zoom στην περιοχή** και «ανοίγει» το cluster.
- **Δείκτης EAQI** με χρωματική κλίμακα και **συμβουλή υγείας** ανά επίπεδο.
- **Τρέχουσες συγκεντρώσεις ρύπων** (PM2.5, PM10, NO₂, O₃) και πίνακας ορίων.
- **Ιστορικό & πρόγνωση 5 ημερών** σε γραφήματα.
- **Εξαγωγή σε PDF**, **αντιγραφή** και **κοινοποίηση**.
- **Δίγλωσσο** περιβάλλον (Ελληνικά / Αγγλικά).

### Πηγές δεδομένων

Τα δεδομένα αντλούνται σε πραγματικό χρόνο από το δίκτυο **Open‑Meteo** και τα μοντελοποιημένα δεδομένα του Ευρωπαϊκού Προγράμματος **Copernicus (CAMS)**.

---

## Credits

Developed by **Alexandros Pantazis** for the **ADONIS TICKET** competition by [Marathon Data Systems](https://marathondata.gr/).
