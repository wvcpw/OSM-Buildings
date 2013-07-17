OSM-Buildings
=============
This repo contains files, commands, etc. used to extract (building) features from OpenStreetMap for use with osm2pgsql to convert to PostGIS/PostgreSQL. Eventually this data can be extracted as shapefile - and this is currently its most common use.

+ used PostgreSQL for Windows: postgresql-9.2.4-1-windows-x64.exe http://www.enterprisedb.com/products-services-training/pgdownload#windows

+ used PostGIS for Windows: postgis-pg92x64-setup-2.0.3-2.exe http://postgis.net/windows_downloads

+ osm2pgsql for Windows obtained from https://github.com/openstreetmap/osm2pgsql/issues/17

+ osm2pgsql command: https://gist.github.com/jlar/6016041 ...uses the `slu.style` file in this repo. Link to Raw, download this https://raw.github.com/SLUGIS/OSM-Buildings/master/slu.style
