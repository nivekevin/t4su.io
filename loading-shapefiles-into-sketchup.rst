.. _loading-data:

﻿Loading your data into SketchUp
#################################

Once you have installed t4su,
click on **File>Import...**. As you click on the available file types,
you can notice that several new types of imports are available :

.. figure:: https://t4su.files.wordpress.com/2016/09/loading-types-of-data.png
   :class: alignnone size-full wp-image-43
   :width: 1918px
   :height: 1024px

You can import geometries :

-  `ASCII Grid
   file <https://en.wikipedia.org/wiki/Esri_grid>`__ types (\*.asc)
-  `Solene <http://aau.archi.fr/crenau/solene/>`__ output files (\*.cir)
-  WellKnownText (\*.wkt) / Comma-Separated Values (\*.csv)
-  Geography Markup Language (\*.gml) / Exentible Markup Language
   (\*.xml)
-   Mesh Files produced by `Gmsh <http://gmsh.info/>`__ (\*.msh)
-  Shapefiles (\*.shp)

Once you've selected your file and clicked **import**, a first window
will inform you of the number of geometries found. A second window will
then appear: this is the Bounding Box.

.. figure:: https://t4su.files.wordpress.com/2016/09/boundingbox1.png
   :class: alignnone size-full wp-image-63
   :width: 422px
   :height: 397px

The X, Y and Z values correspond to the minimum and maximum coordinates of the
geometry. By leaving the default values, the geometry is
re-positioned by taking the lower-left corner of the imported geometry
and setting it at the lower-left corner of the Sketchup local coordinate
system.
