.. _science_behind_skyvf:

######################################
The Science Behind : Sky View Factors
######################################

A Short History
===============


One of the earliest SVF calculations were made with the help of digital cameras mounted with Fisheye lens. The masks were then delineated manually and the SVF is calculated with Steyn's method [#]_. Other raster-based calculations were later developped, using pixel counting methods [#]_ [#]_. To overcome this somewhat manual and time-consuming method [#]_

.. seealso:: 

   If you find yourself confused by the information, equations or terms used on this page, check out the following page:
   :ref:`solarpage`

.. _svfradiation:

Sky View Factor and Radiation
==============================

A Sky View Factor (SVFs) represents the ratio at a point in space between the visible sky and a hemisphere centered over the analyzed location (Oke 1981) :

.. math:: frac{visible sky}/{hemisphere} = between 0 and 1

At a point where the SVF = O, the entire sky is blocked from view by obstacles. 
If there is an obstacle blocking parts of the sky view, the SVF will be greater than 0.

- for SVF = 0 :

    * there is no short-wave reflection
    * there is no long-wave nocturnal interference

According to Oke [#]_, cited by many papers including Hammerle et al. [#]_, the energy budget (in terms of flux) can in this case be considered *ideal* 

.. math:: Q* = Q_G + Q_H + Q_E = 0

Where Q\ :sub:`*`\  is the total energy balance, Q\ :sub:`G`\ is the energy stored in soil and/or buildings, Q\ :sub:`H`\ is the sensible heat (air temperature) and Q\ :sub:`E`\ is the latent heat (evaporated water).

- for SVF > 0 :

    * incoming day-time short-wave reflection increases during the day
    * outgoing night-time long-wave radiation is reduced
    * incoming night-time long-wave radiation is increased
    * altered soil heat flux

.. note:: For more information on th different types of radiation, see :ref:`nightrad`

Because of its influence on energy balances, the SVF holds an importance in various fields of climatology (urban [#]_, forest [#]_, human biometeorology [#]_...) but its most widespread use concerns the heat island phenomena.

.. seealso::
   :ref:`solarpage`
   :ref:`science-behind-iso`

Sky View Factor and Heat Ilsand Phenomena
=========================================

One of the earliest studies demonstrating the link between sky view factor and local urban temperatures was made by Yamashita et al. [#]_ (1985).

.. rubric:: Footnotes 

.. [#] Steyn, D. G. (1980). The calculation of view factors from fisheye‐lens photographs: Research note. Atmosphere-Ocean, 18, 254–258. https://doi.org/10.1080/07055900.1980.9649091
.. [#] MMatzarakis, A., Rutz, F., & Mayer, H. (2007). Modelling radiation fluxes in simple and complex environments: Basics of the RayMan model. International Journal of Biometeorology, 51, 323–334. https://doi.org/10.1007/s00484-006-0061-8
.. [#] Rzepa & Gromk 2006, Gal et al 2007
.. [#] Hämmerle, Gal, Unger, Matzarakis 2001, 
.. [#] Oke, T. R. (1982). The energetic basis of the urban heat island. Quarterly Journal of the Royal Meteorological Society, 108(455), 1–24. https://doi.org/10.1002/qj.49710845502
.. [#] Hämmerle, Gal, Unger, Matzarakis, 2011, Comparison of Models Calculating the Sky View Factor used for Urban Climate Investigations, Theoretical and Applied Climatology, Oct. 2011, Vol. 105, n. 3, pp. 521-527 
.. [#] Watson, I. D., & Johnson, G. T. (1987). Graphical estimation of sky view-factors in urban environments. Journal of Climatology, 7(2), 193–197. https://doi.org/10.1002/joc.3370070210
.. [#] Holmer et al., 2001
.. [#] Matzarakis, 2001
.. [#] Yamashita, 1985, On Relationships Between Heat Ilsand and Sky View Factor in the Cities of Tama River Basin, Japan. Atmopheric Environment Vol. 20, n°4, pp. 681-685 1986 Pergamon Press Ltd.

