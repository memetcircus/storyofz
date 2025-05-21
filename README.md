# 🛰️ OpenAI to Z — Checkpoint 1 Submission

This repository contains my official Checkpoint 1 submission for the [OpenAI to Z Challenge](https://openai.com/openai-to-z). The notebook demonstrates GPT-4.1 interpretation of Amazonian LiDAR and GEDI data to identify potential archaeological anomalies.

---

## ✅ Submission Summary

- **Org ID**: org-Vl41gaxgAP4nJ87yk3cBRWpJ
- **Checkpoint**: 1 — Familiarize and Prompt
- **Notebook**: [`checkpoint-2`](checkpoint-2.ipynb)
- **Status**: Public code execution complete & reproducible

---

## 🗂️ Datasets Used

### 1. **OpenTopography LiDAR (DTM)**
- **File**: `TAP_A04_15_DTM.tif`
- **Source**: ORNL DAAC / OpenTopography
- **Description**: 1m resolution Digital Terrain Model (bare-earth) for the Tapajós National Forest, Brazil

### 2. **NASA GEDI L2A Footprints**
- **File**: `GEDI02_A_2024282205519_O32987_04_T06355_02_004_02_V002.h5`
- **Source**: NASA Earthdata
- **Description**: Full waveform LiDAR data capturing vegetation and terrain structure

---

## 💬 GPT Prompt (Summary Mode)

> *You are analyzing a high-resolution LiDAR-derived Digital Terrain Model (DTM) from the Tapajós region in Brazil… Describe circular depressions, aligned features, and possible anthropogenic patterns.*

---

## 📦 Outputs

- **Processed Notebook**: Includes elevation histogram, hillshade preview, and GPT response
- **GeoJSON**: [`footprints.geojson`](footprints.geojson) — Top 5 high-density GEDI anomaly regions
- **Text Log**: [`footprints.txt`](footprints.txt) — WKT strings for reproducibility

---

## 🧠 GPT Model Used

- `gpt-4-1106-preview`
- Called via `openai-python` API inside the notebook
- Responses grounded in visual cues + spatial context

---

## 🗺️ Footprint Summary (Bounding Boxes)

| Footprint ID | WKT Bounding Box |
|--------------|------------------|
| 1 | `POLYGON ((-58.0000 1.3, -58.0000 1.35, -58.0500 1.35, -58.0500 1.3, -58.0000 1.3))` |
| 2 | `POLYGON ((-57.9000 1.15, -57.9000 1.2, -57.9500 1.2, -57.9500 1.15, -57.9000 1.15))` |
| 3 | `POLYGON ((-57.8000 1.0, -57.8000 1.05, -57.8500 1.05, -57.8500 1.0, -57.8000 1.0))` |
| 4 | `POLYGON ((-58.1000 1.45, -58.1000 1.5, -58.1500 1.5, -58.1500 1.45, -58.1000 1.45))` |
| 5 | `POLYGON ((-58.0500 1.35, -58.0500 1.4, -58.1000 1.4, -58.1000 1.35, -58.0500 1.35))` |

---

## 🛰️ Tools

- `rasterio`, `matplotlib`, `folium` for terrain analysis and overlays
- `openai` Python SDK for GPT call
- `shapely` and `geopandas` for geometry + footprint export

---

## 📌 Next Steps (Checkpoint 2+)

- Link each footprint to a Magellan custom GPT hypothesis
- Integrate TerraBrasilis or other historical boundaries
- Visual anomaly detection using image segmentation
- Add historical coordinates from "The Lost City of Z" sources

---

## 🔒 Notes

This repo uses **public datasets** and does not expose any API keys.  
All output files and prompts are logged for full reproducibility.

---
