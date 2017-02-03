.. _svf-sp:

﻿Joining 2D Sky Maps and Sun Paths with SunnySkyMap
###################################################


Sky View Factors help in the comprehension of an area's potential direct
sunlight in a given amount of time. They are widely used in research
concerning the relationship between urban morphology and climate, such
as the evaluation of heat island effects.

You can find out how to create a simple sky view graph here. T4su allows
use to go a step further : we can directly integrate our sun paths into
our sky view graph. Here is how.

First, create the sun paths you wish to have on your sky view graph.

.. seealso::
   :ref:`drawing-sun-paths`

In this
example, we will be using the sun paths of Winter and Summer solstices,
as well as an equinox, at a latitude of 47°. This allows us to see the
range over an entire year.

.. figure:: https://t4su.files.wordpress.com/2016/09/sunpath-result-year.png
   :class: wp-image-531 aligncenter
   :width: 630px
   :height: 315px

Next, click on \ **Extensions > Sun views > SunnySkyMap2D **:

.. figure:: https://t4su.files.wordpress.com/2016/09/sunysky-get.png
   :class: size-full wp-image-612 aligncenter
   :width: 530px
   :height: 472px

In the following command box, first select the layer containing your sun
path:


.. figure:: https://t4su.files.wordpress.com/2016/09/sunysky-box.png
   :class: size-full wp-image-619 aligncenter
   :width: 626px
   :height: 358px

-  Enter the number of rays used for the calculation, ie: its precision
   in finding the contours of the surrounding buildings
-  Set the visual range : this is the size of your graph. This depends
   your project and your personal preferences : the amount of space you
   have available to plot the graph, how far out you would like to zoom
   and still read it...
-   Select the height at which you would like to calculate your sky view
   factor (z0). If you would like to visualize projections at ground
   floor, 0.0 or 0.1 are an acceptable inputs.
-  Select your unit of length. Be sure to always keep the same units
   throughout the entirety of the project!
-  Next, select the type of projection you would like to use. If you're
   not sure which one fits your needs best, check `this
   page <https://www.uwgb.edu/dutchs/structge/sphproj.htm>`__\ for more
   ample information.
-  Finally, you can change the color of the building projections.

Once you hit \ **OK**, you can start clicking anywhere on your project
to insert an graph at that location.

.. figure:: https://t4su.files.wordpress.com/2016/09/different-sv2d-results.png
   :class: alignnone wp-image-615
   :width: 674px
   :height: 213px

   From left to right : Stereographic, Orthogonal and Isoaire (Equal-Area) projections at the same location.

Reading such graphs are relatively simple. The disc represents a
360-view of the sky: the ground floor is projected at the circumference,
whereas the center of the disk is the point in the sky directly above it
(what happens in between depends on your type of projection). The
filled-in parts of the graph represent parts of the sky that are blocked
off by obstacles.

If a point of the Sun Path is contained in the filled in areas of the
graph, it means that at that specific time and place the point you are
studying is in the shade. Conversely, a sun path point that is not
superimposed over a filled in area of the graph means there is direct
sunlight at that specific time and place.

