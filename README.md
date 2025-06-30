# 📌 Cable Burial Operability

**Geospatial assessment of burial feasibility for submarine cable routes based on seafloor morphology and technical constraints.**

> Developed by [Alejandra L. Cameselle](https://www.linkedin.com/in/alejandralcameselle/)  
> Under the brand [GeoAI Works](https://www.linkedin.com/company/geoai-works/) – Geospatial AI solutions for marine, earth and infrastructure challenges.

---

## 🗂️ Repository structure

```
cable_burial_operability/
│
├── inputs/ ………………. Raw input files (AOI, bathymetry, cable route, etc.)
├── processed_data/ ……….. Intermediary and final geospatial files (grids, geopackages)
└── outputs/
│   ├── maps/ …………….. Final maps and geospatial exports
│   └── plots/ ……………. Plots (e.g., clustering, summary charts)
│   └── summary/ ………….. Summary files
│
├── notebooks/
│   ├── 01_generate_grid.ipynb
│   ├── 02_extract_depth_slope.ipynb
│   ├── 03_morphological_zoning.ipynb
│   ├── 04_cable_burial_operability.ipynb
│   ├── 05_operational_complexity.ipynb
│   └── 06_route_risk_assessment.ipynb
│
├── LICENSE
├── environment.yaml
└── README.md
```

---

## 📖 Description

This repository explores the feasibility of submarine cable burial based on seafloor depth and slope constraints. It provides an operational zoning of the study area and simulates route-specific risks for subsea infrastructure planning. All analyses are reproducible through geospatial notebooks and open data layers.

---

## 🔁 Collaboration and Reuse

The methods and tools in this repository are freely available for **non-commercial use** under the [CC BY-NC 4.0 License](https://creativecommons.org/licenses/by-nc/4.0/).  
👉 **Interested in applying this framework to your own region or project?**  
We are open to technical collaborations and consulting — [contact us](https://www.linkedin.com/company/geoai-works/) to discuss how GeoAI Works can support your initiative.

---

## 📜 License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)**.  
Commercial use or redistribution requires explicit permission. See the LICENSE file for details.
