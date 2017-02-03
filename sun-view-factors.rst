.. _sun-view-factors:

﻿Sun View Factors
#################

Once you've created a Sun
Path, you
can use it to calculate the **Sun View Factor**, which works a little
like the Sky View
Factor : instead
of checking covisibilities between geometry faces and the sky dome, it
will check the covisibility between a geometry and each point of your
Sun Path. 

.. seealso::
   :ref:`drawing-sun-paths`

   :ref:`calc-svf`

Clicking on \ **Extensions > t4su > Sun Views >
SunViewFactor **\ will enable the following command box :

.. figure:: https://t4su.files.wordpress.com/2016/10/sunviewfactor-box.png
   :class: alignnone size-full wp-image-1473
   :width: 857px
   :height: 170px

-  Select the two corresponding layers : your SunPath layer and your
   geometry layer.
-  You can choose to alerate the results slightly by choosing a specific
   type of sky (from "pure" to "cloudy").

Once that is done, you will find that your geometries now have extra
attributes:

-  directSolarIrradiance:Float
   represents the cumulative theoretical radiative energy received by
   the geometry from the sun at each point, which depends on their
    covisibility and the angle of the sun's rays.*
-  nbHitsTotal:Int, the number rays between the geometry and the
   SunPath points
-  nbMinTotal:Float, the number of rays between the geometry and
   SunPath, multiplied by the frequency of the plot of the Sun Path (eg:
   for a plot every 5 minutes if nbHitsTotal=2, nbMinTotal=10)
-  ratioTotal:Float

You can then use
**ColorFaces** to
see the geographical variations of each of these new attributes. Below,
we've drawn two different maps of the same phenomena : The number of
minutes a defined space
will receive direct sunlight on two opposing dates : 21st of June and
21st of December, the longest and shortest days of the year
respectively. 

.. figure:: https://t4su.files.wordpress.com/2016/10/numminwinter.png
   :class: alignnone size-full wp-image-1473
   :width: 857px
   :height: 170px

   Number of Minutes of Sunlight for the 12st of December

.. figure:: https://t4su.files.wordpress.com/2016/10/numminsummer.png
   :class: alignnone size-full wp-image-1473
   :width: 857px
   :height: 170px

   Number of Minutes of Sunlight for the 21st of June

Wouldn't it
be nice to combine these two into a single map, and be able to visualize
the difference? Learn how with ArithmeticsOnAttributes.

.. seealso::
   :ref:`viewing-dsi`

   :ref:`visualizing-bilding-heights`

   :ref:`sampling-bounding-box`
