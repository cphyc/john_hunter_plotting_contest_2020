# Rationale

This repository contains my submission for the John Hunter plotting context, 2020 edition. See the abstract bellow for more information.
The dataset used to generate the plots is linked in the jupyter notebook.

# Abstract

It is still unclear where galaxies get their angular momentum from, and whether its value could be predicted from first principles. One difficulty in this problem is that most of the gas falling onto galaxies moves in random directions, so that its overall angular momentum is null.

Some recent research has however shown that amid this apparent randomness, some gas is expected to be accreted along steady flows that are directly aimed towards the forming galaxy. Thanks to their steadiness, they are able to funnel gas coherently over long time scales and are therefore thought to be key to the spinning-up of galaxies. Understanding their time and spatial evolution is therefore key to understand how galaxies form their angular-momentum structures, such as their disk.
In order to study these flows, scientists rely on the fact that they are denser and cooler than their surroundings. Physically, this make them stable enough to withstand the harsh environment surrounding galaxies and directly flow into it without being shock-heated (i.e. they remain cool all the time). This also gives a practical method to detect them: the thermal history of a parcel of gas encodes whether it moved through these flows or not.

This work was carried on using a code (RAMSES) that is able to capture hydrodynamical shocks very accurately, so that the gas dynamics is well described in the flows. I relied on a tracer particle scheme I developed to sample on-the-fly the history of the gas with hundreds of millions of tracer particles. By studying the detailed thermal history of each of these particle, one can then follow these particular flows, showed in the video around a galaxy (at the centre of the view) 1.8Gyr after the Big Bang.

In order to reveal the 3D structure of the flows unequivocally, I implemented a numerical method to cast rays through my dataset which was then plugged into the yt project to create volumetric renderings. The movie showcases here the density (in purple to yellow shades, yellower is denser) and temperature (in blue shades, whiter is cooler) of the gas in these flows.
The striking structure of the flows is revealed, with galaxies (bright yellow spots) being interconnected and fed by large reservoirs of cold gas (white regions) via filamentary structures.

This movie is, to the best of my knowledge, the first volumetric rendering of a RAMSES dataset. Together with the use of tracer particles, it reveals as never before the complex structure of the flows that feed galaxies. The numerical setup presented here will enable astronomers to better understand how the flows interact with galaxies, how their spatial structure evolves with time and in the end, how galaxies acquire their angular momentum.
