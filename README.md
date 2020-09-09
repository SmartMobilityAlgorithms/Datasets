# Open Datasets

This would be a repository containing a lot of example on the usage of [Overpass QL](https://wiki.openstreetmap.org/wiki/Overpass_API/Overpass_QL) language that runs on [Overpass turbo](http://overpass-turbo.eu/) and how you can use this language to mine OpenStreetMaps data and filter it and get it ready to be used by `osmnx` or any library that parses `.osm` files and then we would go through a quick review over [Overpass API](https://wiki.openstreetmap.org/wiki/Overpass_API), which is the official API for reading data from OpenStreetMap servers and [all the online routing services and software use it](https://wiki.openstreetmap.org/wiki/Routing/online_routers) and usually along side with it we would have [Nominatim](https://github.com/osm-search/Nominatim) to do geo\[coding-decoding\]; translating addresses to/from (latitude - longitude). 

[Overpass turbo](http://overpass-turbo.eu/)'s Wizard provides an easy way to auto-generate Overpass QL queries. Wizard syntax is similar to a search engine. An example of Wizard syntax is `amenity=hospital` that generates an Overpass QL query to find all the hospitals in certain region of interest. Another example is `(amenity=hospital or amenity=school) and (type:way)` to find hospitals and schools with close ways mapped. `amenity=hospital and name~"General Hospital"` will find all the hospitals that have the term General Hospital as part of their names. 

Also be aware of the fact that most of the time if you are taking your dataset over a very big area in the map, the graph parsed from the data by `osmnx` wouldn't be complete even though there are physical feasible routes that could make the graph complete and connect all the nodes, but the deficiency usually is because of the incomplete [relaions](https://wiki.openstreetmap.org/wiki/Relation) and data of `osm` -- don't worry about that now.

That is why we will use [OSRM](http://project-osrm.org/) to fill these gaps when needed with the scripts that are found in [OSMan](https://github.com/omar-3/OSMan), but most of the times `osmnx` does the job perfectly without any help when the graph is over a small area (like the complete map of UofT). 

---
## Datasets

The following `OverPass QL` scripts 

* All nodes/ways/relations in a bounding box

* All firestations around a point of interest

* All the hospitals in Toronto

* All Tim Hortons in Vancouver


---




## Contributing

You have something cool and you want to share it with us? If you got your data by downloading it directly from OpenStreetMaps and did some filtering with `osmfilter`, open a pull request with the details of the data and how you filter it. If you got your data with [overpass turbo](http://overpass-turbo.eu/), please attach your `Overpass QL` script with the data so we can replicate your results and maybe we can learn a thing or two from your script.
