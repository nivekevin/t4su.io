.. _triangle:

Triangulating Geometries with Gmsh
###################################

Unlike other sampling
methods which
result in point samples, or quadrangular (square or rectangle)
 tessellations, Gmsh allows for a complete subdivision of your building
geometries into triangles ; it creates smaller triangles where shapes
are more variable, and larger ones on flatter surfaces.

.. seealso::
   :ref:`sampling-methods`

The first step of the process is to `download
Gmsh <http://gmsh.info/#Download>`__. Keep in mind where you decompress
the .zip file ; you will need to copy/paste that location further on.

.. figure:: https://t4su.files.wordpress.com/2016/09/gmsh-triangulator-whereis.png?w=680
   :class: wp-image-447 aligncenter
   :width: 642px
   :height: 117px

Next, click on **Extensions > t4su > Edit >  GmshTriangulator**

.. figure:: https://t4su.files.wordpress.com/2016/09/gmsh-triangulator-get2.png?w=680
   :class: alignnone wp-image-448
   :width: 612px
   :height: 388px

The command box that follows allows you to connect Sketchup to Gmsh :


.. figure:: https://t4su.files.wordpress.com/2016/09/gmsh-triangulator-box2.png?w=680
   :class: alignnone wp-image-446
   :width: 619px
   :height: 141px

-  Select the correct layer. In this example, we've previously selected
   a building in our layer, the triangulation will therefore be
   performed only on that specific geometry. If nothing is selected, the
   triangulation will be operated over the entirety of the layer.
-  In the text box below, paste the location of wherever you extracted
   the Gmsh zipfile, and add  \\gmsh.exe to the end.
-  The triangulation will be saved in a temp file, you can decide upon
   its location in the third text box.
-  Finally and most importantly, select the default size for your
   triangles, though some will be much smaller depending on the actual
   shape of your building. You may be tempted to create very small
   triangles for better precision, but keep in mind this will have a
   great impact on computation times, especially once you use them to
   analyse Sun View Factors for example.

The next window will tell you the number of triangles that were created.
After clicking **OK**, A new window will appear that is very much like
the one that appeared when you imported your geometry into Sketchup.
Minimum and maximum x,y,z values express the recalibration of the
coordinate system.

.. figure:: https://t4su.files.wordpress.com/2016/09/gmsh-triangulator-box3.png
   :class: alignnone size-full wp-image-457
   :width: 420px
   :height: 355px

Once you click **OK**, a new layer will be added, named as a series of
numbers. Within it, you may find a copy of your original buildings whose
faces have been triangulated.

.. figure:: https://t4su.files.wordpress.com/2016/09/gmsh-triangulator-result.png?w=680
   :class: wp-image-445 aligncenter
   :width: 568px
   :height: 462px
