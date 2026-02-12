<div align="center">

# ☢ Geigerduino — Radiation Monitor

**Real-time environmental radiation monitoring from Lancashire, United Kingdom**

[![Live Dashboard](https://img.shields.io/badge/LIVE%20DASHBOARD-View%20Now-FFD700?style=for-the-badge&logoColor=black)](https://benb0jangles.github.io/Geigerduino/)
[![Hardware](https://img.shields.io/badge/Hardware-ESP32--C3%20%2B%20SBM--20-orange?style=for-the-badge)](#hardware)
[![Location](https://img.shields.io/badge/📍-Lancashire%2C%20UK-blue?style=for-the-badge)](#)
[![Update Rate](https://img.shields.io/badge/Updates-Every%2030s-green?style=for-the-badge)](#)

</div>

---

## 🌐 Live Data Feed

> **[benb0jangles.github.io/Geigerduino](https://benb0jangles.github.io/Geigerduino/)**

The dashboard displays real-time CPM and µSv/h readings with interactive time-range charts, a moving average trend line, period min/max, and a colour-coded dose scale — all auto-refreshing every 30 seconds.

---

## 📊 Dashboard Features

| Card | Description |
|------|-------------|
| ⚡ **Count Rate** | Live Counts Per Minute (CPM) from the Geiger tube |
| ☢ **Dose Rate** | Converted µSv/h using the SBM-20 factor of 0.0057 |
| 🟢 **Radiation Level** | Status: Normal / Slightly Elevated / Elevated / High / Danger |
| 📊 **Data Points** | Number of readings in the selected time window |
| 📈 **Period Average** | Mean µSv/h for the active range (1hr / 24hr / 7 Day / 30 Day) |
| ↕ **Period Range** | Low ▼ and High ▲ µSv/h — High coloured to match the dose scale |

**Charts** show raw readings plus a smoothed moving average trend line. The µSv/h chart includes a green threshold line at **0.30 µSv/h** marking the normal background ceiling.

---

## ☢ Radiation Dose Reference Scale

| Level | Range | Significance |
|-------|-------|--------------|
| 🟢 **Normal** | < 0.30 µSv/h | Natural background. Global average 0.08–0.30 µSv/h |
| 🟡 **Slightly Elevated** | 0.30 – 1.0 µSv/h | Above typical background; not concerning for short exposure |
| 🟠 **Elevated** | 1.0 – 5.0 µSv/h | Warrants investigation of source |
| 🔴 **High** | 5.0 – 20.0 µSv/h | Significantly above background; may require reporting if persistent |
| ⛔ **Danger** | > 20.0 µSv/h | Restricted zone level; significant health risk with prolonged exposure |

### Context & Health Reference

| Dose / Limit | Value |
|---|---|
| Annual public limit | 1 mSv/year ≈ 0.11 µSv/h continuous |
| Nuclear industry worker limit | 20 mSv/year |
| Chest X-ray | ~20–100 µSv total |
| CT scan | ~10,000–20,000 µSv total |
| Acute radiation sickness threshold | ~500,000 µSv received in a short period |

> **Typical reading:** 0.05–0.20 µSv/h is normal. Readings consistently above **1.0 µSv/h** without a known source (e.g. a mineral sample) are worth investigating.

---

## 🔧 Hardware

```
MCU   : ESP32-C3 Super Mini
Tube  : SBM-20 Geiger-Müller Tube
Factor: 0.0057 µSv/h per CPM
IoT   : ioT Server (field1 = CPM, field2 = µSv/h)
Power : USB-C
```

The ESP32-C3 reads pulses from the SBM-20 tube, calculates CPM and µSv/h, then pushes readings to the IoT server every 30 seconds over Wi-Fi.

---

<div align="center">

*Natural background radiation (global average) ≈ 0.10–0.30 µSv/h*

☢ **Geigerduino** · ESP32-C3 + SBM-20 · Lancashire, UK · 2025

</div>
