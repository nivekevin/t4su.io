.. _p2Diso:

﻿Creating Partial 2D Isovists
#############################

Partial isovists are isovists that are constrained by a certain
aperture. You can automate their process using BatchProcess, or set your
positions and orientation manually by clicking **Extensions > t4su
> Visibility Studies > PIsovist 2D**. If you're using the manual method,
you will be redirected to the \ **Partial Isovist Command Box.**

Partial Isovists through BatchProcessing
========================================

First, import  a
linear geometry (ie: made of lines or multilines) into your Layers, or
draw one yourself using the Line Tool.

.. seealso::
   :ref:`loading-data`

.. figure:: https://t4su.files.wordpress.com/2016/09/import-polyline.png
   :class: wp-image-231 aligncenter
   :width: 588px
   :height: 547px

Next, you'll want to sample your
pathway,
then use a Batch
Process.

.. seealso::
   :ref:`sampling-a-path`

   :ref:`batchprocess`

Select **PIsovist2D** (which stands for Partial 2D Isovist) in the
**Process to apply** and select the correct layer (starting with
SamplePathway[...] if you've created your points through sampling).
Finally, select **Sketchup::ConstructionPoint** as Geometry type.

Partial Isovist Command Box
===========================

Whether you're plotting manually or automatically, you will have to fill
in this command box :

.. figure:: https://t4su.files.wordpress.com/2016/09/p2d-iso-box1.png
   :class: size-full wp-image-312 aligncenter
   :width: 556px
   :height: 361px

-  Select the aperture of your circular sectors (ie: how wide you wish
   the isovist to be)
-  Select the number of rays : a higher number will give a more precise
   outline, but a lower number will greatly accelerate computation time.
   For example, setting the aperture to 30 and the number of rays to 60
   will result in a ray every 0.5 degrees.
-  Select ray length. Some trial-and-error may be needed to adjust this
   parameter : too short, they may not cover enough ground. Too long
   will result in confusing overlapping geometries and longer
   computation times.
-  Setting the z0 value allows you to decide at which height the partial
   isovists are calculated. By default, they are at 1m60, an average
   person's eye-height.
-  You may also change the appearance of the isovists : transparency
   (from 0 to 1, 1 being the most opaque) as well as the color.
-  When you are ready, click \ **OK**

Plotting Partial Isovists Manually
===================================

If don't want to use a Batch Process or would rather select the points manually,you can do so too. Simply **click to set the point of
origin and drag to set the orientation** of your partial isovists.

What do we see ?
=================

.. figure:: https://t4su.files.wordpress.com/2016/09/p2d-iso-result1.png
   :class: wp-image-231 aligncenter
   :width: 588px
   :height: 547px

.. figure:: https://t4su.files.wordpress.com/2016/09/p2d-iso-result2.png
   :class: wp-image-231 aligncenter
   :width: 588px
   :height: 547px

The partial isovists are constrained by the extruded building
geometries. Their profile mimics our visibility as we advance along the
path we have decided upon. We can notice the gradual enlargement of the
isovist as we advance towards an plaza or an intersection.
