---
layout: post
title: Reference - ogr2ogr
---



##Reproject
```bash
ogr2ogr -f "esri shapefile" -s_srs epsg:26913 -t_srs epsg:4326 "output/Ft Lupton CINR Min Coverage_region.shp" "Ft Lupton CINR Min Coverage_region.shp"

```

##CSV2SHP
http://www.carocoops.org/twiki_dmcc/bin/view/Main/OGR_example#Converting_from_CSV_to_shapefile
http://www.gdal.org/ogr/drv_vrt.html

```
ogr2ogr -f "ESRI Shapefile" /home/lfelling/tmp caxxxxad.csv
ogr2ogr -overwrite -f "ESRI Shapefile" /home/lfelling/tmp caxxxxad.vrt
```

##PGSQL Export to GeoJSON, SHP, KML
```
ogr2ogr -f "GEOJson" wi_counties.json PG:"host=localhost user=postgres dbname=adc4web password=postgres" "wi_counties"

ogr2ogr -f "ESRI Shapefile" "usa_cities.shp" PG:"host=localhost user=postgres dbname=pgsql2_test password=postgres" "usa_cities"

ogr2ogr -f "KML" mykml.kml PG:"host=localhost user=postgres dbname=eagli_momentumwest password=postgres” data.v_site_chippewa -s_srs EPSG:4326 -t_src EPSG:4326
```