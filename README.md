
# Burial Feasibility Grid – Slope & Depth Classification

This repository defines a slope/depth classification framework to assess submarine cable burial feasibility.  
The model assigns each 100 m grid cell in the Area of Interest (AOI) to a burial category, based on water depth and seabed slope, using a reproducible set of geoprocessing rules.

---

## Motivation

Submarine cables must be buried in the seabed when water depth is <1000 m, except where slope or geology prevents it.  
This model classifies areas according to:

- Whether burial is required (based on depth)
- Whether burial is possible (based on slope)

The resulting map supports engineering routing and trenching decisions during early-stage planning.

---

## Structure

### Notebooks

| Notebook                               | Description                             |
|----------------------------------------|-----------------------------------------|
| `01_generate_grid.ipynb`               | Generate the 100 m base grid            |
| `02_compute_slope_and_depth.ipynb`     | Extract slope and depth values per cell |
| `03_classify_burial_feasibility.ipynb` | Assign burial class index to each cell  |

---

## Classification Logic

The model uses the following rule-based classification:

| Class Index | Burial Feasibility      | Depth Range     | Slope Constraint |
|-------------|-------------------------|-----------------|------------------|
| 0           | Not required            | >1000 m         | —                |
| 1           | Easy burial             | ≤1000 m         | ≤3°              |
| 2           | Moderate constraint     | ≤1000 m         | 3–7°             |
| 3           | High constraint         | ≤1000 m         | 7–15°            |
| 4           | Very difficult          | ≤1000 m         | 15–25°           |
| 5           | Impractical             | ≤1000 m         | >25°             |

---

## Outputs

- `03_burial_feasibility_grid.gpkg`: grid with burial feasibility class
- Plots and validation layers (optional)

---

## Reproduce the Full Pipeline

1. Clone the repository  
2. Prepare input rasters (`slope.tif`, `bathymetry.tif`)  
3. Run notebooks `01` → `03` in order  
4. Final output will be written to `/processed_data/`

---

## Documentation

All notebooks include structured headers and inline comments.  
Classification thresholds and burial assumptions are based on industry best practices and ICPC recommendations.

---

## Collaboration and reuse

This repository is part of an open portfolio of spatial analytics for submarine cable planning.  
All notebooks and methods are designed to be reused and adapted.

If you're interested in using this framework for a different region,  
**we can help you adapt it to your own data, seabed conditions, and regulatory context.**

> Contact: [Alejandra L. Cameselle](https://www.linkedin.com/in/alejandra-cameselle)

---

## License

This work is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License](https://creativecommons.org/licenses/by-nc/4.0/).  
You are free to reuse, adapt, and build upon this work **for non-commercial purposes**, as long as you provide attribution.

For commercial use, please contact the author directly.

---

## Developed by

This repository was developed by **Alejandra L. Cameselle** under the personal brand  
**[GeoAI Works](https://github.com/geoai-works)** — a portfolio of geospatial analytics for marine infrastructure, data science, and spatial risk assessment.