.. _selecting:

﻿Selecting Geometries
#####################

One of the many features of T4su is that it will automatically recognize
selected objets when running a process over a layer, and will run that
process only on the selection. So if you want to run a process on an
entire layer, make sure to not have anything selected. The T4su
extension includes a very extensive assortment of selection tools, each
oriented towards a specific usage. You can find this collection when
clicking \ **Extensions > Select**. Regardless of the type of selection,
you will have the same three \ **post-process after selection** choices:

-  simply selecting the geometries;
-  automatically deleting the geometries;
-  moving the geometries to a new layer. The layer will be named
   [NameOfSelectionProcess]-[Date and Time]

Types of Selection Processes :
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  SelectRoofFaces : this will select the top-most geometries
-  SelectWallFaces : this will select all the vertical faces.

These two selection features are pretty good at distinguishing one from
the other. To test this, I've modified my original shapefile, adding a
pointed roof and a small dormer on top of the original roof. The
selection module still works : [gallery ids="1768,1769"
type="rectangular"]

.. figure:: https://t4su.files.wordpress.com/2016/10/selectroof-ensan-mod.png
   :class: wp-image-531 aligncenter
   :width: 630px
   :height: 315px

   Roof Selection

.. figure:: https://t4su.files.wordpress.com/2016/10/selectfaces-ensan-mod.png
   :class: wp-image-531 aligncenter
   :width: 630px
   :height: 315px

   Wall Selection

-  SelectGroundLevelFaces : Selects all the faces with a z0 value of 0.
   When performing this on a building layer, this selects the ground
   floor. This will also work for ground-level Sampled Faces and
   Bounding Box with a Z-value of 0.

-  SelectAllConnectedFaces : used for export towards Salome

-  Select UnnecessaryEdges : selects Tin edges of coplanar surfaces to
   simplify a rough terrain by grouping coplanar faces. This is mainly
   used  used directly with the **remove geometries **\ option. You may
   have to play around with the \ **threshold value**, as there's a
   strong chance some of your faces will disappear. This is because your
   threshold value is too low, meaning your margin of error is too large
   when selecting coplanar faces. Conversely, choosing too small a value
   will hardly reduce your number of faces, if any at all.

.. figure:: https://t4su.files.wordpress.com/2016/10/before-useless-edges.png
   :class: wp-image-531 aligncenter
   :width: 630px
   :height: 315px

   Original Terrain

.. figure:: https://t4su.files.wordpress.com/2016/10/useless-useless-edges.png
   :class: wp-image-531 aligncenter
   :width: 630px
   :height: 315px

   Deleting Unnecessary Edges with a Too Low Threshold will Puncture the Terrain

.. figure:: https://t4su.files.wordpress.com/2016/10/after-useless-edges.png
   :class: wp-image-531 aligncenter
   :width: 630px
   :height: 315px

   Result of Selecting a Correct Threshold for Unnecessary Edges

-  SelectGroupsAccordingToVolumeProperties : Whether the 3D geometry is
   closed (ie, hermetic, bounded by faces on all sides), or open
   (missing a face, or with window or door openings).

An interesting feature is that these types of selections will bypass
geometry Groups.
