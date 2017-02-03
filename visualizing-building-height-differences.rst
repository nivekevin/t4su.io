.. _visualizing-bilding-heights:

Visualizing Building Height Differences
########################################

T4su allows for an easy and rapid way of determining the range of
building heights.

First, click **Extensions > t4su > View > ColorFaces**

.. figure:: https://t4su.files.wordpress.com/2016/09/colorfaces.png?w=300
   :class: size-medium wp-image-326 aligncenter
   :width: 300px
   :height: 177px

The following box will appear :

.. figure:: https://t4su.files.wordpress.com/2016/09/colorfaces-box.png?w=300
   :class: size-medium wp-image-325 aligncenter
   :width: 300px
   :height: 106px

-  Select your color scheme. You will notice that all colors appear
   twice, one of each containing a "-" in front (see picture above).
    Selecting a color scheme without "-" will allocate darker colors to
   smaller buildings and lighter colors to taller buildings. The "-"
   will produce the opposite : darker colors for higher buildings,
   lighter colors for smaller buildings.
-  Select the correct attribute amongst the list. Here we have selected
   building heights (elevation:double) but you could choose
   another criteria ( as long as it is float or integer).
-  Select the number of classes you wish to create. This is entirely up
   to you, but keep in mind that above 5 classes, the difference in
   color may be difficult to distinguish. If you do, we recommend you
   use "fire", "ice" or "GreenRed" which allows for a change of hue
   instead of a change in lightness / darkness. Be careful to select a
   color scheme that `corresponds to the nature of your
   data <http://icaci.org/files/documents/ICC_proceedings/ICC2011/Oral%20Presentations%20PDF/B1-Graphical%20Semiology,%20visual%20variables/CO-084.pdf>`__.

Here is an example of the end result :

.. figure:: https://t4su.files.wordpress.com/2016/09/colorfaces-results.png?w=300
   :class: size-medium wp-image-324 aligncenter
   :width: 300px
   :height: 176px
