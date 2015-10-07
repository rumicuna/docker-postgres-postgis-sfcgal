# PostgreSQL-PostGIS-sfcgal

expand on https://github.com/docker-library/postgres

includes :

* PostgreSQL 9.4
* PostGIS 2.2.0dev
* geos 3.5.0
* gdal 1.11.2
* proj 4.9.1
* cgal 4.6
* sfcgal 1.2.0

Use template `template_postgis` to create your databases with postgis / sfcgal enabled Build it by running

> $ docker build -t ouruser/postgres-postgis-sfcgal .

To run:

> $ docker run --name mypostgis -e POSTGRES_PASSWORD=postgis -d ouruser/postgres-postgis-sfcgal

Connect to a psql shell:

> $ docker run -it --link mypostgis:postgres --rm postgres sh -c 'exec psql -h "$POSTGRES_PORT_5432_TCP_ADDR" -p "$POSTGRES_PORT_5432_TCP_PORT" -U postgres'
