# rplt
Research Plot Layout Tool for replicated agricultural trials. 



# Research Plot Layout Tool

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Leaflet](https://img.shields.io/badge/Powered%20by-Leaflet-blue)](https://leafletjs.com/)
[![Turf.js](https://img.shields.io/badge/Geometry-Turf.js-green)](https://turfjs.org/)

A **web-based interactive tool** for designing agricultural or ecological research plot layouts directly on satellite imagery. Perfect for field trial planning — define your origin, baseline, plot dimensions, treatments, replications, buffers, and generate GIS-ready files instantly.

---

## 🌟 Features

- **Interactive Map Interface** with Esri World Imagery (or custom tile layers)
- **Click-to-place** Origin and Baseline points
- Support for **metric** and **imperial** units
- Multiple **plot numbering schemes**: Row-major, Column-major, Snake
- Configurable **buffers** (left/right/front/back) and **replication gaps**
- Two **origin reference modes**:
  - Lower-left of first plot (101)
  - Lower-left of entire area (including buffers)
- **Real-time visualization** of:
  - Individual treatment plots
  - Total research area
  - Full buffered area
  - Plot centers & vertices
- **Export multiple formats**:
  - GeoJSON (plots, centers, vertices, total area)
  - KML (total research area)
  - CSV (centers, origin/baseline, vertices)
- **Download all files individually or as ZIP**

---

## 🚀 Live Demo

Try it now: [https://yourusername.github.io/research-plot-layout](https://yourusername.github.io/research-plot-layout) *(replace with your actual URL)*

---

## 📸 Screenshot

![Research Plot Layout Tool Screenshot](./screenshot.png)
> *Example layout with 6 treatments × 3 replications, buffers, and snake numbering*

---

## 🛠️ How to Use

1. **Load custom tiles** (optional) — e.g., drone orthomosaics or high-res imagery
2. **Set Origin & Baseline**:
   - Click **"Set Origin (click map)"** → click lower-left corner
   - Click **"Set Baseline (click map)"** → click a point to your right
3. Enter experiment parameters:
   - Units, treatments, replications
   - Plot width/length, spacing, buffers
4. Click **Generate Layout**
5. Download output files (GeoJSON, KML, CSV, ZIP)

> 💡 **Pro Tip**: Use the "Zoom to Location" panel to quickly navigate to your field.

---

## 📂 Output Files

| File | Description |
|------|-------------|
| `plots.geojson` | All treatment plots with IDs |
| `centers.geojson` / `centers.csv` | Plot center coordinates |
| `vertices.geojson` | Corner points of each plot |
| `total_research_area.kml` | Boundary of all plots (no buffers) |
| `total_area.geojson` | Full area including buffers |
| `origin_baseline.csv` | Origin and baseline coordinates |
| `total_area_vertices.csv` | Corners of the total buffered area |

---

## 🗺️ Custom Tile Layers

Want to use your own imagery (e.g., drone mosaic)?

1. Upload tiles to a server in `{z}/{x}/{y}.png` format
2. Use a URL template like:
