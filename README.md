# 🗺  Shapefiles for Moabit (Berlin 21)

### Shapefiles Included
This repository contains the following shapefiles cropped for my home district [Moabit](https://en.wikipedia.org/wiki/Moabit) in Berlin:

![./plots/Shapes_Overview.png](https://raw.githubusercontent.com/Z3tt/moabit_shapes/master/plots/Shapes_Overview.png)

* `sf_moabit_district.shp`: District border of Moabit

* `sf_moabit_build.shp`: 4056 buildings
  - `OBJECTID`: identification number
  - `Gebaeudefu`: building function number
  - `Gebaeude_1`: building type (in German)
  - `AnzahlDerO`: number of above ground levels
  - `AnzahlDerU`: number of below ground levels
  - `Name`: buidling name (in German)  

* `sf_moabit_landuse.shp`: Landuse classification
  - `osm_id`: OSM identification number
  - `code`: 4 digit code defining OSM feature class
  - `fclass`: OSM feature class
  - `name`: name of the feature
  - `green`: green space classification, boolean variable
    * `TRUE` if fclass one of "park", "recreation_ground", "cemetery", "scrub", "forest", "heath", "allotments" or "grass"
    * `FALSE` otherwise

* `sf_moabit_roads.shp`: Road network
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
  - `layer`: OSM layer  

* `sf_moabit_rails.shp`: Railway tracks
  - `osm_id`: OSM identification number
  - `code`: 4 digit code defining OSM feature class
  - `fclass`: OSM feature class
  - `name`: name of the feature  

* `sf_moabit_water.shp`: Water bodies
  - `osm_id`: OSM identification number
  - `code`: 4 digit code defining OSM feature class
  - `fclass`: OSM feature class
  - `name`: name of the feature

### Data Sources
* District borders ("Prognoseräume"): [Technologiestiftung Berlin](https://data.technologiestiftung-berlin.de/dataset/lor_prognoseraeume/en); last modified: 2015-12-31
* Buildings: [Geoportal Berlin via ESRI DE Open Data](https://opendata-esri-de.opendata.arcgis.com/datasets/ecf431fd8c394ee1b2fd7d54563e7b81_0); uploaded: 2019-01-25
  - Note: `Gebäude__Berlin.shp` and `Gebäude__Berlin.dbf` are not included here due to file size limits
* Landuse categories, road network, railsways and water bodies: [OpenStreetMap contributors via Geofabrik GmbH](https://download.geofabrik.de/europe/germany/berlin.html); last update: 2019-12-04

### Example Plot
![./plots/Moabit_By_Levels.png](https://raw.githubusercontent.com/Z3tt/moabit_shapes/master/plots/Moabit_By_Levels.png)

***

#### Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)
<div style="width:300px; height:200px">
<img src=https://camo.githubusercontent.com/00f7814990f36f84c5ea74cba887385d8a2f36be/68747470733a2f2f646f63732e636c6f7564706f7373652e636f6d2f696d616765732f63632d62792d6e632d73612e706e67 alt="" height="42">
</div>
