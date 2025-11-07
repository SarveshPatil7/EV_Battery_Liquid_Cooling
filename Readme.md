# Single-Phase Immersion Cooling System for EV Batteries

### ME 598: Electronics Cooling — University of Illinois Urbana-Champaign  
**Team:** Sarvesh Patil, Parth Patil, Bharathwaj Ramanathan, Richard Menendez, Shreyan Shastri, Shourya Sahdev  
**Instructor:** Prof. Winston Zhang  
**Semester:** Spring 2024  

---

## Overview
This project investigates **single-phase immersion cooling** as a next-generation thermal management solution for electric vehicle (EV) batteries.  
Using **ANSYS Icepak**, we simulate and compare **air cooling**, **cold-plate liquid cooling**, and **immersion cooling** under varying discharge rates and flow conditions for a 3×3 21700 Li-ion cell module inspired by **Lucid Motors** pack design.  
Special attention is given to **hot spots**, which are a common issue in cold-plate designs. These localized thermal gradients accelerate **cell degradation** and can potentially lead to **thermal runaway**, posing serious safety hazards. 
Immersion cooling effectively minimizes temperature non-uniformities, making it the most robust and fire-safe cooling approach among those evaluated.

---

## Key Contributions
- Modeled **volumetric battery heat generation** for discharge rates (0.5C – 3C) as specifiec by a Lucid report.  
- Designed custom **cold plate** and **immersion enclosures** in *SolidWorks* and imported into *ANSYS Icepak*.  
- Conducted **90 CFD simulations** for six dielectric fluids under both forced-flow and static immersion conditions.  
- Performed **mesh independence** and **pressure–temperature performance** studies.  
- Evaluated coolant options (EG 50/50, Novec, Silicone Oil, Toluene, Mineral Oil) including **environmental factors** (GWP, toxicity, flammability).

---

## Simulation Setup

| Parameter | Range / Value |
|------------|----------------|
| Discharge rate | 0.5C – 3C |
| Flow rate | 2 LPM, 4 LPM, 6 LPM |
| Solver | ANSYS Icepak (steady-state) |
| Turbulence model | Enhanced Realizable k–ε |
| Geometry | 9-cell 21700 honeycomb array |
| Coolants | EG 50/50, Novec 7200, Silicone 100, Mineral Oil, Toluene, etc. |

---

## Results Summary

| Cooling Method | ΔT (°C) | Pressure Drop (N/m²) | Remarks |
|----------------|----------|----------------------|----------|
| **Air Cooling** | 80 – 265 | – | Inefficient; severe overheating |
| **Cold Plate** | 23 – 60 | 2,200 – 4,200 | Adequate cooling; high ΔP |
| **Static Immersion** | 76 – 528 | – | Overheating at high discharge |
| **Flow Immersion** | **26 – 40** | **3 – 10** | **46 % temperature reduction; ≈ 400× lower ΔP** |

> Flow immersion cooling maintained battery temperatures between **27 °C – 45 °C** across all discharge rates, outperforming both air and cold-plate systems while drastically reducing pumping losses.

---

## Environmental Evaluation
| Coolant | Thermal Performance | Environmental Safety | Notes |
|----------|--------------------|----------------------|-------|
| EG 50/50 | ★★★★★ | ★★☆☆☆ | Best thermal performer |
| Novec 7200 | ★★★★☆ | ★★★★★ | Low GWP, non-toxic |
| Silicone 100 | ★★★★☆ | ★★★★★ | Stable, safe, higher viscosity |
| Toluene | ★★★★☆ | ★☆☆☆☆ | Flammable |
| Mineral Oil | ★★★☆☆ | ★★★★☆ | Cost-effective alternative |

---

## Tools Used
- **ANSYS Icepak** — CFD thermal simulation  
- **SolidWorks** — cell geometry & cold-plate design   


