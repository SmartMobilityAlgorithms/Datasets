# Open Datasets

This would be a very lengthy tutorial on [Overpass QL](https://wiki.openstreetmap.org/wiki/Overpass_API/Overpass_QL) language and its only interpreter [Overpass turbo](http://overpass-turbo.eu/) and how you can use this DSL (Domain Specific Language) to scrap OpenStreetMaps data and filter it and get it ready to be used by `osmnx` and then we would go through a quick review over [Overpass API](https://wiki.openstreetmap.org/wiki/Overpass_API). This is the official API for reading data from OpenStreetMap servers and [all the online routing services and software use it](https://wiki.openstreetmap.org/wiki/Routing/online_routers) usually along side [Nominatim](https://github.com/osm-search/Nominatim) to do geo\[coding-decoding\]; translating addresses to/from (latitude - longitude).

Also be aware of the fact that most of the time if you are taking your dataset over a very big area in the map, the graph parsed from the data by `osmnx` wouldn't be complete even though there are physical feasible routes that could make the graph complete and connect all the nodes, but the deficiency usually is because of the incomplete [relaions](https://wiki.openstreetmap.org/wiki/Relation) and data of `osm`.

That is why we will use [OSRM](http://project-osrm.org/) to fill these gaps when needed with the scripts that are found in [OSMan](https://github.com/omar-3/OSMan), but most of the times `osmnx` does the job perfectly without any help when the graph is over a small area (like the complete map of UofT). 

---
## Datasets

These datasets with the associated `Overpass QL` script that generated the dataset

- TBD...

---
## Contributing

You have something cool and you want to share it with us? If you got your data by downloading it directly from OpenStreetMaps and did some filtering with `osmfilter`, open a pull request with the details of the data and how you filter it. If you got your data with [overpass turbo](http://overpass-turbo.eu/), please attach your `Overpass QL` script with the data so we can replicate your results and maybe we can learn a thing or two from your script.
