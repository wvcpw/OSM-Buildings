OSM-Buildings
=============
This repo contains files, commands, etc. used to extract (building) features from OpenStreetMap for use with osm2pgsql to convert to PostGIS/PostgreSQL. Eventually this data can be extracted as shapefile/similar - and this is currently its most common use.

###Overview
1. Download extract from OSM API
2. Load into PostGIS
3. Export to portable format for end-users

###Detailed instructions
+ used PostgreSQL for Windows: http://www.enterprisedb.com/products-services-training/pgdownload#windows > Choose a personal password > Uncheck the Stack Builder option before finishing installation. 

+ used PostGIS for Windows: http://postgis.net/windows_downloads. Direct link to download: http://download.osgeo.org/postgis/windows/

+ navigate to `C:\Program Files\PostgreSQL\9.x\data` and edit `pg_hba.conf` with a text editor > adjust the IPv4 local line, change md5 to trust, Save file > press the Windows (logo) button, type 'services', right-click the postgresql entry and restart.

+ osm2pgsql for Windows obtained from https://github.com/openstreetmap/osm2pgsql/issues/17 > See bottom of issue thread to determine most recent version of osm2pgsql > Direct link to working version, for us: https://vanguard.houghtonassociates.com/browse/OSM-OSM2PSQL-43/artifact > Download `cygwin-package` and extract the contents to a location (e.g. make a new folder `C:\osm2pgsql`) extract the contents to `C:\osm2pgsql`.

+ to obtain a .osm file: follow this guide https://gist.github.com//wvcpw/dcffce8fea9412f6c178 > place the .osm file in the directory you extracted osm2pgsql to.

+ create a database using pgAdminIII. This program was installed with PostgreSQL and can be accessed from the Start Menu in Windows.

+ osm2pgsql command (can be done by holding shift and right-clicking on the osm2pgsql folder, then opening the command window option): `osm2pgsql -S wvc.style -d your_postgis_database -U postgres -H localhost -x your_osm_file.osm` ...uses the `slu.style` file in this repo. Link to Raw, download this https://github.com/wvcpw/OSM-Buildings/blob/master/wvc.style > Make sure to replace the "your_postgis_database" with the database name created above >Replace the "your_osm_file.osm" with what you named your osm file (can be dragged into the command window). 

+ Connect to PostGIS database from QuantumGIS and add buildings/polygons layer > Save As shapefile or other format, and potentially reproject coordinate system.

