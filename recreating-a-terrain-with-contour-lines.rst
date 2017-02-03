.. _contour-lines:

﻿Recreating a Terrain with Contour Lines
########################################

On many topographical maps, altitude levels are frequently represented
by contour lines, or "isohypes" : lines representing equal elevation. We
can turn these isolines into a usable digital terrain model. Start
by importing your
lines.

.. seealso::
   :ref:`loading-data`

 This case has an **extra step during the import** **process**
: click on \ **Options.. **\ and change the \ **Build group(s) of entities** line to "**No group"**.\

.. figure:: https://t4su.files.wordpress.com/2016/10/import-isolines.png
   :class: alignnone size-full wp-image-1365
   :width: 785px
   :height: 497px

Next, select
everything **(Ctrl+A)** and click on **Draw > Sandbox > From Contours.** If when selected, your geometries appear individually
bounded by selections boxes, it means you've forgotten to import them
as **No Group**. Instead of re-importing your geometries, you
can **right-click** on your selected geometries, then
hit **Explode**.

.. figure:: https://t4su.files.wordpress.com/2016/10/isolines-get.png
   :class: alignnone wp-image-1363
   :width: 641px
   :height: 362px

   Correct importation of isolines

.. figure:: https://t4su.files.wordpress.com/2016/10/isocontours-bad.png
   :class: alignnone wp-image-1363
   :width: 641px
   :height: 362px

   Incorrect importation of isolines

You should end up with a layer that resembles this:

.. figure:: https://t4su.files.wordpress.com/2016/10/isolines-filled.png
   :class: alignnone wp-image-1363
   :width: 641px
   :height: 362px

Visibility, including sky view factors, changes on a rough terrain: our
sky view is much more restrained at the bottom of a valley than at the
top of a hill. Adding precise altitudes to your map will greatly aid in
the accuracy of your calculations.

.. figure:: https://t4su.files.wordpress.com/2016/10/isocontours-2d-skyview.png
   :class: alignnone wp-image-1419
   :width: 648px
   :height: 279px

   Close-up of three "2D Sky-Maps" on a rough terrain : areas in dips and valleys "see" less of the the sky than the tops of hills.
