# 🩸 HemoScan AI — Non-Invasive Hemoglobin Monitor

> **Painless. Needle-free. Real-time hemoglobin detection for everyone.**

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Startup TN](https://img.shields.io/badge/Startup%20TN-Recognized-blue)](https://startuptn.in)
[![Udyam](https://img.shields.io/badge/Udyam-Certified-orange)](https://udyamregistration.gov.in)
[![IJERT](https://img.shields.io/badge/IJERT-Published-red)](https://ijert.org)
[![Hackathon](https://img.shields.io/badge/Bharat%20Academix-CodeQuest%202026-purple)](https://unstop.com)

---

## 🏆 Bharat Academix CodeQuest 2026 — Round 2 Submission

**Team:** Medicore Innovation  
**Members:** Mahambihai T (Founder & Tech Lead) · Sujay B (CEO) · Xavier Jerfin (CXO)  
**Institution:** St. Michael College of Engineering & Technology, Kalayarkoil, Sivagangai  

---

## 🎯 Problem We're Solving

India has **500 million+ anemia patients** — yet most cannot afford frequent hemoglobin monitoring:

- 💉 **Invasive** — Current CBC tests require needle pricks every visit
- 💸 **Expensive** — Lab tests cost ₹200–₹500 per visit
- 🏥 **Inaccessible** — 80% of rural patients go undiagnosed
- ⏳ **Slow** — Lab results take 2–3 days

**HemoScan AI solves all of this in under 30 seconds, for ₹2 per test, with zero needles.**

---

## 💡 Our Solution

Multi-wavelength LED Photoplethysmography (PPG) + Beer-Lambert Law + AI signal processing to measure hemoglobin non-invasively through the fingertip.

```
Finger on sensor → 4 LEDs fire → Photodiode captures absorption → 
ESP32 runs Beer-Lambert algorithm → Hb result in <30 seconds
```

| Metric | Value |
|--------|-------|
| Cost per test | ₹2 (vs ₹300 lab test) |
| Result time | < 30 seconds |
| Needles required | 0 |
| Target accuracy | ±0.5 g/dL (post clinical validation) |

---

## 📁 Repository Structure

```
HemoScan-AI-Medicore/
│
├── hemoscan_complete.html        # 🎯 Main MVP — Camera scan + Dashboard
├── hemoscan_simulation.html      # 🔬 ESP32 firmware logic browser demo  
├── hemoscan_sketch.ino.txt       # ⚙️ Arduino firmware for ESP32 + MAX30102
├── README.md                     # 📖 This file
└── LICENSE                       # MIT License
```

---

## 🚀 Live Demo

**Camera-based PPG Scanner (MVP):**  
👉 [https://codepen.io/Mahambihai/full/xbggrPa](https://codepen.io/Mahambihai/full/xbggrPa)

> Open on mobile → Allow camera → Place finger on rear camera + flash → Get Hb result in 15 seconds

---

## ⚙️ Technology Stack

### Hardware (Phase 2)
- ESP32-S3 Microcontroller
- MAX30102 PPG Sensor
- 4-Wavelength LED Array (660nm, 880nm, 520nm, 940nm)
- OLED Display SSD1306
- Li-Po Battery + USB-C charging
- Custom PCB + Silicone ergonomic casing

### Software (MVP — Current)
- HTML5 + CSS3 + Vanilla JavaScript (no framework)
- WebRTC `getUserMedia` API for camera PPG
- Beer-Lambert Law signal processing algorithm
- HTML5 Canvas for real-time waveform visualization
- Browser `localStorage` for patient data persistence

### Algorithm
```
R = (AC_red / DC_red) / (AC_ir / DC_ir)
Hb (g/dL) = 22.0 - (6.5 × R)
```
*Coefficients are demo-calibrated. Clinical validation in Phase 3.*

---

## 📱 How to Use

### Camera MVP (hemoscan_complete.html)
1. Open [live demo](https://codepen.io/Mahambihai/full/xbggrPa) on mobile Chrome
2. Tap **"Open Camera & Start"** → Allow camera permission
3. Cover rear camera + flash with fingertip
4. Hold still for 15 seconds
5. Fill patient details → Save to dashboard
6. View trends and AI recommendations

### ESP32 Firmware (hemoscan_sketch.ino.txt)
1. Open in Arduino IDE (rename .txt → .ino)
2. Install ESP32 board support
3. Connect ESP32 + MAX30102 via I2C (SDA=21, SCL=22)
4. Upload and open Serial Monitor at 115200 baud
5. Place finger on sensor — scan starts automatically

### Browser Simulation (hemoscan_simulation.html)
1. Download and open in any browser
2. Click **"▶ Run Simulation"**
3. Watch ESP32 firmware logic execute with real Beer-Lambert calculation

---

## 📊 Hemoglobin Reference Ranges

| Level | Range | Status |
|-------|-------|--------|
| Normal | ≥ 13 g/dL | ✅ Healthy |
| Mild Anemia | 10–13 g/dL | ⚠️ Monitor |
| Severe Anemia | < 10 g/dL | 🚨 Consult doctor |

---

## 🗺️ Project Roadmap

| Phase | Timeline | Status | Deliverables |
|-------|----------|--------|--------------|
| Phase 1 | Complete | ✅ Done | Algorithm, firmware code, web MVP, IJERT paper, startup registration |
| Phase 2 | 3 months | ⏳ Next | Breadboard prototype, PCB, silicone casing, 4-LED array |
| Phase 3 | 6 months | 📋 Planned | Clinical validation, hospital testing, CDSCO submission |
| Phase 4 | 12 months | 🚀 Future | Market launch, rural distribution, mobile app, PHC contracts |

---

## 👥 Team — Medicore Innovation

| Name | Role | Contribution |
|------|------|-------------|
| **Mahambihai T** | Founder & Tech Lead | Hardware design, algorithm, web dashboard, camera PPG |
| **Sujay B** | Co-Founder & CEO | Business strategy, market research, partnerships |
| **Xavier Jerfin** | Co-Founder & CXO | Technical guidance, clinical domain, faculty mentorship |

---

## 🏢 About Medicore Innovation

- 🏢 **Udyam Registered** MSME Startup
- 🌟 **Startup TN Recognized** — Tamil Nadu Government
- 📄 **IJERT Published** Research Paper — Vol. 15 Issue 03
- 🎓 **SMCET, Kalayarkoil**, Sivagangai, Tamil Nadu

---

## ⚠️ Disclaimer

This is a **research prototype** for hackathon demonstration purposes. HemoScan AI is at TRL 4-5. Camera-based readings are demo-grade estimates and **must not be used for medical diagnosis**. Clinical-grade accuracy requires hospital validation and regulatory approval (CDSCO).

---

## 📄 License

MIT License — see [LICENSE](LICENSE) file for details.

---

*© 2026 Medicore Innovation. Built with ❤️ in Tamil Nadu, India.*
