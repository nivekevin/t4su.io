.. _3d-sky-maps-and-building-facades:

﻿3D Sky Maps and Building Facades
#################################

3D Sky Maps and Building Facades both start from
a half-dome,
at the center of which is the point of interest. Rays start from the
center point, pass through the center of each dome face and continue on,
either hitting a facade or not.

.. figure:: https://t4su.files.wordpress.com/2016/10/skymap-3d-buildingfacade-result.png
   :class: alignnone wp-image-1387
   :width: 670px
   :height: 549px

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
   :ref:`svf-sp`

.. figure:: https://t4su.files.wordpress.com/2016/10/skymap-3d-result.png
   :class: alignnone wp-image-1388
   :width: 668px
   :height: 523px

   Sky-Map 3D over an intersection

.. figure:: https://t4su.files.wordpress.com/2016/10/skymap3d-ray-casting1.png
   :class: alignnone size-full wp-image-1414
   :width: 720px
   :height: 450px

The BuildingFacade module works great for street-level visibility : it
highlights the skyline, the openings in the urban space represented by
"dips" in the dome formation, allowing you to assess the relative
confinement of urban space.

.. figure:: https://t4su.files.wordpress.com/2016/10/buildingfacades-street.png
   :class: alignnone wp-image-1381
   :width: 677px
   :height: 421px

   Typical BuildingFacade profile for a narrow street

Once built, the dome faces also hold an attribute,
"dist\_to\_facade"(float). This feature expresses the distance between
the point of interest and the obstacle represented by the dome face.

.. figure:: https://t4su.files.wordpress.com/2016/10/buildingfacade-rubyconsole.png
   :class: alignnone size-full wp-image-1386
   :width: 672px
   :height: 277px

   Ruby console showing attributes when using PickUpEntity

You can view it by clicking \ **View > ColorFaces **\ and choosing the
dist\_to\_facade attribute.

.. figure:: https://t4su.files.wordpress.com/2016/10/buildingfacades-colorfaces-box.png
   :class: alignnone size-full wp-image-1384
   :width: 430px
   :height: 137px

   ColorFaces Command Box

Originally, the faces all turn inwards: the results may be more visible
if the faces where reverted. This can be easily achieved by
selecting **Edit > AutomaticReverseFaces**, and selecting your
BuildingFacade layer. Sometimes, intersecting faces are not
automatically reversed. For an optimal result, render your building
layer invisible before reversing your BuildingFacade layer.
