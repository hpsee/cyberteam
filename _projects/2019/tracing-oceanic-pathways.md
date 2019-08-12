---
title: Tracing Oceanic Pathways using High Resolution Model Output
image: maine_lighthouse.jpg
tags: []
status: In progress
project_institution: Stonehill College
anchor_institution: MGHPCC
recruiting:  I am open to working with any Cyberteam student that feels that they have the expertise to complete this project. However, a student that has some experience working with Fortran (the LTRANS code is written in Fortran 90) would be beneficial.
owner: kristin-burkholder
mentors: [chris-hill]
students: [nicholas-colella]
email: kburkholder@stonehill.edu
---

The amazingly productive waters of the Gulf of Maine (GOM) support one of the most biodiverse and economically important marine habitats in the world. This productivity relies on adequate concentrations of nutrients being transported into the photic zone during times of the year when significant amounts of sunlight are present. As such, an understanding of the nature and variability of the pathways that deliver nutrients to the photic zone is desirable. Since studying the real ocean is experimentally difficult, models of ocean circulation can provide valuable information to researchers about the nature of ocean circulation. My research relies on using output from one such model, the Regional Ocean Modeling System (ROMS), to investigate nutrient pathways in the GOM and how they are changing as oceanic temperatures warm. In order to study pathways in the ROMS model, my lab makes use of a code called LTRANS (http://northweb.hpl.umces.edu/LTRANS.htm) to launch synthetic "drifters" in the model and to calculate their trajectories through the GOM using the model velocity fields (which vary in time). However, running this code becomes quite time and resource intensive: for each "drifter" launched, the computer must calculate a new position at each time step through the time-varying velocity field. I hope that the Cyberteam will help me to make this process more efficient such that my students and I are able to access the data more easily and run larger numbers of trajectories without being limited by computational power.
