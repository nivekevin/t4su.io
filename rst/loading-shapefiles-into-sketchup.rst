.. _loading-data:

﻿Loading your data into SketchUp
#################################

Once you have installed t4su,
click on **File>Import...**. As you click on the available file types,
you can notice that several new types of imports are available :

.. figure:: /T4SU_screenshots/loading-types-of-data.png
   :class: aligncenter size-full

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

.. figure:: /T4SU_screenshots/boundingbox1.png
   :class: aligncenter

The X, Y and Z values correspond to the minimum and maximum coordinates of the
geometry. By leaving the default values, the geometry is
re-positioned by taking the lower-left corner of the imported geometry
and setting it at the lower-left corner of the Sketchup local coordinate
system.

.. _csv::

Importing CSV Files
====================

“Comma-Seperated Value” files store tabular data in the form of a plain text file. These files are very common in GIS, partly because they can be combined with the Well-Known Text format, which translate geometries into text. Here’s an example of a CSV file opened in Qgis :

.. figure:: /T4SU_screenshots/csv-qgis1.png
   :scale: 50% 

   Csv File opened in QGIS.


To import csv/wkt files :

Open the file with a traditional GIS software. If need be, refine your selected area, then save your selection as csv.

.. figure:: /T4SU_screenshots/csv-qgis-box1.png

   Saving a CSV file.
  
Chose the following Save Options :

    CREATE_CSVT: NO

    GEOMETRY: AS_WKT

    LINEFORMAT: Default

    SEPARATOR: SEMICOLON

    WRITE_BOM: NO

Open your new CSV file in a text editor. In a regular csv file, your first few lines should resemble something like this :

.. figure:: /T4SU_screenshots/csv-original1.png

   Original QGIS export file

 

SketchUp needs to know the type of each attribute to properly read csv files, so replace the first line from this :

    WKT;id;elevation

to this :

    # the_geom:Polygon; id:int; elevation:float

Of course, Polygon should be replaced accordingly by Linestring or Point. You may also have other attributes other than these basic ones, including boolean and string types.

Delete the “” at the start and end of each line. The fastest way to do this is by clicking Edit > Replace, entering ” in the find line and leaving the replace by line empty, and clicking Replace All.

.. figure:: /T4SU_screenshots/csv-import2.png

   Modified SketchUp import file.

You can then import you file into SketchUp.

Let’s change it up a bit by calculating the sky view factor on the sampled bounding box :

.. figure:: /T4SU_screenshots/bbox-in-sketchup.png
   :scale: 50%

   Sky View Factor on Sampled Bounding Box.

Now that we’ve found what we’re looking for, how can we import this file back to our standard cartography software?
To export CSV files:

Click on t4su > New I/O > CsvWktWriter. The following command box will appear :

.. figure:: /T4SU_screenshots/csvwktwriter-box.png

   CsvWktWriter Command Box.

You can choose to import all (*) or a single Layer at a time. In our example, we’re just interested in our new bounding box. You will also need to supply the geometry type to correctly instantiate the WKT portion of the csv file. In this example, we’re just going to export our bounding box as the oether geometry layer hasn’t been modified.

If you’ve decided to import all your layers (*), you can choose create a single document for all your geometries. Be warned though, this will not work if you have conflicting geometry types : a single csv file cannot contain more than one geometry type. Here’s what our exported bounding box looks like :

.. figure:: /T4SU_screenshots/bbox-csv-export-original.png

   Original Sketchup Output File

Once again, you’ll have to change the first line of your new CSV file : remove the attribute types and replace #the_geom:GEOMETRY by WKT so as to mimic the original file.

.. figure:: /T4SU_screenshots/bbox-csv-export-mod.png

   Modified Qgis Input File

If your file is part of a larger map, select yes at Back to world coordinates. This will reset the geometries to their original geographic location. This way, any geometries or features we have added on SketchUp can be found again at the correct location and coordinate system when re-exporting to a tradition GIS system. To view the Sky Viw Factor in Qgis, **right-click on the layer name > Properties > Style > Categorized > svf > classify**.

.. figure:: /T4SU_screenshots/bbox-in-qgis1.png

   Bounding Box with Sky View Factor viewed in QGIS.

My thanks to Houda Belgacem for letting me use her geometry file and for her help with .csv file conversion.

.. _cir::

Importing Solene Files
=======================

.cir files are Solene’s geometry files. Solene is T4su’s standalone counterpart, so switching from one software to another is pretty straightforward in this case.
Skp2Solene export.png
Exporting a Layer to Solene

You can only import one layer at a time, so make sure everything you need is in the correct one. You can further choose to keep your geometries in a local coordinate system, or use the coordinate system used during the original file import. Solene also uses local coordinates, so choose no unless you’re planning on exporting your Solene file back into real world coordinates further on. You can also choose whether or not to have a unique output file if you’re importing several layers at a time. Unlike other I/O options, this command box does not ask the geometry type because Solene only uses faces.

.. figure:: /T4SU_screenshots/cirvalwriter-box1.png

   Solene Export Command Box

Once you hit OK, choose your export path and file name to finalize the .cir file creation. Once in Solene, create a new project, then click on the icon with the red box, file and arrow to import your .cir file.

.. figure:: /T4SU_screenshots/solene-export.png
   :scale: 50% 

   Layer’s Geometry Imported in Solene
