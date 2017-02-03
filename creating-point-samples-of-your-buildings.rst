.. _building-sampling:

﻿Creating Point and Face Samples of your Buildings
##################################################


As we have seen in previous posts, we can sample a line or your bounding box into points or faces.

.. seealso::

   :ref:`sampling-methods`

   :ref:`p2Diso`

   :ref:`sampling-bounding-box`

We can perform the same type of task on your geometry
faces. Here is how :

-  Click \ **Extensions > t4su > Edit > SampleFacesAreas**

You will be asked to fill in the following command box: 

.. figure:: https://t4su.files.wordpress.com/2016/09/samplefacesarea-box.png
   :class: alignnone size-full wp-image-318
   :width: 894px
   :height: 277px

   SampleFaces Command Box

   -  Select the layer to sample.
   -  Select the sampling distance : unlike \ **SampleBBoxArea**,  you
      only have one sampling distance : you can only create squares, or
      points separated by an equal distance in both (X and Y)
      directions.
   -  Select your unit length
   -  You can also select the \ **distance to face**. Similar to the z0
      value, the distance is calculated as the normal to the surface.
      Setting a small distance (eg:0.1) is helpful in avoiding pesky
      overlapping sketchup geometries.
   -  Again, you can choose to create points or faces. This really
      depends on what information you wish to visualize over the
      discretized space.

Here are two examples of the difference between Sample Points and Sample
Faces, both with a 5.0m precision and 0,1m distance from the original
geometries.

.. figure:: https://t4su.files.wordpress.com/2016/09/samplefacesarea-result.png?w=300
   :class: wp-image-320 aligncenter
   :width: 656px
   :height: 289px

.. figure:: https://t4su.files.wordpress.com/2016/09/samplefacesarea-result-2.png?w=300
   :class: wp-image-317 aligncenter
   :width: 656px
   :height: 283px
