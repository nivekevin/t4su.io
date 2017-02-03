.. _what-is-isovist:

﻿What is an isovist ?
#####################

Isovists represent the entirety of the visible plain (in 2D) or volume
(in 3D) at a specific point in space, bounded by the built environment.
Because isovists are built upon a point, the associated form changes as
it is displaced, just as our notion of urban space changes as we walk
through it. They are frequently used in many fields of visibility
studies : wireless network design, landscape management and analysis,
pedestrian access or security.

.. figure:: https://t4su.files.wordpress.com/2016/09/what-is-isovist-2.png
   :class: wp-image-311 aligncenter
   :width: 624px
   :height: 146px

.. figure:: https://t4su.files.wordpress.com/2016/09/what-is-isovist-1.png
   :class: wp-image-311 aligncenter
   :width: 624px
   :height: 146px


https://t4su.files.wordpress.com/2016/09/what-is-isovist-1.png
https://t4su.files.wordpress.com/2016/09/what-is-isovist-2.png
So how are isovists built? Originating from our point of origin (**view point**), rays are cast into the open space, up to a certain arbitrary distance (**view limit**). The resulting points of impact between each ray and its
barriers (either obstacles or the view limit) are joined to form the
**isovist's edge**. The rays are then replaced by an **isovist area**.

.. seealso::
   :ref:`ray-casting`

.. figure:: https://t4su.files.wordpress.com/2016/09/what-is-isovist-ray-cast.png
   :class: wp-image-311 aligncenter
   :width: 624px
   :height: 146px

.. figure:: https://t4su.files.wordpress.com/2016/09/iso-propre.png
   :class: wp-image-311 aligncenter
   :width: 624px
   :height: 146px

Isovists can also be used to study a space's
`convexity <http://www.spacesyntax.net/symposia-archive/SSS1/SpSx%201st%20Symposium%2097%20-2003%20pdf/1st%20Symposium%20Vol%20III%20pdf/40%20Peponis%20pdfW.pdf>`__,
that is, a region for which every pair of points in said region can be
linked by a straight line also within the region. Here is a simple
example of convex and non-convex spaces:

.. figure:: https://t4su.files.wordpress.com/2016/10/convex-space2.png
   :class: wp-image-311 aligncenter
   :width: 624px
   :height: 146px

   In a Convex Space, Isovists have the Same Shape no Matter the Location of the View Point

.. figure:: https://t4su.files.wordpress.com/2016/10/non-convex-both-isovists.png
   :class: wp-image-311 aligncenter
   :width: 624px
   :height: 146px

   In a Non-Convex (Concave) Space, more than one Isovist is Needed to Map the Totality of the Area.

We can notice the link
between ray casting and isovist formation when playing with its precision.

.. seealso::
   :ref:`running-times`

