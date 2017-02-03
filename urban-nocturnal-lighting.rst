##############################
Urban Nocturnal Lighting
##############################

As with our trees, we can predefine the location of our streetlamps. We can also loop through our srtreetlamps to imitate the environing lighting conditions.

Create a Streetlamp
====================

This example uses a basic model from the 3D warehouse, but you can create your own model streetlamp if you want to. 
Open a new new SketchUp Window and import / create your lampost. Set it as a group. 

Next, create a new layer (let's call it "lightbulb"). Place points where lampost's lightsource would be. If you want to be precise you can set the point inside the lampost. In that case, make sure to remove any transparent faces that would represent the lampost's glass because they will interfere with ray casting. Create a group joining both your lightbulb and streetlamp layer.

Set your geometry at the center of your axes. Save your .skp model, and open your window containing your map. 


Plot your Streetlamps
=====================

Create a new layer of points where you want your streetlamps to be set. Open data locating urban furniture for your area may be available. Otherwise, use sampling points and a projection along the Z axis.

.. seealso::
   :ref:`proj`
   :ref:`sampling-methods`

Next, import your lampost.

.. code:: 

   lampost = Sketchup.active_model.definitions.load('Path/streetlamp.skp)

Two new layer will have been imported : your lampost and your lightbulb. But theses two layers are in the same group. You will need to explode your group to be able to iterate over the lightbulb layer when needed. You can then paste your exploded group over each point :

.. code::

   transforms = []
   i = 0
   EntitiesListing.allConstructionPointsInLayer('myStreetlampPositions').each { |p|
   transforms.push(Geom::Transformation.new(p.position))
   myLampostInst = Sketchup.active_model.active_entities.add_instance(lampost, transforms[i])
   myLampostInst.explode
   i += 1
   }

.. seealso::
   :ref:`vegetation`

Create your 3D Partial Isovists
===============================

Now that your streetlamps and lightbulbs are set, you can make a batch process to create partial 3D isovists.
The last important step is to set the Partial isovist's direction. To achieve this, you need to add an attribute to your lightbulb points :

.. code::

   EntitiesListing.allConstructionPointsInLayer('lightbulb').each { |p|
   p.set_attribute("sln_dictionary", 'motion_direction:Array', [0,0,-1])
   isov.execWithArgs(pickedPoint = p.position, pickedFace = p)
   }

.. seealso::
   :ref:`batchprocess`

