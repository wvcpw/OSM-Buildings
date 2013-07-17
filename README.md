OSM-Buildings
=============
This repo contains files, commands, etc. used to extract (building) features from OpenStreetMap for use with osm2pgsql to convert to PostGIS/PostgreSQL. Eventually this data can be extracted as shapefile - and this is currently its most common use.

+ used PostgreSQL for Windows: postgresql-9.2.4-1-windows-x64.exe http://www.enterprisedb.com/products-services-training/pgdownload#windows

+ used PostGIS for Windows: postgis-pg92x64-setup-2.0.3-2.exe http://postgis.net/windows_downloads

+ osm2pgsql for Windows obtained from https://github.com/openstreetmap/osm2pgsql/issues/17 > Direct link: https://vanguard.houghtonassociates.com/browse/OSM-OSM2PSQL-43/artifact > Download `cygwin-package` and extract to a location (e.g. `C:\osm2pgsql`).

+ to obtain a .osm file: follow this guide https://gist.github.com/jlar/3035152 > place the .osm file in the directory you extract osm2pgsql to.

+ osm2pgsql command: https://gist.github.com/jlar/6016041 ...uses the `slu.style` file in this repo. Link to Raw, download this https://raw.github.com/SLUGIS/OSM-Buildings/master/slu.style

+ Connect to PostGIS database from QuantumGIS and add buildings/polygons layer > Save As shapefile or other format.

