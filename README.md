# tiles_gen.py

A script to get tiles from mapnik. Area can be defined by bbox, polygon or an OSM polygon; tiles can be served in image files or mbtiles. Run the script without parameters to see command line help.

## Requirements

Mapnik and `python-shapely` package. Optional dependencies are `python-psycopg2` and `sqlite3`.

## Author and license

based on:
* script written by Ilya Zverev, [polytiles](https://github.com/zverik/polytiles)
* based on [generate\_tiles\_multiprocess.py](http://svn.openstreetmap.org/applications/rendering/mapnik/generate_tiles_multiprocess.py), licensed WTFPL.


## Carto
Generate mapnik xml from carto project

```bash
carto project.mml > ../tiles_gen/mapsmd.xml
```
## create symbolic link

```bash
ln -s ../hartamd-carto/symbols/ symbols
ln -s ../hartamd-carto/data/ data
```

## Execute

```bash
./tiles_gen.py -a -1003 -m MBTILES --name hartamd.mbtiles -z 7 10
```
