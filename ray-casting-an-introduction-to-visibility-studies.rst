.. _ray-casting:

Ray Casting : an Introduction to Visibility Studies
####################################################

Ray Casting involves choosing a point in your urban space, from which
rays will spread at equal distance from each other. The ray stops when
it hits either an obstacle or its set limit. It is the simplest and
quickest way to assess visibility, but doesn't give as much information
as isovists or hedgehog. First off, click on \ **Extensions > t4su >
Visibility studies > RayCasting. **\ A\ ** **\ command box will appear,
giving you the following possibilities:

.. figure:: https://t4su.files.wordpress.com/2016/09/raycasting-box.png
   :class: size-full wp-image-757 aligncenter
   :width: 334px
   :height: 275px

-  Choose the number of rays. This will affect the results' precision,
   but taking the maximum isn't necessarily better : if you select a
   small visible range, you may not need too many rays.
-  The visual range is the maximum length of the rays ; any obstacle
   after said range will not be picked up during the process
-  Set the height (z0 value). If you're using ray casting for visibility
   purposes, keep a z-value around eye-level.
-  Make sure the units you are working with are correct.
-  Finally, you can choose to cast rays in a 2D or 3D space. This is
   entirely up to the type of information you want to collect. If you
   are only interested in street visibility and do not need information
   on the impact of building heights for example, a 2D Ray Casting is
   much more legible and should suffice.

Once you have click \ **OK**, you can click anywhere on your map to cast
your rays, as many times as you need (you do not need to repeat the
procedure to plot a second RayCast).

.. figure:: https://t4su.files.wordpress.com/2016/09/raycasting-result256-40.png
   :class: size-full wp-image-763 aligncenter
   :width: 712px
   :height: 548px

   2D Ray Casting with 256 rays at a distance of 40m

.. figure:: https://t4su.files.wordpress.com/2016/09/raycasting-result-1024-150.png
   :class: size-full wp-image-762 aligncenter
   :width: 700px
   :height: 1016px

   2D Ray Casting with 1024 rays at a distance of 150m

If you are not interested in the rays
themselves, but rather the point of impact they share with the facades
of your buildings, check out CloudOfPoints.
