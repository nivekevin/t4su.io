##############
T4SU Ruby API
##############


.. _T4SU Home Page: http://t4su.wordpress.com

.. default-domain:: rb

Everything explained in this manual can be reproduced through the Ruby Console.

.. warning:: This section is still under construction, and only presents a few limited examples. Nonetheless, we encourage you to understand the logic behind these small scripts and adapt them to your own needs.


Readers:
========

::

    AscReader.new.readAndPlot("d:/tleduc/t4gs/papers/scan-2016/dev/data/dem_ecn_5m.asc", 1.m, true, 1)

::

    ShpDbfReader.new.readAndPlot('d:/tleduc/t4gs/papers/scan-2016/dev/data/vegetation.shp')


Sampling:
=========

::

    SampleFacesAreas.new("vegetation", 15.m, true, -10.cm).run

.. index::
   single: Introduction; Listing

Listing Samples :
=================
::

    EntitiesListing.allConstructionPointsInLayer("SampleFacesAreas_15.00.m_15.00.m").size

Returns the number of entites.

ProjectAllong Z Axis :
======================

::

    ProjectAlongZAxis.new("SampleFacesAreas_15.00.m_15.00.m", true).exec

Select "true" for "upwards" and "false" for "downwards".

::

    EntitiesListing.allConstructionPointsInLayer("ProjectAlongZAxis_upwards_SampleFacesAreas_15.00.m_15.00.m").size

Make Layer Invisible :
======================

::

    Sketchup.active_model.layers['vegetation'].visible = false

Remove Layer :
==============

::

    Sketchup.active_model.layers.remove('SampleFacesAreas_15.00.m_15.00.m', true)

Load Trees :
============

::

    treeCompDef = Sketchup.active_model.definitions.load("~/tree.skp")
    transforms = []
    i = 0
    EntitiesListing.allConstructionPointsInLayer('ProjectAlongZAxis_upwards_SampleFacesAreas_15.00.m_15.00.m').each { 
    |p| transforms.push(Geom::Transformation.new(p.position))
    Sketchup.active_model.active_entities.add_instance(treeCompDef, transforms[i])
    i += 1}

    transforms = nil

Create a Partial 3D Isovist :
=============================

::

    pisov = PIsovist3D.new(aperture = Angle.toRadians(30), z0 = 1.6.m, nbRays = 256, transparency = 0.5, spotColorName = 'Red', tetrahedraColorName = 'Yellow', sketchOption = 1)

Iterating over a Point :
=========================

::

    EntitiesListing.allConstructionPointsInLayer('layerName').each { |p|p.set_attribute("sln_dictionary", 'motion_direction:Array', [0,0,-1]) isov.execWithArgs(pickedPoint = p.position, pickedFace = p) }

Create a line at a point, pointing downards:
=============================================

::

    EntitiesListing.allConstructionPointsInLayer('...').each { |p| e = Sketchup.active_model.entities.add_edges(p.position, Geom::Point3d.new (p.position.x, p.position.y, p.position.z - 1))

Create a 3D isovist:
====================

::

    Iso3D = Isovist3D.new(0.m, 20.m,64, 0.5, 'Red', 'Yellow', 1)

Partial 3D Isovist
==================

::

    Piso3D = PIsovist3D.new(Angle.toRadians(30), 0.M, 20.m, 64, 0.5, 'Red', 'Yellow', 1)
