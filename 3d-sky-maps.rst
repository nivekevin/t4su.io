.. _3d-sky-maps:

3D Sky Maps
############

What's a 3D Sky Map ?
=====================

Sky Maps are exactly what they're named after : maps of the visible sky.
Remember Ray Casting? Sky Maps work in a similar fashion : as rays are sent from a point of origin, they either reach the sky vault or they don't : Sky maps only take into account the rays that do reach the sky. It's the "opposite of BuildingFacade".

.. seealso::
    :ref:`3d-sky-maps-and-building-facades`

    :ref:`ray-casting`

Let's imagine for starters that we're at a point on a completely flat
surface, without anything blocking our view. Our result would be
something like this :

.. figure:: https://t4su.files.wordpress.com/2016/10/raycast3dsm.png
   :class: alignnone size-full wp-image-2192
   :width: 528px
   :height: 406px

Of course in an urban setting, some of our rays would be blocked, and the associated dome faces would not appear :

.. figure:: https://t4su.files.wordpress.com/2016/10/raycast3dsm-wall.png
   :class: alignnone size-full wp-image-2200
   :width: 836px
   :height: 664px

How do I create 3D Sky Maps?
============================

You can place 3D Isovists through the point-and-click method by
clicking \ **t4su > Sky views > 3D Sky Map**, or through a
BatchProcess if
you already have your locations set out.

.. seealso::
    :ref:`batchprocess`

What Can I Use Them For?
========================

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


.. figure:: https://t4su.files.wordpress.com/2016/10/3dsm-and-sunvf.png
   :class: alignnone size-full wp-image-2242
   :width: 893px
   :height: 852px

   3D Sky Maps Created by Point-And-Click, Colored by Direct Solar Irradiation Value

We can see a lot more information at
particular points in space than when doing a regular `SunViewFactor over
a tesselated
area: 

.. figure:: https://t4su.files.wordpress.com/2016/10/numminwinter.png
   :class: alignnone size-full wp-image-2242
   :width: 893px
   :height: 852px

we can see what parts of the sky contribute most (and least) to our
direct solar irradiation. Naturally, North-facing faces receive the
least sunlight, and Southern faces at a roughly 45° vertical angle
receive the most. We can thus find which sections of the sky contribute
most to the points' solar energy gains.  


