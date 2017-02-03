.. _proj:

Projecting Along the Z Axis
############################

Projecting along the Z-axis is really helpful in plotting many objects,
like trees or people, on a uneven terrain. The concepts is pretty
straightforward : we first import or create a layer of points, then
project them on our target surfaces. This technique also works for line
segments. So first, import your uneven ground layer and the layers to be
projected:

.. figure:: https://t4su.files.wordpress.com/2016/10/initial-trees.png
   :class: alignnone size-full wp-image-2020
   :width: 1488px
   :height: 612px

   Rough Terrain Layer above a Layer Representing Wooded Areas.

Below our ground layer, we can see
another set of geometries which correspond in this case to forested
areas. That is the layer to perform a `point
sample on.

.. seealso::
   :ref:`building-sampling`

Once you have your points, you can delete the previous layer : we'll
only be needing the points from now on. Hit **t4su > Edit >
ProjectAlongZAxis. **

.. figure:: https://t4su.files.wordpress.com/2016/10/zaxis-trees.png
   :class: alignnone size-full wp-image-2019
   :width: 1490px
   :height: 636px

   The "Wooded Area" Faces are Sampled into Points, which are then Projected onto our Terrain Layer.

Once
the command box appears, select the layer containing your sampling
points. Next, decide which direction to give to the projection : you may
choose between \ **upwards **\ and \ **downwards**. Since our points
were created from a layer \ *below our ground layer*, we are going
to \ **project upwards**. If of course, your point layer is situated
above the ground layer, chose \ **downwards projection**. This will
result in your points "travelling" in the Z direction until they hit a
face (in our case, the ground face).  We can then use the projected
sampling points as locations for more complex
geometries.

.. figure:: https://t4su.files.wordpress.com/2016/10/final-trees.png
   :class: alignnone size-full wp-image-2018
   :width: 1472px
   :height: 504px

   Example of the Use of Z-Axis Projection

.. seealso::
   :ref:`vegetation`
