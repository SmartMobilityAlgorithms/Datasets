# Open Datasets
A home for miscellaneous data.

This would be a very lengthy tutorial on [Overpass QL](https://wiki.openstreetmap.org/wiki/Overpass_API/Overpass_QL) and how you can use this DSL to scrap OpenStreetMaps data filtered and ready to be used by `osmnx` and then we would go through a quick review over [Overpass API](https://wiki.openstreetmap.org/wiki/Overpass_API); this is the official API for reading data from OpenStreetMap servers and [all the online routing services and software use it](https://wiki.openstreetmap.org/wiki/Routing/online_routers) usually along side [Nominatim](https://github.com/osm-search/Nominatim) to do geo\[coding-decoding\]; translating addresses to/from (latitude - longitude).


Also be aware of the fact that most of the time if you are taking your dataset over a very big area, the graph on `osmnx` wouldn't be complete and you would find it even though there is an obvious routes that could make the graph complete but the deficiency usually is because of the incomplete [relaions](https://wiki.openstreetmap.org/wiki/Relation) with the `osm` data.

That is why we will use [OSRM](http://project-osrm.org/) to fill these gap when needed with the scripts that are found in [OSMan](https://github.com/omar-3/OSMan), but most of the times `osmnx` does the job perfectly without any help. 

---
## Datasets

These datasets with the associated `Overpass QL` script that generated the dataset

- TBD...

