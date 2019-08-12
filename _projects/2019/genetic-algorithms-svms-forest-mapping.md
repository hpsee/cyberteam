---
title: Genetic Algorithms and Support Vector Machines in Forest Mapping
image: blurb_figure.png
tags: [machine learning, matlab, programming]
status: Complete
project_institution: University of Maine
anchor_institution: University of Maine
recruiting:  An undergraduate student with familiarity with Matlab, C, and High Performance Computing
owner: kasey-legaard
mentors: [chris-wilson, larry-whitsel]
students: [noah-howard]
email: kasey.legaard@maine.edu
---

Satellite-derived maps of forest conditions play diverse roles in research and resource management. Maps provide a basis for planning and executing field studies, developing and calibrating models, quantifying ecosystem processes or services, and evaluating environmental change. Natural resource managers use maps to characterize resource conditions, project changes, and direct management actions. However, inferences and decisions must be made within the context of map error, and methods used to produce maps generally result in patterns of error that are potentially detrimental. The researcher has developed machine learning techniques that effectively reduce undesirable systematic error when mapping forest attributes from satellite imagery and geospatial data. The approach is based on support vector machines using a multi-objective genetic algorithm (GA) designed to simultaneously minimize both total and systematic error. Using this approach, we have mapped tree species abundance and forest disturbance across northern Maine, obtaining outcomes that compare well against other approaches previously applied either regionally or nationally. Our algorithms are, however, computationally demanding, and large-scale applications will require more effective use of computing resources. The purpose of this project is to develop software that enables statewide and regional application of our algorithms through enhanced parallelization and new approaches to coordinate and accelerate the convergence of GAs operating across multiple, geographically distributed problem sets defined by input spatial data. We will specifically develop techniques for sharing prospective solutions between GAs executing on adjacent spatial data tiles, mimicking migration of individuals between locally adaptive subpopulations. Algorithm improvements will be coupled with more efficient and more automated methods for input and output data handling. The primary project outcome will be software that supports locally adaptive mapping of forest resources and environmental conditions across large spatial scales through innovative algorithms and efficient use of available cyberinfrastructure.
