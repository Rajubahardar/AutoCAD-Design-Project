# Industrial Power Distribution and Illumination — AutoCAD Design Project

A complete electrical power distribution and illumination design for a multi-storey academic building (Thapathali Campus extension), developed as part of the *Services II* course at the Institute of Engineering, Pulchowk Campus, Tribhuvan University.

![AutoCAD](https://img.shields.io/badge/AutoCAD-Electrical%20Design-red)
![Status](https://img.shields.io/badge/status-completed-brightgreen)
![License](https://img.shields.io/badge/license-Academic--Use-blue)

## 📋 Project Overview

This project delivers a full end-to-end electrical distribution design for a 4-storey commercial/academic building (Basement, Ground, First, and Second Floor), covering everything from lux-level lighting calculations to transformer sizing. The design follows IS/IEC standards and was carried out using **AutoCAD Electrical** for layout and single-line diagram (SLD) development.

**Institution:** Institute of Engineering, Pulchowk Campus
**Course:** Services II (Industrial Power Distribution and Illumination)
**Supervisor:** Asst. Prof. Akhileshwar Mishra, Department of Electrical Engineering
**Submission Date:** 2082-12-18 (BS)

## 👥 Team

| Name | Roll No. | Floor Responsibility |
|---|---|---|
| Raju Bahardar | 079BEL066 | First Floor |
| Sanjaya Limbu | 078BEL081 | Basement Floor |
| Sumit Karki | 078BEL089 | Ground Floor |
| Yashitosh Kumar Yadav | 078BEL094 | Second Floor |

## 🏗️ Scope of Work

- **Lighting Design** — Lux-level calculations per room using the lumen method (`N = E×A / Φ×μu×μm`), fixture selection, and placement across all floors
- **Power Layout** — Socket outlet placement and circuiting for classrooms, offices, and common areas
- **Sub Distribution Boards (SDBs)** — Load scheduling, demand factor application, MCB rating selection, and cable sizing for every SDB on all 4 floors (14 SDBs total)
- **Floor Distribution Boards (FDBs)** — Aggregated floor-level load calculations and MCCB selection
- **Main Distribution Board (MDB)** — Building-wide load consolidation with simultaneity factor (Ks) applied
- **Cable Sizing** — Voltage-drop based conductor sizing (IEC formula: `A ≥ 1.732×K×I×L / Vdrop`) for all MDB–FDB–SDB runs
- **Transformer Sizing** — Demand-based KVA calculation with 20% future-load margin → **400 KVA transformer selected**
- **Main MCCB Selection** — 600A TPN MCCB sized from total secondary-side full load current

## 📊 Key Results

| Parameter | Value |
|---|---|
| Total Connected Load | 679.45 KW |
| Total Maximum Demand | 418.55 KW |
| Demand after Simultaneity Factor (Ks = 0.8) | 334.84 KW |
| Selected Transformer | 400 KVA |
| Main Incomer Breaker | 800A TP VCB |
| Main Bus Bar Rating | 1000A TPN |

## 📁 Repository Structure

```
├── drawings/
│   ├── power-layout.dwg          # Floor-wise power socket & SDB layout
│   ├── lighting-layout.dwg       # Floor-wise luminaire layout & circuiting
│   └── single-line-diagram.dwg   # Full SLD: Transformer → MDB → FDB → SDB → circuits
├── report/
│   └── Industrial_Power_Distribution_and_Illumination_Report.pdf
├── calculations/
│   ├── lux-calculation-tables.xlsx
│   ├── SDB-DB-box-calculations.xlsx
│   ├── cable-sizing-calculations.xlsx
│   └── transformer-MCCB-selection.xlsx
└── README.md
```

## 🛠️ Tools & Standards Used

- **AutoCAD Electrical** — layout drafting and SLD development
- **MS Excel** — load scheduling, demand factor, and cable-sizing computations
- Reference standards: **IEC 60947-2**, **IEC 60898-1:2019**, **IEEE Red Book (1993)**, **NFPA 70 (NEC 2020)**

## 📐 Design Assumptions

- Utilization factor (μu) and maintenance factor (μm) applied per room type per lumen-method standards
- Simultaneity factor: **Ks = 1** for lighting, **Ks = 0.6–0.5** for power sockets, **Ks = 0.7–0.8** at MDB/floor level (assuming general-hours campus occupancy)
- 15% cable-length margin added to all calculated runs for practical routing
- 20% headroom included in transformer sizing for future load expansion

## 📄 License

Shared for academic and portfolio purposes. Please credit the team above if referencing or reusing this work.
