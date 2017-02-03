.. _sampling-a-path:

Sampling A Path
################

As We've seen, sampling
methods will grid your your area of study evenly through point or line sampling, whethere they be your bounding
box, or your geometry faces.
You can also perform this operation on line segments : the command box
for SamplePathway is comparatively very simple :

.. seealso::
   :ref:`sampling-methods

.. figure:: https://t4su.files.wordpress.com/2016/10/linesample-box.png
   :class: alignnone size-full wp-image-1864
   :width: 1075px
   :height: 135px

   "SamplePathway" Command Box

-  Select the layer containing your edge geometry.
-  Set the sampling distance. Curvilinear is a fancy way to say we are
   leaving cartesian coordinates: the distance taken into account
   only follows the line segment, not the X/Y coordinates. If a line is
   10m long and  is sampled every 3m, three points will be made along
   the line at the 3m, 6m, and 9m marks.
-  Always keep the same unit length throughout of your project.

You now have a new Layer called SamplePathWay\_[original\_file\_name],
containing points spread along your line.

.. figure:: https://t4su.files.wordpress.com/2016/10/samplepath-result.png
   :class: alignnone size-full wp-image-1913
   :width: 476px
   :height: 1032px

   Line Segment Sampled every 5m.

.. seealso::
   :ref:`buffers`
   :ref:`p2Diso`
   :ref:`viewing-dsi`
