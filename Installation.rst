=============================
Welcome to T4SU’s Doc Page
=============================

Introduction
============

__ http://aau.archi.fr/crenau/

t4su (Tools for SketchUp) is a SketchUp plugin, implemented in Ruby, that gives you the capability:

    * To couple SketchUp (the well-known CAAD tool) with the SOLENE simulation software developed in the CERMA__ laboratory.


    * To achieve several (visual-based) morphological analysis in the urban fabric.

Software
========
The latest version of the plugin is hosted at Renater, France's National Research and Education Network.


References
===========

If you use T4SU, please cite it in any publication reporting results obtained with this software :

.. cite:: 
	Developped by Thomas Leduc,
	(c)UMR 1563 AAU / CRENAU (CNRS/MCC/ECN), 2014-2016

T4SU has already been used in the following publications :

  *Signorelli, V., & Leduc, T. (2016). De l’influence de la végétation et du relief dans la simulation de la ville à l’échelle du quartier. In J.-P. Goulette & B. Ferries (Eds.), SCAN’16 (pp. 125–134). Toulouse, France: Presses Universitaires de Nancy.

  *Signorelli, V., Leduc, T., & Chauvat, G. (2016). How far is far enough? Towards an adaptive and “site-centric” modelling integrating co-visibility constraints for optimal land use. In J.-S. Bailly, D. Griffith, & D. Josselin (Eds.), 12th Spatial Accuracy Assessment in Natural Resources and Environmental Sciences (pp. 233–240). Montpellier, France.

  *Signorelli, V., Leduc, T., & Tourre, V. (2016). Ego-city - Automatic textual description of urban ambiences’ factors. In 3rd International Congress on Ambiances - Ambiances, tomorrow. Volos, Greece.


===================================
Installing T4SU (Linux)
===================================

Sketchup doesn’t propose a native Linux distribution. Nonetheless, many people use wine. There are many tutorials already online explaining how to install sketchup in an Ubuntu-based environment, so we’re not going to go through that again.

Nonetheless, if you are having problems installing, here is a nifty little github project called SkipI  that can make your life a little easier :

First remove any earlier attempts at installing Sketchup. Then open a new terminal and hit :

    wget https://raw.githubusercontent.com/wilfm/SkipI/master/skipi.sh
    chmod +x skipi.sh
    ./skipi.sh

Many Sketchup installation configurations require disabling the Ruby API, which we need. This method will ensure you can keep the API enabled by automatically installing a stable version of Sketchup8. SkipI will also configure a desktop shortcut for you.


Next, downoad the plugin from renater_. Once in Sketchup, you may realize that .rbs folders, which work on Windows, don’t work in older Sketchup versions : you’ll need a .rbz file.

Making a .rbz is fairly straightforward, as it is actually just a .zip file. So send your T4su extension to a compressed file, then simply change the end of it’s name from .zip to .rbz.

You’re now ready to go to Window > Preferences > Install Extensions… and select your t4su_version.rbz file.

If all goes well, that’s all there is to it!

=========================
Installing T4SU (Windows)
=========================

The following installation procedure assumes that you already have installed a recent release of the SketchUp software (Make or Pro).

You simply have to:
	__ http://sourcesup.renater.fr/projects/t4su/
    - Download the latest Ruby script file (a file with the .rbs extension) available on renater_.
    - Install the plugin by placing this Ruby script file into the appropriate folder (the Windows default location is: C:\Users\YOUR USERNAME\AppData\Roaming\SketchUp\SketchUp 2016\Tools),
    - Restart SketchUp.

Once you have restarted SketchUp, you should see that various new commands have been added to the menus bar.

=====================================
Installing T4SU (through the console)
=====================================

The following installation procedure assumes that you already have installed a recent release of the SketchUp software (Make or Pro).

You simply have to:

    - Download the Ruby script file (a file with the .rbs extension) available on renater_;
    - Copy it in the folder you want (let’s assume we choose: D:\myThesis\myScripts\);
    - Open ruby’s Console via the « Window > Ruby Console » menu entry;
    - Install this new script file copying-pasting the following Ruby instruction into the command line interface (the console):

Sketchup::require('D:/myThesis/myScripts/t4su-20161017.rbs')

You should not have to restart SketchUp to see that various new commands have been added to the menus bar.


.. _renater: http://sourcesup.renater.fr/projects/t4su/
