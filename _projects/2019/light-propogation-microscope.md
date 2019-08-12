---
title: Light Propagation in a Temporal Focusing Microscope using Matlab
image: light-charging.png
tags: [parallelization, vectorization, site-specific, matlab]
status: New and recruiting
project_institution: Middlebury College
anchor_institution: University of Vermont
recruiting:  The PI has written the wave propagation code in Matlab, and this project needs a student who can transform the calculations to run on a cluster. Because Matlab will also be installed on the cluster, the student will be responsible for developing the workflow for running the simulation on the cluster, as well as to enhance the existing code to take advantage of the cluster’s parallel computing power. The ideal candidate would be an undergraduate student at the PI’s home institution.
owner: michael-durst
mentors: []
students: []
email: mdurst@middlebury.edu
---

Understanding the propagation of light is essential for developing new techniques for biomedical optics. Characterizing the resolution of a microscope requires calculating how light travels through optical elements such as lenses, apertures, and diffraction gratings. This project uses Fourier optics to analyze the propagation of light through a temporal focusing microscope, in which laser pulses pass through a diffraction grating, a collimating lens, and an objective lens on their way to the sample. Because each wavelength can be treated independently, a cluster will perform parallel numerical calculations to reconstruct the light field at the focus of the microscope, allowing for a more complete understanding of how different laser parameters affect the resolution of a temporal focusing microscope.
