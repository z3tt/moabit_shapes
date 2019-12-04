# 🗺  Shapefiles for Moabit (Berlin 21)

![./plots/Moabit_By_Levels.png](https://raw.githubusercontent.com/Z3tt/moabit_shapes/master/plots/Moabit_By_Levels.png)

### Shapefiles Included
This repository contains the following shapefiles cropped for my home district [Moabit](https://en.wikipedia.org/wiki/Moabit) in Berlin:

* District border: `sf_moabit_district.shp`<br>
* 4056 buildings: `sf_moabit_build.shp`
  - `OBJECTID`: identification number
  - `Gebaeudefu`: building function number
  - `Gebaeude_1`: building type (in German)
  - `AnzahlDerO`: number of above ground levels
  - `AnzahlDerU`: number of below ground levels
  - `Name`: buidling name (in German)<br>
* Landuse classification: `sf_moabit_landuse.shp`
  - `osm_id`: OSM identification number
  - `code`: 4 digit code defining OSM feature class
  - `fclass`: OSM feature class
  - `name`: name of the feature
  - `green`: green space classification, boolean variable
    * `TRUE` if fclass one of "park", "recreation_ground", "cemetery", "scrub", "forest", "heath", "allotments" or "grass"
    * `FALSE` otherwise<br>
* Road network: `sf_moabit_roads.shp`
  - `osm_id`: OSM identification number
  - `code`: 4 digit code defining OSM feature class
  - `fclass`: OSM feature class
  - `name`: name of the feature
  - `ref`: reference number
  - `maxspeed`: speed limit
  - `oneway`: boolean variable, `T` if feature is a oneway, `F` otherwise
  - `bridge`: boolean variable, `T` if feature is a bridge, `F` otherwise
  - `tunnel`: boolean variable, `T` if feature is a tunnel, `F` otherwise
  - `stroke`: `0.1` in case of "path" and "footway", `0.2` otherwise
  - `layer`: OSM layer<br>
* Railways: `sf_moabit_rails.shp`
  - `osm_id`: OSM identification number
  - `code`: 4 digit code defining OSM feature class
  - `fclass`: OSM feature class
  - `name`: name of the feature<br>
* Water bodies: `sf_moabit_water.shp`
  - `osm_id`: OSM identification number
  - `code`: 4 digit code defining OSM feature class
  - `fclass`: OSM feature class
  - `name`: name of the feature

### Data Sources
* District borders ("Prognoseräume"): [Technologiestiftung Berlin](https://data.technologiestiftung-berlin.de/dataset/lor_prognoseraeume/en); last modified: 2015-12-31
* Buildings: [Geoportal Berlin via ESRI DE Open Data](https://opendata-esri-de.opendata.arcgis.com/datasets/ecf431fd8c394ee1b2fd7d54563e7b81_0); uploaded: 2019-01-25
  - Note: `Gebäude__Berlin.shp` and `Gebäude__Berlin.dbf` are not included here due to file size limits
* Landuse categories, road network, railsways and water bodies: [OpenStreetMap contributors via Geofabrik GmbH](https://download.geofabrik.de/europe/germany/berlin.html); last update: 2019-12-04
