.. _running-times:

﻿Running Times and Geometrical Precision
########################################

Most modules in T4SU allow you to choose your precision. There are
general guidelines for choosing the correct. First, we can notice that
the precision "p" follows the equation p+1 = p\*4, therefore **p(n)
=n\ :sup:`4`** What is the concrete impact of augmenting precision ?
Here is a first concrete example using 3D Sky Map: 

.. figure:: https://t4su.files.wordpress.com/2016/10/sky-map-3d-41.png
   :class: alignnone wp-image-1150
   :width: 659px
   :height: 348px

   3D Skymap (p=4)

.. figure:: https://t4su.files.wordpress.com/2016/10/sky-map-3d-16.png
   :class: alignnone wp-image-1150
   :width: 659px
   :height: 348px

   3D Skymap (p=16)

.. figure:: https://t4su.files.wordpress.com/2016/10/sky-map-3d-64.png
   :class: alignnone wp-image-1150
   :width: 659px
   :height: 348px

   3D Skymap (p=64)

.. figure:: https://t4su.files.wordpress.com/2016/10/sky-map-3d-256.png
   :class: alignnone wp-image-1150
   :width: 659px
   :height: 348px

   3D Skymap (p=256)

.. figure:: https://t4su.files.wordpress.com/2016/10/sky-map-3d-1024.png
   :class: alignnone wp-image-1150
   :width: 659px
   :height: 348px

   3D Skymap (p=1024)

.. figure:: hhttps://t4su.files.wordpress.com/2016/10/sky-map-3d-4096.png
   :class: alignnone wp-image-1150
   :width: 659px
   :height: 348px

   3D Skymap (p=4096)

.. figure:: https://t4su.files.wordpress.com/2016/10/sky-map-3d-16384.png
   :class: alignnone wp-image-1150
   :width: 659px
   :height: 348px

   3D Skymap (p=16384)

For n=1, the most basic form is a four-sided pyramid. For n=2, the number of faces is 4\ :sup:`2`\ = 16. For n=3, the number of faces is 4\ :sup:`3 `\ = 64
and so on. To calculate running times, each type of 3D SkyView has been
repeated ten times, leaving the Ruby Console window on to show the
elapsed time after each run. Although computation times will change
according to the hardware used, here is a general idea of how long each
type of 3D Sky View will take; As you can see, the last construction
took 19 minutes (1150 seconds) to finish!

.. figure:: https://t4su.files.wordpress.com/2016/10/timing-results.png
   :class: alignnone wp-image-1150
   :width: 659px
   :height: 348px

   Time (in seconds) taken for each 3D SkyView construction depending on its number of faces

Precision is also important when `constructing
isovists.
As with Sky Views, we have the a choice of 4\ :sup:`n` precision. In
this case, we are subject to 4, 16, 64 (...) rays to build our isovist.
Too few rays, and the negative space will not be entirely mapped out :

.. figure:: https://t4su.files.wordpress.com/2016/10/rayiso-4.png
   :class: alignnone wp-image-1150
   :width: 659px
   :height: 348px

   2D isovist built with 4 Rays, also shown.

.. figure:: https://t4su.files.wordpress.com/2016/10/rayiso-16.png
   :class: alignnone wp-image-1150
   :width: 659px
   :height: 348px

   2D isovist built with 16 rays, also shown

In the pictures above
(n=1,2 respectively), because the precision is too low, parts of the
isovist traverse the buildings. You can verify this by clicking **View > Face Style > X-ray**. When moving to a precision of 256 (n=3), we can
still notice a small error: 

.. figure:: https://t4su.files.wordpress.com/2016/10/iso-2561.png
   :class: alignnone wp-image-1150
   :width: 659px
   :height: 348px

.. figure:: https://t4su.files.wordpress.com/2016/10/iso-error-256.png
   :class: alignnone wp-image-1150
   :width: 659px
   :height: 348px

Moving to 1024 or 4096 rays correct this problem: they are almost
identical, but the first one takes approximately 0.3 seconds whilst the
second one take 1.3 seconds.

.. figure:: https://t4su.files.wordpress.com/2016/10/iso-1024.png
   :class: alignnone wp-image-1150
   :width: 659px
   :height: 348px

.. figure:: https://t4su.files.wordpress.com/2016/10/iso-4096.png
   :class: alignnone wp-image-1150
   :width: 659px
   :height: 348px

In this case, the isovist with a precision of 1024 rays has the best precision to calculation time ratio.

.. seealso::
   :ref:`what-is-isovist`
