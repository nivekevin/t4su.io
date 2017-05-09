.. _drawing-sun-paths:

﻿Drawing Sun Paths
##################

Drawing Paths of Points
========================

Tools4SketchUp offers very different possibilities than the built-in
Shadow feature or other plugins available.

The first step in your solar analysis should be to set the location of
your project, as well as setting the time-period for your analysis. This
will be automatically translated into the appropriate Sun Paths.

First, click on **Extensions > t4su > Sun views > SunPath :**

.. figure:: /T4SU_screenshots/sunpath-get.png
   :class: aligncenter

The next window allows you to enter the necessary information for the
creation of sun paths :

-  Set the correct latitude.
-  Set the start date and time
-  Set the end date and time

It is sometimes practical to select dates that are of special interest
for solar paths such as the solstices : the 21st of June and 21st of
December represent the highest and lowest paths of the year,
respectively.

-  The daily sun path is a continuous line in the sky, which is here
   represented by a series of points. You can therefore decide on the
   interval of time (in minutes) at which the position of the sun is
   saved.
-  If your start and end dates are not on the same day, you will have a
   series of sun paths. If you don't wish to trace a path for every
   single day, you can change this parameter : setting "2" will trace
   one path every two days. Setting "30" will trace a path roughly every
   month.

.. figure:: /T4SU_screenshots/sunpath-box.png
   :class: aligncenter

   Sun Path Command Box

Once your sun paths have been traced and placed in a Layer, as well as
triangulated your
geometries, 
you will be ready to run analyses such as Sun View Factor.

.. seealso::
   :ref:`triangle`

.. figure:: /T4SU_screenshots/sunpath-result-21-09.png
   :class: aligncenter

   Sun Path Result for the 21st of September

.. figure:: /T4SU_screenshots/sunpath-box2.png
   :class: aligncenter

   Setting Sun Paths from September 21st to Ocober 21st every two days, plotting every 10 minutes.

.. figure:: /T4SU_screenshots/sunpath-result-21-09-21-10.png
   :class: aligncenter

   Resulting Solar Paths from September 21st to October 21st.

.. figure:: /T4SU_screenshots/sunpath-result-year.png
   :class: aligncenter

   Resulting Solar Paths from the 21st of June to the 21st of December, every 90 days, with 5-minute intervals.

.. _geode-sp::

Geode Sun Paths
================

Once you’ve  drawn your Sun Paths, you may realize your calculation times for Sun View Factors are too much to handle. There is a way to drastically reduce time, but it come at the price of precision : Geode Sun Paths.

.. figure:: /T4SU_screenshots/geodsunpath-get.png

   Reaching the Geode Sun Path

.. figure:: /T4SU_screenshots/geodsunpath-box.png

   Geode Sun Path Command Box

The “sun points”, representing the location of the sun at a specific time, travel over a sky vault. By intersecting our sun path points with the sky vault, we can find which facets of the sky could replace our sun path.
geodsunpath-isoca-resulthigh-nb-patches
Geode Sun Path with very high resolution : as each face is allocated to only one point, calculation times may stay similar but precision will be lost

.. figure:: /T4SU_screenshots/geodsunpath-geode-result.png

   Geode Sun Path : each face covering multiple points, reducing calculation time

You can use the Geode Sun Path for processes such as the Sun View Factor. In that case, the center of each face is taken into account : the bigger the tessellation and the further away their center is from the original sun path, the less precises the model become.

Here is an exaggerated view of the problem (the model has been designed to maximize the discrepancy) :

.. figure:: /T4SU_screenshots/dsi-geodepath.png

   Gedoe Sun Path result : 83.4 seconds.

.. figure:: /T4SU_screenshots/dsi-pointpath.png

   Point Sun Path : 346 seconds

.. _specific-sun-paths:

﻿Specific Sun Paths
===================

Now that we've seen how to create sun
paths, you may want to study solar radiation during specific time periods.

.. seealso::
   :ref:`drawing-sun-paths`

You can, for example, decide to only plot for specific hours. Here is an
example for plotting the sun's position at noon once a month:

The input goes as such :

-  Set the start date at 21/06 (summer solstice)
-  set your start time at 12:00 (noon)
-  set the end date to 21/12 (winter solstice)
-  leave the end time at 23:59
-  Set the time slice per day to 1440 (24hours)
-  Set the time slice between dates to 30.

.. figure:: /T4SU_screenshots/solar-path-noon-year.png
   :class: size-full aligncenter

   Position of the Sun at Noon every 21st, from June to December at 24.7° latitude.

You may also want to have a more precise idea of the course o the sun
through the entire year. Here is the appropriate input :

-  Set the start date at 21/06 (summer solstice)
-  Set your start time at 00:00
-  Set the end date to 21/12 (winter solstice)
-  Leave the end time at 23:59
-  Set the time slice per day to 10 minutes
-  Set the time slice between dates to 30.

.. figure:: /T4SU_screenshots/solar-path-10m-year.png
   :class: size-full aligncenter

   Daily Sun Paths every 21st, from June until December, 10-minute intervals.
