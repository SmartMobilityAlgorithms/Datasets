# Datasets

This repo contain information about how to obtain or compile a dataset for the coruse project problem. 

---
## Geospatial Datasets
Geospatial datasets contain map locations of regions or points of interest.

### 1. Compile your dataset
You can compile your own dataset using [Overpass QL](https://wiki.openstreetmap.org/wiki/Overpass_API/Overpass_QL) language that runs on [Overpass turbo](http://overpass-turbo.eu/). You can use this query langauge to mine OpenStreetMaps data and filter it and get it ready to be used by `osmnx` or any library that parses `.osm` files and then we would go through a quick review over [Overpass API](https://wiki.openstreetmap.org/wiki/Overpass_API), which is the official API for reading data from OpenStreetMap servers and [all the online routing services and software use it](https://wiki.openstreetmap.org/wiki/Routing/online_routers) and usually along side with it we would have [Nominatim](https://github.com/osm-search/Nominatim) to do geo\[coding-decoding\]; translating addresses to/from (latitude - longitude). 

Also be aware of the fact that most of the time if you are taking your dataset over a very big area in the map, the graph parsed from the data by `osmnx` wouldn't be complete even though there are physical feasible routes that could make the graph complete and connect all the nodes, but the deficiency usually is because of the incomplete [relaions](https://wiki.openstreetmap.org/wiki/Relation) and data of `osm` -- don't worry about that now.

That is why we will use [OSRM](http://project-osrm.org/) to fill these gaps when needed with the scripts that are found in [OSMan](https://github.com/omar-3/OSMan), but most of the times `osmnx` does the job perfectly without any help when the graph is over a small area (like the complete map of UofT). 

[Overpass turbo](http://overpass-turbo.eu/)'s Wizard provides an easy way to auto-generate Overpass QL queries. Wizard syntax is similar to a search engine. An example of Wizard syntax is `amenity=hospital` that generates an Overpass QL query to find all the hospitals in certain region of interest. Hospital locations will be visualized on the map and can downloaded/copied using "Export" button as GeoJSON, GPX, KML, raw OSM data, raw data directly from Overpass API. You can them us `osmnx` to read `.osm` file with [`osmnx.graph_from_xml`](https://osmnx.readthedocs.io/en/stable/osmnx.html?highlight=from%20file#osmnx.graph.graph_from_xml).

The following `Overpass turbo`'s wizard synatx: 
#
* `amenity=restaurant in "Toronto, Canada"` to find all resturant in City of Toronto.
* `amenity=cafe and name="Tim Hortons"` to find all Tim Hortons coffee shops.
* `(amenity=hospital or amenity=school) and (type:way)` to find hospitals and schools with close ways mapped.
* `amenity=hospital and name~"General Hospital"` will find all the hospitals that have the term General Hospital as part of their names. 
#

**Contributing:** You have something cool and you want to share it with us? If you got your data by downloading it directly from OpenStreetMaps and did some filtering with `osmfilter`, open a pull request with the details of the data and how you filter it. If you got your data with [overpass turbo](http://overpass-turbo.eu/), please attach your `Overpass QL` script with the data so we can replicate your results and maybe we can learn a thing or two from your script.

### 2. Avialable open datasets
* [Geofabrik](https://download.geofabrik.de/index.html)
* [Factory POI](http://www.poi-factory.com/)
* [Global Rural-Urban Mapping Project (GRUMP)](https://sedac.ciesin.columbia.edu/data/set/grump-v1-settlement-points)
* [GeoNames Data](https://www.geonames.org/export/)
* ...

### 3. Commerically available datasets
* [Planet.osm](https://planet.openstreetmap.org/)
* [Factual Global Places](https://www.factual.com/data-set/global-places/)
* [TravelTime API](https://docs.traveltime.com/api/overview/introduction)
* [Precisely](https://www.precisely.com/)
* [World Cities Database](www.worldcitiesdatabase.com )
* [SafeGraph](https://www.safegraph.com/)
* [Google Maps Platform](https://cloud.google.com/maps-platform/)
* [Here Maps for Developers](https://developer.here.com/products/here-sdk)
* ...

---
## Traffic Datasets
* [Toronto Open Data](https://www.toronto.ca/city-government/data-research-maps/open-data/)
* ...

---
## Public Transport Networks Datasets
* [Google Transit APIs](https://developers.google.com/transit)
* ...

---
## Traffic Crashes Datasets
* [A Countrywide Traffic Accident Dataset (2016 - 2020)](https://www.kaggle.com/sobhanmoosavi/us-accidents)
* ...

---
## Emission Datasets
* [Ontario Air Quality Data Sets](http://www.airqualityontario.com/science/data_sets.php)
* ...

---
## Environment Datasets
* [Canadian Open Geospatial Data](https://canadiangis.com/data.php)
* [Government of Canada Open Data Portal](https://open.canada.ca/data/en/dataset)
* ...
