# Geometrien der Wahlkreise

Das Original als ESRI-Shape stammt von: [bundeswahlleiter.de/.../downloads.html](https://www.bundeswahlleiter.de/bundestagswahlen/2017/wahlkreiseinteilung/downloads.html)

Das GeoJSON wurde erzeugt mit [GDAL](http://gdal.org):  
`ogr2ogr -f GeoJSON -t_srs EPSG:4326 wahlkreise.geojson original/Geometrie_Wahlkreise_19DBT_VG250_geo.shp`
