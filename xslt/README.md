#unstats2osm

This xslt script can be used to convert the city list you find at [UNGEGN World Geographical Names](http://unstats.un.org/unsd/geoinfo/geonames/Cities.ashx) to a compliant OSM file ready to be used in your maps. Usage: 

```
xsltproc -o cities.osm unstats2osm.xslt http://unstats.un.org/unsd/geoinfo/geonames/Cities.ashx 
```

Then, to obtain a geojson file to be used in your map editing tool (I am using [Kosmtik](https://github.com/kosmtik/kosmtik)) you can use [osmtogeojson](https://github.com/tyrasd/osmtogeojson) (npm install -g osmtogeojson). Usage:

```
osmtogeojson cities.osm > cities.geojson 
```
