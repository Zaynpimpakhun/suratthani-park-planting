# suratthani-park-planting
URBAN - Rama IX Park Strategic Planting and Treecare Plan | Urban Resilience Building and Nature
# Surat Thani Rama IX Park — Urban Strategic Planting Plan

**Strategic tree planting plan for UHI (Urban Heat Island) reduction**  
Rama IX Public Park, Suratthani Municipality, Thailand

Live Dashboard → [zaynpimpakhun.github.io/suratthani-park-planting](https://zaynpimpakhun.github.io/suratthani-park-planting/)

---

## About

Rama IX Park is an 8.97-hectare public park in central Suratthani, built on former 
wetland and peat swamp. Current canopy coverage sits at 31%, well below the WHO 
recommended 40%. This project develops an evidence-based planting plan to bring 
coverage to 60% over 10 years, while reducing surface temperatures and restoring 
some ecological character of the original site.

The work was carried out under the Urban Resilience Building and Nature project, 
funded by the International Climate Initiative (IKI) of the Federal Republic of Germany.

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

The park is divided into five zones, each with its own species composition and 
planting pattern.

**Zone A: Riparian Edge**
Canal-facing buffer. Species drift in loose clusters parallel to the water, with 
gaps every 25-40m to preserve sightlines. Dominant species: *Barringtonia acutangula*, 
*Syzygium cumini*.

**Zone B: Open Parkland**
The main lawn area around the pond. Large canopy clusters alternate with open space 
for activities. Dominant species: *Neolamarckia cadamba*.

**Zone C: Wetland Memory**
Former peat bog. Planting is restricted to the pond edge only — no trees in water. 
Density increases with distance from the waterline, referencing the feel of the 
original swamp without recreating it literally. Dominant species: *Syzygium* sp., 
*Palaquium obovatum*.

**Zone D: Back-of-House**
Green buffer behind park buildings. Mixed species in loose Poisson-distributed 
clusters with void gaps. Dominant species: *Mimusops elengi*.

**Zone E: Playground**
Edge-only planting around the perimeter. Center kept open for visibility and safety. 
All species are child-safe, thorn-free. Dominant species: *Mimusops elengi*.

---

## Data Sources

- **LiDAR Canopy Coverage** — Meta + LiDAR derived canopy shapefile
- **Tree Inventory** — Municipal survey, 435 trees (KML)
- **Zone Boundaries** — Field-verified polygons (KML)
- **Wildlife Data** — iNaturalist observations (381 records, CSV)
- **Satellite Imagery** — Landsat 8/9 for LST baseline

---

## Methodology

Canopy gaps were identified from LiDAR-derived shapefiles and cross-referenced with 
a field survey of 435 existing trees. Each candidate planting location was scored 
by UHI priority (surface temperature, distance from water, imperviousness) and 
assigned a species based on the ecological character of its zone.

Placement uses controlled randomness rather than a uniform grid: Poisson-disk 
clustering with zone-specific void ratios and density gradients. Species groupings 
follow plant community logic, so trees that appear together make ecological sense 
rather than being scattered randomly.

Wildlife data from 381 iNaturalist observations in the park informed species 
selection. For example, *Barringtonia* and *Syzygium* were prioritized in Zone A 
and C because fruiting species directly support the bird species already recorded 
on site.

All 437 final positions were checked and confirmed by municipal staff on the ground.

Tools used: Python, GeoPandas, Shapely, Leaflet.js, QGIS.

---

## LA Design Principles Applied

- **Massing vs Scattering** : Poisson-disk clusters with glade voids, not uniform grid
- **Plant Community / Phytosociology** : species grouped by ecological association per zone
- **Rhythm & Sequential Experience** : corridor planting with regular spacing and accent nodes
- **Wetland Memory** : planting design references the site's original peat swamp ecology conceptually, not as full ecosystem reconstruction

*Reference: the Guidelines on greenery provision and tree conservation for developments (NPark, Singapore)*

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

## Credit

Developed under the **Urban Resilience Building and Nature** project under funded by IKI, Germany
Surat Thani City Municipality · Thailand  


