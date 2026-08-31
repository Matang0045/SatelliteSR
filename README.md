# 🛰️ SatResolve: Satellite Image Super-Resolution

**Smart India Hackathon 2026 - Official Prototype**  
**Team Name:** [Your Team Name Here]  
**Problem Statement ID:** 26142

---

## 📖 Project Overview
SatResolve is an AI-powered pipeline designed to synthetically enhance free 10m Sentinel-2 satellite imagery into crisp, <4m high-resolution outputs. 

Unlike standard upscaling, our solution explicitly focuses on preserving real-world geographic coordinates (GeoTIFF) and generating **Pixel-Level Uncertainty Maps** to separate true observed data from AI-inferred structures. This ensures the data is strictly reliable for government operations, disaster management, and precision agriculture.

## ✨ Key Features
* **Sub-4m Enhancement:** Achieves a 2.5x spatial resolution upscale while preserving multi-spectral reflectance fidelity (RGB + NIR).
* **Anti-Hallucination & Uncertainty Mapping:** Outputs an AI confidence heatmap (Green/Yellow/Red) to highlight areas of potential generative hallucination.
* **Native GIS Interoperability:** Exports directly to GeoTIFF, retaining full Coordinate Reference Systems (CRS) for immediate use in QGIS and ArcGIS.
* **Downstream Analytical Utility:** Quantifiably improves building footprint extraction and narrow road segmentation for municipal and rural governance.

## 🛠️ Technology Stack
* **Deep Learning Core:** PyTorch, TorchVision
* **Geospatial Processing:** GDAL, Rasterio, Copernicus API
* **Backend API:** FastAPI
* **Frontend/Visualization:** React.js, Leaflet

## 📂 Dataset Reference
* **Input Data:** European Space Agency (ESA) Copernicus Sentinel-2 (L2A) 10m Imagery.
* **Ground Truth / Paired Data:** Our model is trained on a paired dataset sourced from **https://www.kaggle.com/datasets?search=Sentinel+2+Super+Resolution**, which contains perfectly cropped and aligned 10m low-resolution and sub-4m high-resolution patches for accurate model weight calculation.

## 🚀 Getting Started

### Prerequisites
Make sure you have Python 3.9+ installed along with the required geospatial libraries.
```bash
pip install -r requirements.txt
