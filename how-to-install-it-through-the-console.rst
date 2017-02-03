.. _installing-ruby:

﻿Installing T4SU through the Ruby console
#########################################

The following installation procedure assumes that you already have
installed a recent release of the SketchUp software (Make or Pro). You
simply have to:

-  Download the Ruby script file (a file with the .rbs extension)
   available on
   `sourcesup.renater.fr <https://sourcesup.renater.fr/frs/?group_id=684>`__;
-  Copy it in the folder you want (let's assume we choose:
   D:\\myThesis\\myScripts\\);
-  Open ruby's Console via the "*Window > Ruby Console*" menu entry;
-  Install this new script file copying-pasting the following Ruby
   instruction into the command line interface (the console):

::

    Sketchup::require('D:/myThesis/myScripts/t4su-20161017.rbs')

You should not have to restart SketchUp to see that various new commands
have been added to the menus bar.
