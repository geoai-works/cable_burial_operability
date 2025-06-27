# Cable Burial Operability

**Assessment of burial feasibility for submarine cable routes based on seafloor morphology and technical constraints.**

This project evaluates the feasibility of submarine cable burial by analyzing key geospatial parameters: depth and slope. It classifies seabed regions into operational classes (e.g., critical, high, moderate, low) based on burial requirements and slope limits, which are essential for route engineers and decision-makers in the early planning stages.

---

## 📁 Repository structure

```
cable_burial_operability/
│
├── inputs/ ................... Raw input files (AOI, bathymetry, cable route, etc.)
├── processed_data/ ........... Intermediary and final geospatial files (grids, geopackages)
└── outputs/
│   ├── maps/ ................. Final maps and geospatial exports
│   └── plots/ ................ Plots (e.g., clustering, summary charts)
│   └── summary/ ................ summary files
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

## 📦 Installation

It is recommended to use a clean Conda environment. You can create one using the provided environment file:

```bash
conda env create -n cable_burial_env -f environment.yaml
conda activate cable_burial_env
```

---

## 🧭 Project overview

1. **Grid Generation**: Create a uniform grid covering the AOI.
2. **Depth & Slope Extraction**: Assign bathymetric metrics to each grid cell.
3. **Geomorphological Zoning**: Apply KMeans clustering to define seabed zones based on depth/slope.
4. **Operability Classification**: Identify areas where burial is feasible, required, or not possible.
5. **Operational Complexity**: Integrate burial needs and slope constraints into a unified risk score.
6. **Route Evaluation**: Overlay simulated cable routes to assess their operational risk segments.

---

## 🔖 License

This project is licensed under the [MIT License](LICENSE). You are free to use, adapt, and share the materials, provided that attribution is given.

---

## 🔗 Learn more

For updates, follow [GeoAI Works on LinkedIn](https://www.linkedin.com/company/geoai-works).
