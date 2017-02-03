.. _viewing-dsi:

﻿Viewing Direct Solar Irradiation along a Path
##############################################

The city landscaping team has a new shipment of flowers, and they must
decide where to plant them. They already have a general idea along a new
pathway, using planters that reach two meters high so they can be seen
from afar. These plants are very fragile and burn easily in the direct
sun.

To find the ideal spot, we first have to recreate the path with line
segments that you can import or draw with the SketchUp tool (we will be
using the one we've
used before to
explain sampling points). We then proceed to the sampling of line or
multi-line into points for example every 5m.

.. seealso::
   :ref:`p2dIso`

Then, we need to emulate the planters. To do so, we can create a 3D
buffer. Click on **Extensions > Edit > Buffer**


.. figure:: https://t4su.files.wordpress.com/2016/09/pathway-buff-get.png
   :class: alignnone size-full wp-image-904 aligncenter
   :width: 493px
   :height: 353px

Select the name of the layer containing your sampled
pathway and the geometry of the samples (ConstructionPoints). Next, you
have the choice to create Round buffers or Mitre buffers (ie, with sharp
corners). Select its size : we want 2m because we want to know the
conditions at the top of our pedestals, not at ground floor.

.. figure:: https://t4su.files.wordpress.com/2016/09/pathway-buff-box.png
   :class: alignnone size-full wp-image-903 aligncenter
   :width: 727px
   :height: 248px


.. figure:: https://t4su.files.wordpress.com/2016/09/pathway-buff-res-1.png
   :class: alignnone size-full wp-image-909 aligncenter
   :width: 1631px
   :height: 803px

Next, we would like to know how
much direct solar radiation each pedestal top would receive throughout
the year. Create the appropriate sun
paths.

.. figure:: https://t4su.files.wordpress.com/2016/09/pathway-buff-res-1.png
   :class: alignnone size-full wp-image-909 aligncenter
   :width: 1631px
   :height: 803px

.. seealso::
   :ref:`specific-sun-paths`

Our plants are here to stay, so let's create sun paths for the entire
year. Go to **Extensions > t4su > Select > SelectRoofFaces ** and
select your buffer layer.

.. figure:: https://t4su.files.wordpress.com/2016/09/pathway-buff-select-roofs.png
   :class: alignnone size-full wp-image-908 aligncenter
   :width: 726px
   :height: 117px

 We are finally
ready to calculate the direct solar irradiation. Click on \ **Extensions
 > t4su > Sun views > SunViewFactor. ** Select your buffer layer in the
drop-down list, which still has the "rooftops" selected, as well as your
Sunpath layer. You also have the choice of the type of sky. Let's take
the sky will give the highest radiation results : "Pure". If you click
on **Extensions > t4su > View > PickUpEntity**, you can select
each buffer to see the new attributes that have been added. Click
on **Extensions > t4su > View > ColorFaces ** and select
DirectSolarIrradiance:Float as your classification criteria. You
shouldn't need more than four or five classes. The results show that areas close to intersections generally
receive slightly more radiation. It would be best to place the plants
along the narrowest streets.

.. figure:: https://t4su.files.wordpress.com/2016/09/direct-solar-path-result.png
   :class: alignnone size-full wp-image-1010
   :width: 1192px
   :height: 896px

.. figure:: https://t4su.files.wordpress.com/2016/09/direct-soal-where-to-put-plants.png
   :class: alignnone size-full wp-image-1017
   :width: 1078px
   :height: 924px
