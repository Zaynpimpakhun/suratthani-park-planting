# suratthani-park-planting
URBAN - Rama IX Park Strategic Planting and Treecare Plan | Urban Resilience Building and Nature
# Suratthani Rama IX Park — Urban Planting Plan

**Strategic tree planting plan for UHI (Urban Heat Island) reduction**  
Rama IX Public Park, Suratthani Municipality, Thailand

Live Dashboard → [zaynpimpakhun.github.io/suratthani-park-planting](https://zaynpimpakhun.github.io/suratthani-park-planting/)

---

## Overview

This project develops a spatial planting recommendation plan for Rama IX Public Park 
in Suratthani, Thailand — a former wetland area now serving as the city's primary 
green space. The plan aims to increase canopy coverage from 31% to over 60% and 
reduce urban surface temperatures through evidence-based tree placement.

Carried out under the **Urban Resilience Building and Nature** project, supported by 
the Federal Ministry for the Environment, Climate Action, Nature Conservation and 
Nuclear Safety of the Federal Republic of Germany (IKI).

---

## Key Results

| Metric | Value |
|--------|-------|
| Park area | 8.97 ha |
| Trees recommended | 437 trees · 14 species |
| Canopy coverage (current) | 31.3% |
| Canopy coverage (projected, 10yr) | ~64% |
| Surface temperature reduction | −2.6°C avg |
| CO₂ sequestration (new trees) | ~9,527 kg/yr |
| Existing tree inventory | 435 trees · 53 species |
| Wildlife observations (iNaturalist) | 381 records |

---

## Planting Zones

| Zone | Character | Dominant Species | Pattern |
|------|-----------|-----------------|---------|
| A — Riparian Edge | Canal buffer | *Barringtonia acutangula*, *Syzygium cumini* | Drift + Layered Edge |
| B — Open Parkland | Activity lawn | *Neolamarckia cadamba* | Cluster + Open Matrix |
| C — Wetland Memory | Former peat bog | *Syzygium* sp., *Palaquium obovatum* | Dense edge ring |
| D — Back-of-House | Building buffer | *Mimusops elengi* | Poisson Cluster + Void |
| E — Playground | Child-safe edge | *Mimusops elengi* | Loose Cluster, edge only |

---

## Data Sources

- **LiDAR Canopy Coverage** — Meta + LiDAR derived canopy shapefile
- **Tree Inventory** — Municipal survey, 435 trees (KML)
- **Zone Boundaries** — Field-verified polygons (KML)
- **Wildlife Data** — iNaturalist observations (381 records, CSV)
- **Satellite Imagery** — Landsat 8/9 for LST baseline

---

## Methodology

1. **Canopy Gap Analysis** from LiDAR shapefile
2. **UHI Priority Scoring** — weighted overlay of LST, imperviousness, distance from water
3. **Species-Site Matching** — zone-specific plant community assignment based on ecology and local species associations
4. **Placement Logic** — zone-specific controlled randomness (Poisson-disk clustering, drift patterns, density gradients)
5. **Wildlife-informed Selection** — species chosen to support observed fauna (iNaturalist)
6. **Ground Truth Verification** — all 437 planting positions verified on-site by municipal staff

**Tools:** Python · GeoPandas · Shapely · Leaflet.js · QGIS

---

## LA Design Principles Applied

- **Massing vs Scattering** — Poisson-disk clusters with glade voids, not uniform grid
- **Plant Community / Phytosociology** — species grouped by ecological association per zone
- **Rhythm & Sequential Experience** — corridor planting with regular spacing and accent nodes
- **Wetland Memory** — planting design references the site's original peat swamp ecology conceptually, not as full ecosystem reconstruction

*Reference: Bidadari Park, Singapore (Habitat Mosaics framework)*

---

## Files
index.html  — Interactive dashboard (standalone, no server required)
planting_verified_437.csv   — Verified planting positions (Lat/Lon + attributes)
planting_verified_437.kml   — Same data for Google Earth / QGIS

---

## How to Use

**View dashboard** → open the live link above

**Use in QGIS:**
- CSV: Layer → Add Delimited Text Layer → set X = Longitude, Y = Latitude, CRS = EPSG:4326
- KML: drag `.kml` directly into QGIS Layers panel

---

## Project Team

Developed under the **Urban Resilience Building and Nature** project  
Suratthani Municipality · Thailand  
*Supported by International Climate Initiative (IKI) of the Federal Republic of Germany*

