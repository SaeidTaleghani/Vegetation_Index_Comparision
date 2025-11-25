# Vegetation_Index_Comparision

# Vegetation Index Comparison Using Landsat 8 and Sentinel-2  
### Caspian Provinces — Multi-Sensor Analysis & Visualization

This repository contains a complete Python workflow for computing, mosaicking, stretching, and visualizing vegetation indices from **Landsat 8 (OLI)** and **Sentinel-2 (MSI)** imagery across the **Caspian provinces of Iran**.  
The project includes:

- Multi-scene mosaicking to generate unified regional composites  
- Calculation of four vegetation indices: **NDVI, EVI, SAVI, MSAVI**  
- Percentile-based stretching (2–98%) for improved visualization  
- High-resolution comparison maps (2×2 panels) for LinkedIn-ready presentation  
- Clean, replicable Python code using **Rasterio, NumPy, Matplotlib**

---

##  Project Motivation

During my Teaching Assistant experience at the **University of Waterloo**, I observed how effective visualizations help students intuitively grasp complex geospatial concepts.  
This project aims to:

- Demonstrate how different vegetation indices respond to the same landscape  
- Compare results from two widely used satellite sensors  
- Provide a clear educational example for students and practitioners in **remote sensing, GIS, environmental science, and agriculture**

---

##  Study Area  
The analysis focuses on the **Caspian provinces** of northern Iran — a region with diverse forests, croplands, and coastal ecosystems. The variability in vegetation makes it an ideal area for evaluating multi-sensor vegetation indices.

---

##  Satellites Used

### **Landsat 8 — Operational Land Imager (OLI)**
- 30 m resolution  
- Long-term scientific continuity (Landsat program)  
- Robust spectral response for vegetation monitoring  

### **Sentinel-2 — Multispectral Instrument (MSI)**
- 10–20 m resolution  
- Higher spatial detail  
- Dense revisit frequency (5 days with S2A/S2B)

---

##  Vegetation Indices Computed

### **1. NDVI — Normalized Difference Vegetation Index**
`NDVI = (NIR - RED) / (NIR + RED)`

- Most widely used vegetation index  
- Measures greenness, chlorophyll abundance, and canopy density  
- Range typically **–1 to +1**

### **2. EVI — Enhanced Vegetation Index**
`EVI = 2.5 × (NIR - RED) / (NIR + 6×RED - 7.5×BLUE + 1)`

- More sensitive than NDVI in dense vegetation  
- Reduces atmospheric and canopy background effects  
- Useful for humid and forested regions  

### **3. SAVI — Soil-Adjusted Vegetation Index**
`SAVI = (NIR - RED) / (NIR + RED + 0.5) × (1.5)`

- Corrects NDVI biases in sparsely vegetated or semi-arid landscapes  
- Reduces soil background interference  

### **4. MSAVI — Modified Soil-Adjusted Vegetation Index**
`MSAVI = (2 × NIR + 1 - sqrt((2 × NIR + 1)^2 - 8 × (NIR - RED))) / 2`

- Improved version of SAVI  
- Automatically adjusts for soil effects  
- Ideal for heterogeneous vegetation/soil regions  

---

##  Workflow Overview

1. **Load Landsat 8 and Sentinel-2 scenes**  
2. **Merge multi-date images** using raster mosaicking  
3. **Clip to Caspian provinces boundary**  
4. **Compute NDVI, EVI, SAVI, MSAVI**  
5. **Apply 2–98% percentile stretch**  
   - Enhances visualization  
   - Preserves original numeric values  
6. **Generate comparison panels**  
   - 2×2 layouts  
   - Landsat vs. Sentinel for each index  
7. **Export figures as PNG for sharing/publication**

---

##  Comparison Results

The repository includes two comparison figures:

### **Comparison 1**
- Landsat NDVI  
- Sentinel NDVI  
- Landsat EVI  
- Sentinel EVI  

### **Comparison 2**
- Landsat SAVI  
- Sentinel SAVI  
- Landsat MSAVI  
- Sentinel MSAVI  

These visualizations highlight differences in:

- Spatial resolution  
- Sensor spectral response  
- Index sensitivity  
- Vegetation structure across the region  

---

## 📂 Repository Structure

