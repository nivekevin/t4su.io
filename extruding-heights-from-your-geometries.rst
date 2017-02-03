.. _extrude-path:

﻿Extruding Heights from your Geometries
#######################################

Once you have loaded your
data,
it will appear on your screen as well as in your Layers. The geometries
are, for now, flat. To analyse our data, we must first extrude the
geometries to their corresponding heights.

.. seealso::
   :ref:`loading-data`

To do this, click \ **Extensions > t4su > Edit > FootprintExtruder**


.. figure:: https://t4su.files.wordpress.com/2016/09/footprint-extruder.png
   :class: size-full wp-image-72 aligncenter
   :width: 1920px
   :height: 1018px

A new window will open, asking for the attribute's name. Select the name
of the column where your heights are stored.


.. figure:: https://t4su.files.wordpress.com/2016/09/extruding1.png?w=300
   :class: size-medium wp-image-315 aligncenter
   :width: 300px
   :height: 115px

If you are not sure which column it is, open your file in an external
application and check. Here is an example of a WellKnown-Text file : the
attribute we are looking for is named "elevation:double".

.. figure:: https://t4su.files.wordpress.com/2016/09/cathedral-wkt.png
   :class: wp-image-71 aligncenter
   :width: 497px
   :height: 419px

Select whether you would like the geometries to be extruded Upwards (Z
direction) or Downwards (-Z direction) and click \ **Okay**.

.. figure:: https://t4su.files.wordpress.com/2016/09/extruding-downwards-result1.png
   :class: alignnone wp-image-617
   :width: 656px
   :height: 374px

   Top Image : The imported geometries are rooftops. Bottom Image : Rooftops have been extruded downwards to create buildings

!Attention! If you do not select a specific object, the extrusion will
be carried over all geometries. You may also select specific geometries
before extruding, in which case only the selected figures will be
affected by the extrusion.

.. figure::https://t4su.files.wordpress.com/2016/09/extrudingone.png
   :class: alignnone wp-image-617
   :width: 656px
   :height: 374px

.. figure:: https://t4su.files.wordpress.com/2016/09/extrudingall.png
   :class: alignnone wp-image-617
   :width: 656px
   :height: 374px
