# opm-basemaps

Rebooting OPM activities (Oct 2022), here are some notes to sharing with historic and new contributors.

Main OPM interfaces:

- OPM Datasets: interface to OPM geospatial datasets database (using RESTO, PostGIS/PostgresQL DB w/ STAC API)
- OPM S3 Server: download interface to OPM raster (XYZ) and vector tiles (MBTiles, Geopackage), assets (fonts, symbols, patterns); source and 
  processed data products (eg: celestia_mars-shaded-16k_global.tif)
- OPM Basemaps: interface OPM vector tiles and map styles (using TileServer GL, see also Mapbox Style Specification).

Using these interfaces:

- Developers can embed beautiful vector-based basemap in their web applications.
- QGIS/ArcGIS users can visualise and use OPM basemaps, via WMTS end-points.
- Map designer can modify or create new map styles using Maputnik.

For all of this work, we need to define and agree on a common **"planetary map layers schema"**.
That is, a set of attributes for different types of geospatial dataset that one can be used
to style a given map layer. These datasets should also include information that is required
for  geocoding and geospatially-based classification of other assets (eg: data product
footprint).

## Layers/themes/classification

- Nomenclature
  - IAU nomenclature
  - Quadrangles
- Geography ?
- Seasonal pole cap contours
- Morphology
  - Craters
  - Scrap
  - Crater rims
  - Channel talweg
- Topography
  - Contour line
  - Peak
- Geology
  - Geological units
  - Geological linear fitures
  - Goological point features
- Mineralogy
  - Hydrous site locations
  - point-based mineral species locations
  - polygon-based mineral species locations
- Landing sites
  - Landing ellipse
  - Exploration vehicle locations
  - Exploration vehicle tracks
  - Static lander locations
  - Artefact locations

---

- nomenclature
- topography_contours_lines
- topography_contours_polygon
- albedo
- mineralogy_features_pts
- mineralogy_features_poly
- geology_features_pts
- geology_features_poly
- landing_ellipse
- exploration_vehicle_locations
- exploration_vehicle_tracks
- static_lander_locations
- artefact_locations

---

Feature types:

- Nomenclature
  - Albedo Feature
  - Catena
  - Cavus
  - Chaos
  - Chasma
  - Collis
  - Crater
  - Dorsum
  - Fluctus
  - Fossa
  - Labes
  - Labyrinthus
  - Lingula
  - Macula
  - Mensa
  - Mons
  - Palus
  - Patera
  - Planitia
  - Planum
  - Rupes
  - Scopulus
  - Serpens
  - Sulcus
  - Terra
  - Tholus
  - Unda
  - Vallis
  - Vastitas

---
