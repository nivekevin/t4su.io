.. _solarpage:

################################################
The Science Behind : Solar Radiation
################################################


The Earth and the Sun:
######################

Initial Definitions :
======================


Solar Energy is the amount of energy sent by the sun, meaning the maximum energy received by the Earth, without taking into account climatic conditions (clouds), date or time of day which impact the angle of the surface relative to the sun.


Solar Irradiance (or insolation) is the energy received by a given area of the Earth's surface. It's measured in Watts per square meter. As the angle between Sun and surfaces' normal grows, the solar energy is spread over a larger surface, reducing solar radiance.

.. math:: $latex i\hbar\frac{\partial}{\partial t}\left|\Psi(t)\right>=H\left|\Psi(t)\right>$


Solar Irradiation is Solar Irradiance intergrated over time. 

.. _solarangle:

Solar Angle and Irradiance 
===========================

Both place and time come into play when calculating the the solar angle. Place concerns where we are : latitude and longitude :

.. math:: lat/long = angle

There are two conjoined earthly movement to be taken into account.
- The rotation of the Earth on itself :

	.. math:: 2pi / 24h = 15°/h

- The rotation of the Earth around the Sun : 

	.. math:: 365j +/- 6h

Finally, we must keep in mind that the Earth's rotation axe is inclined at 23°27 from the ecliptic plane. This tilt is at the origin of our yearly seasons : we consider the Earth tilted at +23°27 during summer (Souther hemisphere) and -23°27 during winter, the tilt beeing equal to 0 during the equinoxes.

Time concerns The day of the year and the time of day. All of these factors need to be taken into account before any more local analyses.

.. math:: time @ lat/long = angle

For Solar irradiation, we need to factor in time :

.. math:: delta time @ lat/long = delta angle

.. _atmointerference:

Atmorsphere's Interference
==========================

Radiation reaches the Earth's surface in a more or less direct way, depending on the atmospheric interference. Water, dust and pullutants floating in the air will refract rays, dispersing sunlight in multiple directions. The higher the interference, the more diffused the sunlight will be when reaching the surface. The unit of measurement to describe the amount of cloud cover is called an Okta, where 0 Okta is a completely clear sky and 8 Okta is a completely cloudy sky. 


.. _nightrad:

Night-time Radiation
=====================

Any radiation received by the ground (or buildings) will start releassing heat the moment the air surrounding it turns colder than the soil, typically during night-time.

The radiation emitted has changed to long-wave radiation. In a given urban model, for there to be energy loss (ie, heat loss), the radiation needs to escape back to the atmosphere. This implies a covisibility between the surfaces and the sky vault. More information on :ref:`svfradiation`

Local weather will greatly affect solar radiation, especially the presence of clouds. As the sun passes through them, the light gets reflected and defused.
