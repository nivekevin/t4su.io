.. _sampling-bounding-box:

﻿Sampling the Bounding box
##########################

:date: 2016-09-20 14:39
:tags: 
:author: Kevin Hartwell

As with lines and geometries, the "ground floor" of your SketchUp can also be sampled into points or faces.

.. seealso::
   :ref:`sampling-methods`

Start by clicking \ **Extensions > t4su > Edit > SampleBBoxArea.**

.. figure:: https://t4su.files.wordpress.com/2016/09/bbox-sampling-box.png
   :class: alignnone size-full wp-image-358
   :width: 812px
   :height: 316px

   Sample BBox Command Box

-  Set the X sampling distance : that is the direction of the red line
   in Sketchup. The "(less than [...m])" gives you an information on how
   large the bounding box will be.
-  Set the Y sampling distance : that is the length of the sample in the
   direction of the green line.
-  You can set the z0 value. You may want to change this for several
   reasons: if you are studying at which intersections a driver would be
   directly blinded by the incoming sunlight, it would be best to set
   the z-value at eye-level when sitting down. If you are looking at how
   much direct sunlight hits the ground, setting a z0 value to 0 or 0.1
   is more appropriate.
-  You can select your unit length, which should not change throughout
   your project, and be in concordance with your original SketchUp
   model.
-  The "**Sample into**" is very important:

   -  If you select **SketchUp::ConstructionPoint**, points will be
      created. In this case, X and Y distances represent the distance
      between points (every Xmeters in the "red direction", every Y
      meters in the "green direction").
   -  If you select \ **SketchUp::Face**, rectangles or squares will be
      created. In this case, X and Y distances represent the length of
      the sides of the sampling area.

-  Finally, selecting \ **indoor or outdoor **\ will sample either the
   area inside of your geometries (indoor) exclusively, or use the
   building faces as a limit to sample only the outside area
   (outdoor). If you choose \ **both**, the bounding box will be evenly
   discretized, ignoring any limits set by your buildings/geometries.

.. seealso::
   :ref:`calc-svf`
   :ref:`sun-view-factors`

.. figure:: https://t4su.files.wordpress.com/2016/09/boundingbbox-result-2.png
   :class: alignnone wp-image-656
   :width: 549px
   :height: 397px

   Up-facing view with sampling distances X and Y at 1m
