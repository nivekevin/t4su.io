.. _normal-vector:

﻿Checking the Normal Vector of your Geometries
##############################################

For any simulation to run smoothly, you must make sure that all of
your two-dimensional geometries face the correct direction.

To check this, just click \ **Extensions > t4su > View > PlotAllNormals**. The following box will appear. Select the correct
layer name, and size of the vectors :

.. figure:: /T4SU_screenshots/normal_box.png
   :class: size-medium wp-image-314 aligncenter

   Checking Normals Comand Box

Once you click **OK**, a new layer will be created resembling this
screenshot:

.. figure:: /T4SU_screenshots/normal-not-good.png
   :class: aligncenter

   Incorectly Positioned Normal Vectors.

As you can notice, one of the geometries is facing the wrong way. Let's
change that :

-  select the faces you wish to reverse
-  click on \ **Extensions > t4su > Edit > ReverseFaces**

.. figure:: https://t4su.files.wordpress.com/2016/09/reverting-normals.png
   :class: size-full wp-image-123 aligncenter
   :width: 1446px
   :height: 706px

-  Delete the obsolete PlotAllNormals layer
-  Repeat **Extensions > t4su > View > PlotAllNormals **\ to see if
   everything worked.


