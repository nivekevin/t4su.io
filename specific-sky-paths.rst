.. _specific-sun-paths:

﻿Specific Sun Paths
###################

Now that we've seen how to create sun
paths, you may want to study solar radiation during specific time periods.

.. seealso::
   :ref:`drawing-sun-paths`

You can, for example, decide to only plot for specific hours. Here is an
example for plotting the sun's position at noon once a month:

The input goes as such :

-  Set the start date at 21/06 (summer solstice)
-  set your start time at 12:00 (noon)
-  set the end date to 21/12 (winter solstice)
-  leave the end time at 23:59
-  Set the time slice per day to 1440 (24hours)
-  Set the time slice between dates to 30.

.. figure:: https://t4su.files.wordpress.com/2016/09/solar-path-noon-year.png
   :class: size-full wp-image-1029 aligncenter
   :width: 1320px
   :height: 844px

   Position of the Sun at Noon every
21st, from June to December at 24.7° latitude

You may also want to have a more precise idea of the course o the sun
through the entire year. Here is the appropriate input :

-  Set the start date at 21/06 (summer solstice)
-  Set your start time at 00:00
-  Set the end date to 21/12 (winter solstice)
-  Leave the end time at 23:59
-  Set the time slice per day to 10 minutes
-  Set the time slice between dates to 30.

.. figure:: https://t4su.files.wordpress.com/2016/09/solar-path-10m-year.png
   :class: size-full wp-image-1028 aligncenter
   :width: 1436px
   :height: 980px

   Daily Sun Paths every 21st, from June until December, 10-minute intervals
