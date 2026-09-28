# Fundamentals of GIS & Remote Sensing Portfolio
**Practical Projects & Spatial Analysis with QGIS**  
*Completed through Precision Field Academy*

---

## 📖 Overview
This repository documents end-to-end spatial analysis and remote sensing workflows executed in **QGIS**. The projects cover vector spatial modeling, satellite index derivation, and multi-variable demographic choropleth cartography.

---

## 🗺️ Project 1: School Proximity & Transit Accessibility Analysis (Lagos State)

![Lagos School Accessibility Analysis](images/Lagos_Schools_Proximity_Analysis.jpg)

### Objective
Assess geographic accessibility of educational facilities relative to major transportation corridors in Lagos State to identify urban service clusters and peripheral coverage gaps.

### Methodology & Workflow
1. **Vector Integration:** Ingested point datasets representing educational facilities (categorized into public and private institutions) and line networks of primary transit routes.
2. **Reprojection:** Re-projected datasets from geographic coordinates (`WGS 84 / EPSG:4326`) to metric grid projection (`UTM Zone 31N / EPSG:32631`) to ensure accurate distance measurement.
3. **Proximity Buffering:** Generated a **5 km buffer zone** along primary road corridors to model realistic accessibility and emergency transit zones.
4. **Spatial Overlays:** Intersected school points with buffer corridors to evaluate service coverage density.

---

## 🛰️ Project 2: Satellite Earth Observation & Vegetation Dynamics (AOI)

![Vegetation Index Analysis](images/AOI_Veg_Idx.jpg)

### Objective
Evaluate surface canopy vigor, vegetation health, and land cover patterns across an Area of Interest (AOI) using multi-spectral satellite imagery.

### Methodology & Workflow
1. **Spectral Analysis:** Examined reflectance characteristics across visible red (chlorophyll absorption) and near-infrared (NIR, canopy reflection) bands.
2. **NDVI Computation:** Calculated Normalized Difference Vegetation Index:
   $$\text{NDVI} = \frac{\text{NIR} - \text{Red}}{\text{NIR} + \text{Red}}$$
   Classified pixels into Built-Up, Bare Ground, Less Healthy, and Healthy Vegetation.
3. **EVI Derivation:** Computed Enhanced Vegetation Index to minimize atmospheric noise and background soil brightness, optimizing canopy sensitivity in dense regions.
4. **Comparative Analysis:** Assessed index variations across bare land and dense vegetation canopies.

---

## 📊 Project 3: Regional Demographic & Gender Distribution Atlas (Morocco)

![Morocco Regional Population Atlas](images/Morocco_Population.jpg)

### Objective
Visualize regional population patterns, gender distributions, and geographic imbalances across the 12 administrative regions of Morocco.

### Methodology & Workflow
1. **Attribute Data Joining:** Joined tabular census data (CSV format) to regional polygon boundary shapefiles using common administrative key identifiers.
2. **Thematic Classification:** Applied graduated color symbology (equal intervals and quantiles) to map:
   * **Total Population**
   * **Male Population**
   * **Female Population**
3. **Derived Attribute Modeling:** Computed regional gender variance ratios within the QGIS Field Calculator to generate a dedicated **Gender Difference** classification layer.
4. **Multi-Panel Cartography:** Designed a synchronized 4-panel print layout incorporating coordinate graticules, graduated legends, ratio scale bars, and north arrows.

---

## 🛠️ Software & Data Specifications
* **Software:** QGIS (v3.x)
* **Vector Formats:** Shapefile (`.shp`), GeoPackage (`.gpkg`), Delimited Text (`.csv`)
* **Raster Formats:** GeoTIFF (`.tif`)
* **Coordinate Systems Used:** WGS 84 (`EPSG:4326`), UTM Zone Projections