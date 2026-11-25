# Industrial Power Distribution and Illumination — AutoCAD Design Project

[![AutoCAD Electrical](https://img.shields.io/badge/AutoCAD-Electrical%20Design-B71C1C?logo=autodesk&logoColor=white)](#repository-structure)
[![Building Scope](https://img.shields.io/badge/Scope-4--Storey%20Academic%20Building-0b2545)](#project-overview)
[![Transformer Rating](https://img.shields.io/badge/Transformer-400%20kVA%20%7C%20800A%20VCB-2E7D32)](#key-engineering-results)
[![Technical Report](https://img.shields.io/badge/Report-Full%20Design%20Report%20(PDF)-1d4e89)](report/Industrial_Power_Distribution_and_Illumination_Report.pdf)
[![License](https://img.shields.io/badge/License-Academic--Use-6A1B9A)](#license)

A complete end-to-end **electrical power distribution and illumination engineering design** for a four-storey academic building (**Thapathali Campus Extension**), developed for the *Services II* course at the **Institute of Engineering (IOE), Pulchowk Campus, Tribhuvan University**. Covering room-by-room lux calculations, socket circuiting, 14 Sub Distribution Boards (SDBs), Floor Distribution Boards (FDBs), Main Distribution Board (MDB) consolidation, IEC voltage-drop cable sizing, protective switchgear coordination, and **400 kVA transformer sizing**, the project is drafted in **AutoCAD Electrical** and verified through structured **MS Excel** engineering schedules.

> **Read Full Design Report:** Open **[`report/Industrial_Power_Distribution_and_Illumination_Report.pdf`](report/Industrial_Power_Distribution_and_Illumination_Report.pdf)** for complete room-wise illumination sheets, load schedules, cable voltage-drop checks, protective device coordination, and Single-Line Diagram (SLD) documentation.

---

## Project Overview

| Attribute | Details |
| :--- | :--- |
| **Facility Type** | 4-Storey Academic & Commercial Building (*Basement, Ground, First, and Second Floors*) |
| **Institution** | Institute of Engineering (IOE), Pulchowk Campus, Tribhuvan University |
| **Course** | Services II — Industrial Power Distribution and Illumination |
| **Supervisor** | Asst. Prof. Akhileshwar Mishra, Department of Electrical Engineering |
| **Submission Date** | 2082-12-18 (BS) |
| **Design Tools & Codes** | AutoCAD Electrical, MS Excel · IEC 60947-2, IEC 60898-1:2019, IEEE Red Book (1993), NFPA 70 (NEC 2020) |

### Project Team & Floor Responsibilities

| Name | Roll No. | Assigned Floor | Scope Delivered |
| :--- | :---: | :--- | :--- |
| **Raju Bahardar** | `079BEL066` | First Floor | Lux layout, socket circuiting, SDB/FDB schedules & cable sizing |
| **Sanjaya Limbu** | `078BEL081` | Basement Floor | Lux layout, socket circuiting, SDB/FDB schedules & cable sizing |
| **Sumit Karki** | `078BEL089` | Ground Floor | Lux layout, socket circuiting, SDB/FDB schedules & cable sizing |
| **Yashitosh Kumar Yadav** | `078BEL094` | Second Floor | Lux layout, socket circuiting, SDB/FDB schedules & cable sizing |

---

## Key Engineering Results

| Design Parameter | Calculated / Selected Value | Engineering Basis |
| :--- | :---: | :--- |
| **Total Connected Load** | **`679.45 kW`** | Sum of all lighting and power socket circuits across 4 floors |
| **Total Maximum Demand** | **`418.55 kW`** | After applying circuit-level and SDB/FDB demand factors |
| **Net Demand after Simultaneity ($K_s = 0.8$)** | **`334.84 kW`** | Building-wide MDB consolidation for general campus occupancy |
| **Selected Distribution Transformer** | **`400 kVA`** | Sized from net kVA demand with **20% future-load headroom** |
| **Main Incomer Breaker** | **`800 A TP VCB`** | Primary/incomer Vacuum Circuit Breaker protection |
| **Main Busbar Rating** | **`1000 A TPN`** | Main Distribution Board (MDB) copper busbar capacity |
| **Main Secondary MCCB** | **`600 A TPN MCCB`** | Sized from total secondary-side full-load current |
| **Distribution Hierarchy** | **`14 SDBs` $\to$ `FDBs` $\to$ `MDB`** | Complete floor-wise radial distribution network |

---

## Scope of Work & Design Formulations

### 1. Illumination Design (Lumen Method)
Room-by-room luminaire counts are calculated from target illuminance ($E$), room area ($A$), lamp luminous flux ($\Phi$), utilization factor ($\mu_u$), and maintenance factor ($\mu_m$):

$$N = \frac{E \times A}{\Phi \times \mu_u \times \mu_m}$$

### 2. Power Layout & Distribution Hierarchy (`14 SDBs` $\to$ `FDBs` $\to$ `MDB`)
- **Power Circuiting:** Dedicated socket outlet placement and circuit grouping for classrooms, faculty offices, laboratories, and common corridors.
- **Sub Distribution Boards (14 SDBs):** Load scheduling, demand factor application, MCB rating selection (`IEC 60898-1:2019`), and outgoing circuit sizing across all four floors.
- **Floor & Main Distribution Boards (FDBs & MDB):** Aggregated floor-level MCCB selection (`IEC 60947-2`) and building-wide MDB consolidation using simultaneity factor $K_s$.

### 3. Voltage-Drop Cable Sizing & Transformer Selection
All MDB–FDB–SDB feeder conductors are sized to satisfy allowable IEC voltage-drop limits with a **15% practical routing length margin**:

$$A \ge \frac{\sqrt{3} \times K \times I \times L}{V_{\text{drop}}}$$

Transformer capacity is selected from the diversified MDB demand with **20% expansion margin**, resulting in a **400 kVA** unit protected by an **800 A TP VCB** incomer, **1000 A TPN** busbar, and **600 A TPN** secondary MCCB.

---

## Design Assumptions & Standards

### Engineering Assumptions
- **Illumination Factors:** Room-specific utilization factor ($\mu_u$) and maintenance factor ($\mu_m$) applied per standard lumen-method tables.
- **Simultaneity Factors ($K_s$):** $K_s = 1.0$ for lighting loads, $K_s = 0.5\text{--}0.6$ for power socket circuits, and $K_s = 0.7\text{--}0.8$ at FDB/MDB level assuming general-hours academic occupancy.
- **Routing & Expansion Margins:** **15% cable-length margin** added to all measured run lengths; **20% kVA headroom** included in transformer sizing.

### Reference Codes & Standards
- **IEC 60947-2** — Low-voltage switchgear and controlgear (MCCB selection and breaking capacity)
- **IEC 60898-1:2019** — Circuit-breakers for overcurrent protection for household and similar installations (MCB sizing)
- **IEEE Std 141 (IEEE Red Book, 1993)** — Electric Power Distribution for Industrial Plants
- **NFPA 70 (NEC 2020)** — National Electrical Code conductor ampacity and feeder protection guidelines

---

## Repository Structure

```text
AutoCAD-Design-Project/
├── drawings/
│   ├── power-layout.dwg                                      # Floor-wise power socket & SDB layout
│   ├── lighting-layout.dwg                                   # Floor-wise luminaire layout & circuiting
│   └── single-line-diagram.dwg                               # Complete SLD: Transformer → MDB → FDB → SDB → circuits
├── report/
│   └── Industrial_Power_Distribution_and_Illumination_Report.pdf   # Full technical report & calculations
├── calculations/
│   ├── lux-calculation-tables.xlsx                           # Room-by-room lumen-method lighting schedules
│   ├── SDB-DB-box-calculations.xlsx                          # 14 SDB & FDB load schedules and breaker sizing
│   ├── cable-sizing-calculations.xlsx                        # IEC voltage-drop & ampacity feeder calculations
│   └── transformer-MCCB-selection.xlsx                       # MDB demand, 400 kVA transformer & MCCB/VCB sizing
└── README.md                                                 # Project summary, results & documentation
```

---

## Deliverables Quick Access

| Category | File | Contents |
| :--- | :--- | :--- |
| **Technical Report** | [`report/Industrial_Power_Distribution_and_Illumination_Report.pdf`](report/Industrial_Power_Distribution_and_Illumination_Report.pdf) | Complete methodology, calculations, schedules & SLD documentation |
| **AutoCAD Drawings** | `drawings/single-line-diagram.dwg`, `power-layout.dwg`, `lighting-layout.dwg` | Native AutoCAD Electrical `.dwg` layouts and full building SLD |
| **Excel Schedules** | `calculations/*.xlsx` | Interactive spreadsheets for lux, SDB/FDB, cable sizing & transformer/MCCB selection |

---

## Citation

```bibtex
@misc{bahardar2026autocaddistribution,
  author       = {Bahardar, Raju and Limbu, Sanjaya and Karki, Sumit and Yadav, Yashitosh Kumar},
  title        = {Industrial Power Distribution and Illumination — AutoCAD Design Project},
  year         = {2025},
  howpublished = {\url{[https://github.com/Rajubahardar/AutoCAD-Design-Project](https://github.com/Rajubahardar/AutoCAD-Design-Project)}},
  note         = {Services II Design Project, Department of Electrical Engineering, IOE Pulchowk Campus, Tribhuvan University}
}
```

---

## License

Shared for academic and portfolio purposes. Please credit the project team above when referencing or reusing these drawings, schedules, or calculations.
