# gdal-snap

Docker image for gdal and Sentinel Application Platform (SNAP) toolbox

## gdal: `osgeo/gdal:ubuntu-small-latest`

* Image used from [gadl](https://github.com/OSGeo/gdal/blob/master/gdal/docker/README.md#small-osgeogdalubuntu-small-latest)
* Raster drivers: all built-in + JPEG + PNG + JP2OpenJPEG + WEBP +SQLite-based ones + network-based ones
* Vector drivers: all built-in + XML based ones + SQLite-based ones + network-based ones + PostgreSQL
* External libraries enabled: libsqlite3, libproj, libcurl, libjpeg, libpng, libwebp,
  libzstd, libexpat, libxerces-c, libpq, libssl, libgeos
* GDAL Python (Python 3.6)
* Base PROJ grid package
* Overall licensing terms of the GDAL build: LGPL + permissive (X/MIT, BSD style, Apache, etc..)

## Sentinel Application Platform (SNAP) toolbox:

* Downloaded and installed from [SNAP All toolboxs for Unix 64-bit](https://step.esa.int/main/download/snap-download/)

See [Dockerfile](Dockerfile)

## Usage example

```shell
docker pull docker.pkg.github.com/geospoc/gdal-snap/gdal-snap:latest
docker run --rm -v /home:/home docker.pkg.github.com/geospoc/gdal-snap/gdal-snap:latest gdalinfo --version
```
