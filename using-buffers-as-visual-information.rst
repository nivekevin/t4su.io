.. _buffers:

﻿Using Buffers as Visual Information
####################################

T4su allows you to create buffers around points: a polygon enclosing a
point at a fixed distance. You can access it by clicking **Extensions > t4su > Edit > Buffer**.

.. figure:: https://t4su.files.wordpress.com/2016/10/buffer-box.png
   :class: alignnone size-full wp-image-1836
   :width: 1062px
   :height: 234px

The buffer's form can be either **Round** or **Mitre**, meaning
square.

.. figure:: https://t4su.files.wordpress.com/2016/10/round-buffers1.png
   :class: alignnone size-full wp-image-1836
   :width: 1062px
   :height: 234px

   Round 2D Buffers

.. figure:: https://t4su.files.wordpress.com/2016/10/square-buffers.png
   :class: alignnone size-full wp-image-1836
   :width: 1062px
   :height: 234px

   Mitre 2D Buffers

The buffer's command box also allows you to set your buffer in 2D or 3D
space. If you have selected a mitre buffer, the 3D result will be a
cube, the size of the sides being your **set buffer size**. If you've
selected a round buffer, your **set buffer size** will represent the
length of the radius of a sphere.

.. figure:: https://t4su.files.wordpress.com/2016/10/cube-buffers.png
   :class: alignnone size-full wp-image-1836
   :width: 1062px
   :height: 234px

   Cubic Buffer

.. figure:: https://t4su.files.wordpress.com/2016/10/round-buffers.png
   :class: alignnone size-full wp-image-1836
   :width: 1062px
   :height: 234px

   Spheric Buffer

Be warned : these buffers are regular geometries in your field. If they
are left apparent while running a module that requires ray casting, your
buffers will be taken into account and **will interfere with the calculations**.


