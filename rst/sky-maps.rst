
.. _sky-maps:

Sky Maps
#########

Sky Maps are exactly what they're named after : maps of the visible sky.
Sky Maps work in a similar fashion as Ray Casting : as rays are sent from a point of origin, they either reach the sky vault or they don't : Sky maps only take into account the rays that do reach the sky. They can be projected onto a dome, or reprojected onto a disc for a 3D or 2 visualization.

.. _3d-sky-maps:

3D Sky Maps
============

.. seealso::
    :ref:`3d-sky-maps-and-building-facades`

    :ref:`ray-casting`

What's a 3D Sky Map ?
----------------------

Let's imagine for starters that we're at a point on a completely flat
surface, without anything blocking our view. Our result would be
something like this :

.. figure:: /T4SU_screenshots/raycast3dsm.png
   :class: aligncenter
   :scale: 25% 


Of course in an urban setting, some of our rays would be blocked, and the associated dome faces would not appear :

.. figure:: /T4SU_screenshots/raycast3dsm-wall.png
   :class: aligncenter
   :scale: 25% 

How do I create 3D Sky Maps?
-----------------------------

You can place 3D Isovists through the point-and-click method by
clicking \ **t4su > Sky views > 3D Sky Map**, or through a
BatchProcess if
you already have your locations set out.

.. seealso::
    :ref:`batchprocess`

What Can I Use Them For?
-------------------------

On their own and at a first glance, theses domes help you assess the
openness of an area, the local skyline and roughly estimate the sky view
factor. But they hold much more interesting information when used, for
example, to assess solar radiation. As we've
seen, we have methods to calculate the Sun View Factor after having drawn Sun
Paths.
What happens when we reproduce this procedure on our 3D Sky Maps ? To
try this out, first create your domes, then click \ **t4su > Edit >
AutomaticReverseFaces** because half of your dome's faces are facing
inwards. Then proceed to draw your Sun Paths and calculate your Sun View
Factor over the layer containing your 3D Sky Maps. Finally, use
ColorFaces to depict the differences in energy received by each face :

.. seealso::
    :ref:`sun-view-factors`

    :ref:`drawing-sun-paths`


.. figure:: /T4SU_screenshots/3dsm-and-sunvf.png
   :class: aligncenter size-full
   :scale: 25% 

   3D Sky Maps Created by Point-And-Click, Colored by Direct Solar Irradiation Value

We can see a lot more information at
particular points in space than when doing a regular `SunViewFactor over
a tesselated area: 

.. figure:: /T4SU_screenshots/numminwinter.png
   :class: aligncenter size-full
   :scale: 25% 

We can see what parts of the sky contribute most (and least) to our
direct solar irradiation. Naturally, North-facing faces receive the
least sunlight, and Southern faces at a roughly 45° vertical angle
receive the most. We can thus find which sections of the sky contribute
most to the points' solar energy gains.  

.. _3d-sky-maps-and-building-facades:

﻿3D Sky Maps and Building Facades
=================================

3D Sky Maps and Building Facades both start from
a half-dome,
at the center of which is the point of interest. Rays start from the
center point, pass through the center of each dome face and continue on,
either hitting a facade or not.

.. figure:: /T4SU_screenshots/skymap-3d-buildingfacade-result.png
   :class: aligncenter
   :scale: 25% 

   A combination of SkyMap 3d (clear blue) and BuildingFacade (grey) at the same point in space

.. seealso::
   :ref:`running-times`

Whilst Building Facades will only show the dome faces who's rays have
hit an obstacle, 3D Sky Maps will only show those that have not :
They show complementary information. So when is one or the other more
appropriate?

Sky maps are much more useful in showing which parts of the sky are
visible at a certain point. They hold an advantage over 2D Sky Maps,in
that the sky is not projected over a 2D surface: they are not deformed
by any necessary spherical projection.

.. seealso::
   :ref:`calc-svf`

.. figure:: /T4SU_screenshots/skymap-3d-result.png
   :class: aligncenter
   :scale: 25% 

   Sky-Map 3D over an intersection

.. figure:: /T4SU_screenshots/skymap3d-ray-casting1.png
   :class: aligncenter size-full
   :scale: 25% 

The BuildingFacade module works great for street-level visibility : it
highlights the skyline, the openings in the urban space represented by
"dips" in the dome formation, allowing you to assess the relative
confinement of urban space.

.. figure:: /T4SU_screenshots/buildingfacades-street.png
   :class: aligncenter
   :scale: 25% 

   Typical BuildingFacade profile for a narrow street

Once built, the dome faces also hold an attribute,
"dist\_to\_facade"(float). This feature expresses the distance between
the point of interest and the obstacle represented by the dome face.

.. figure:: /T4SU_screenshots/buildingfacade-rubyconsole.png
   :class: aligncenter

   Ruby console showing attributes when using PickUpEntity

You can view it by clicking \ **View > ColorFaces **\ and choosing the
dist\_to\_facade attribute.

.. figure:: /T4SU_screenshots/buildingfacades-colorfaces-box.png
   :class: aligncenter
   :scale: 80%

   ColorFaces Command Box

Originally, the faces all turn inwards: the results may be more visible
if the faces where reverted. This can be easily achieved by
selecting **Edit > AutomaticReverseFaces**, and selecting your
BuildingFacade layer. Sometimes, intersecting faces are not
automatically reversed. For an optimal result, render your building
layer invisible before reversing your BuildingFacade layer.

.. _vegetation:

2D Sky Maps and Vegetation Modelization
========================================

As we have seen, we can easily cover large areas by multiplying a single
object, such as a person to make a crowd or a tree to make a forest.
There are more than `1400 trees to choose
from <https://3dwarehouse.sketchup.com/search.html?q=3d+trees&rsi=sbis&backendClass=entity>`__\ in
the 3D Warehouse, you really have a large choice. So are all SketchUp
trees the same? What types are there and how do they affect the results
of our visibility studies? Let's take two concrete examples.

