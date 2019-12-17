# 🗺  GIS Layers for Moabit aka Berlin 21

### Layers Included
This repository contains the following shapefiles cropped for my home district [Moabit](https://en.wikipedia.org/wiki/Moabit) in Berlin that is also known as "Berlin 21":

![./img/layer_overview.png](https://raw.githubusercontent.com/Z3tt/moabit_shapes/master/img/layer_overview.png)

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

Data sources that have been used:

* District borders ("Ortsteile"): [Berlin Open Data](https://daten.berlin.de/datensaetze/rbs-ortsteile-dezember-2014); uploaded: 2014-12-31
* Buildings: [Geoportal Berlin via ESRI DE Open Data](https://opendata-esri-de.opendata.arcgis.com/datasets/ecf431fd8c394ee1b2fd7d54563e7b81_0); uploaded: 2019-01-25
  - Note: `Gebäude__Berlin.shp` and `Gebäude__Berlin.dbf` are not included here due to file size limits
* Landuse categories, road network, railsways and water bodies: [OpenStreetMap contributors via Geofabrik GmbH](https://download.geofabrik.de/europe/germany/berlin.html); last update: 2019-12-04

Other useful reosurces:

* A collection of (all?!) [Berlin's spatial units](https://lab.technologiestiftung-berlin.de/projects/spatial-units/en/) including districts, district areas, LORs, traffic cells, corridors, and ZIP code areas
* [BerlinOpenData](https://daten.berlin.de/) for a range of (potentially) interesting data about Berlin


### Example Plot
![./img/build_levels.png](https://raw.githubusercontent.com/Z3tt/moabit_shapes/master/img/build_levels.png)

***

#### Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)
<div style="width:300px; height:200px">
<img src=https://camo.githubusercontent.com/00f7814990f36f84c5ea74cba887385d8a2f36be/68747470733a2f2f646f63732e636c6f7564706f7373652e636f6d2f696d616765732f63632d62792d6e632d73612e706e67 alt="" height="42">
</div>
