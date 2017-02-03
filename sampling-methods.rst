.. _sampling-methods:

﻿Sampling Methods
#################

T4su offers a four ways to sample your geometries. Sampling is
very useful whenever a phenomena may be better studied with spatial
discretization. whether they be flat surfaces or lines. They can be
found by clicking \ **Extensions > t4su > Edit :**

**SampleBBoxArea**
==================

**`SampleBBoxArea <https://t4su.wordpress.com/2016/09/20/sampling-the-bounding-box/>`__ **\ will
operate over the Bounding Box, that is, the smallest surface that will
encompass all your geometries.

[gallery ids="1840,1841,1842,1845,1846,1844" type="rectangular"] You can
find more about the applications of the BoundingBox sampling with these
posts on calculating \ `Sun View
Factors <https://t4su.wordpress.com/2016/10/11/sun-view-factors/>`__ and
the \ `Sky View
Factor <https://t4su.wordpress.com/2016/09/27/calculating-the-sky-view-factor-in-an-urban-setting/>`__.

**SampleFacesAreas**
====================

**`SampleFacesAreas <https://t4su.wordpress.com/2016/09/20/creating-point-samples-of-your-buildings/>`__**
will operate over your geometry faces. It's important to remember that
if anything is selected, the sampling will be made only on said selected
faces. You can take advantage of this when you only want to discretize
certain sections of you buildings: only rooftops or only facades for
example (see: `Selecting
Geometries <https://t4su.wordpress.com/2016/10/26/selecting-geometries>`__).
You can find an application to Sample Faces
`here <https://t4su.wordpress.com/2016/10/26/2030/>`__. [gallery
ids="1886,1887" type="rectangular"]

**SamplePathway**
=================

**`SamplePathway <https://t4su.wordpress.com/2016/10/20/sampling-a-path/>`__ **\ will
sample only sample lines, or edges. The most common use is probably road
networks, or a single specific route. SketchUp is very practical for
drawing line segments in space : once you've drawn your own, create a
new layer (eg:MyPathway). Then select your pathway, go to \ **Entity
Info > Layer: **\ and change it to your newly created layer
(eg:MyPathway). Once you've done that, your line segment will be ready
to be sampled, as you can simply select it in the SamplePathway command
box.

.. figure:: https://t4su.files.wordpress.com/2016/10/linesample-result.png
   :class: alignnone wp-image-1863
   :width: 647px
   :height: 254px

   Line Segments Sampled every 10m.

**GmshTriangulator**
====================

**`GmshTriangulator <https://t4su.wordpress.com/2016/09/21/triangulating-geometries-with-gmsh/>`__**
uses `Gmsh <http://gmsh.info/>`__, a "*free 3D finite-element grid
generator built to provide a fast, light and user-friendly meshing
tool"*.

.. seealso::
   :ref:`triangle`

Gmsh creates a TIN (Triangulated Irregular Network), which holds several
advantages over regular tesselation. Most importantly, a TIN will cover
the entirety of your geometry, and reproduce significant changes in form
and orientation, making it very useful for modelizing rough terrains and
other irregular surfaces. You can find an application to
this type of triangular meshing applied to building facades here.

.. figure:: https://t4su.files.wordpress.com/2016/10/triangulation-result.png
   :class: alignnone wp-image-1923
   :width: 664px
   :height: 293px

   Irregular Building Triangulated with Gmsh