.. seealso:
  :ref:`proj`


First Tree : the FaceMe Tree
------------------------------

If you're familiar with Sketchup, you may know about
the \ `faceMe <https://blog.sketchup.com/sketchupdate/making-your-own-face-me-people>`__ technique.
Basically, a 2D Object is set to automatically turn to always face your
camera, no matter which way you look at it (unless you look from above).

.. figure:: /T4SU_screenshots/tree-1.png
   :class: aligncenter size-full
   :scale: 25% 

Second Tree : the Carboard Cutout
-----------------------------------

The Cardboard Cutout also uses the faceMe method for it's vertical face,
but also has an added horizontal face.

.. figure:: /T4SU_screenshots/tree-2.png
   :class: aligncenter
   :scale: 25% 

Comparison :
-------------

Let's now compare the impact these two different trees would have on our
visibility studies. For starters, are the sky maps the same? If they're
not, what else would that change? To find out, import both types of
trees into different layers, and place them at identical spots. To make
sure we compare the same points in space, we can create a path, sample it and
project the sampling points over our terrain. We can then launch a 2D
Sky
Map \ Batchprocess over
our sampled path twice ; once for each tree layer type. 

.. figure:: /T4SU_screenshots/tree-result-1.png
   :class: aligncenter size-full
   :scale: 25% 

   Sky view Factor with Tree 1.

.. figure:: /T4SU_screenshots/tree-result-2.png
   :class: aligncenter size-full
   :scale: 25% 

   Sky view Factor with Tree 2.

.. figure:: /T4SU_screenshots/tree-comparison.png
   :class: aligncenter size-full
   :scale: 25% 

   Comparison of Both Sky View Factors.


Clearly, trees composed of only
a vertical face allow for a much greater sky view factor. In this
particular case, a greater sky view also means greater direct solar
radiation.

.. seealso::
    :ref:`sampling-a-path`

    :ref:`batchprocess`

Conclusion:
-----------

Choosing the correct type of tree is very important : they're part of
every urban setting and need to be taken into account when analysing
urban energy balances. Vegetation's correct integration in such
simulations is still at its premise, mainly because their modelization
induces calculating variable opacity over many complex shapes.
Comparatively, this SketchUp method may not be as precise as other
microclimatic models, but it's definitely much faster. In any case, it's
vital to know what type of geometries we're working with and anticipate
the types of problems that could be encountered, whether it be a 2D, 2D+
or 3D tree model.

.. _ssm.rst::

Sunny Sky Maps
===============

We can project given sun paths onto our 2d sky map. This allows us to quickly understand buildings' impact on solar availability at a point in space, over different periods of time.

First, create the sun paths you wish to have on your sky view graph.

.. seealso::
   :ref:`drawing-sun-paths`

In thisexample, we will be using the sun paths of Winter and Summer solstices,
as well as an equinox, at a latitude of 47°. This allows us to see the
range over an entire year.

.. figure:: /T4SU_screenshots/sunpath-result-year.png
   :class: aligncenter

   Sun Paths during the Solstices in Nantes, France.

Next, click on \ **Extensions > Sun views > SunnySkyMap2D **:

.. figure:: /T4SU_screenshots/sunysky-get.png
   :class: size-full aligncenter

   Reaching SunnySkyMap 

In the following command box, first select the layer containing your sun
path:


.. figure:: /T4SU_screenshots/sunysky-box.png
   :class: size-full aligncenter

   SunnySkyMap Command Box

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

.. figure:: /T4SU_screenshots/different-sv2d-results.png
   :class: aligncenter

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

