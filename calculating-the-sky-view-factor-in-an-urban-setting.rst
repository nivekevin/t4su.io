.. _calc-svf:

Calculating the Sky View Factor in an Urban Setting
####################################################

The Sky View Factor (SVF) is used in the evaluation of the impact of
urban geometry on the micro-climate, specifically temperature and the
Urban Heat Island phenomenon. The SVF indicates the ratio between :

-  the radiation received / emitted by a surface from/to the sky

and

-  the theoretical total hemispheric radiating environment.

Direct "visibility" between the sky and a plane means radiation can
escape the urban setting into the atmosphere, whereas radiation between
said plane and another plane keeps radiation trapped. Higher SVFs
therefore indicate spaces that would theoretically cool down (emit more
radiation towards the sky) than a space with low SVF.

Let's see how we assess the Sky View Factor in an urban setting. First
off, follow the
instructions to create
a grid layout of the urban space. For this example, we're using a 10x10
grid, with z=0.1m.

Next, select the Sky View Factor in
the BatchProcessing options.

.. seealso::
   :ref:`sampling-bounding-box`

   :ref:`batchprocess`

Fill in the next two command boxes accordingly. In the first box:

-  Select SkyViewFactor as process
-  Select the layer containing your sampled bounding box
-  Select "Sketchup:Face"

.. figure:: https://t4su.files.wordpress.com/2016/09/bbox-5x5-for-svf-box1.png
   :class: wp-image-868 aligncenter
   :width: 651px
   :height: 89px

The second command allows you to control the SVF parameters:

-  Select the number of rays used to calculated the SVF, ie: its
   precision. Be careful though, this process is repeated for each
   sample and will impact your computing time dramatically
-  Set the z0 value to 0.1, meaning we will check the SVF at ground
   level.
-  Select your unit length
-  Finally, select the name under which the values are stored. We
   recommend you keep  the default name "svf" to keep from any
   confusion.

.. figure:: https://t4su.files.wordpress.com/2016/09/bbox-5x5-for-svf-box2.png
   :class: size-full wp-image-869 aligncenter
   :width: 336px
   :height: 177px

Once that is done, you can check your new feature by
selecting **Extensions > View > PickUpEntity ** to view individual
squares, or by going to **Extensions > View > PrintAttributeValues ** and by selecting **svf:Float** in the following
command box to show the values of every sample. 

.. figure:: https://t4su.files.wordpress.com/2016/09/pickupentity-result.png
   :class: size-full wp-image-858 aligncenter
   :width: 519px
   :height: 292px

But there is a much better way of viewing and presenting the data, much
like what we've done when viewing building
heights.

.. seealso::
   :ref:`visualizing-bilding-heights`

Select **Extensions > t4su > View > ColorFaces.** 

.. figure:: https://t4su.files.wordpress.com/2016/09/view-svf-box.png
   :class: size-full wp-image-860 aligncenter
   :width: 446px
   :height: 148px

-  In the next command box, select the color range you wish to use.
-  In the drop-down menu next to "select attribute's name", find and
   select "svf:Float"
-  Select the number of classes you want for your map.
-  Hit \ **OK**

Your grid should be colored to resemble something like this :

.. figure:: https://t4su.files.wordpress.com/2016/09/skyview-10x10-result.png
   :class: size-full wp-image-860 aligncenter
   :width: 446px
   :height: 148px


.. figure:: https://t4su.files.wordpress.com/2016/09/skyview-10x10-result-box.png
   :class: size-full wp-image-860 aligncenter
   :width: 446px
   :height: 148px

Unless you've taken a color range with a "-" in front, lighter values
express areas with a high SVF, meaning areas which "view" much of the
sky. Darker areas, mostly in small streets and inside building blocks,
do not "see" much sky directly : most of the radiation is captured and
recaptured by adjacent walls.
