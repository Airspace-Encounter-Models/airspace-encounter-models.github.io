---
layout: single
title:  "Airspace Encounter Models Updates - July 2021"
date:   2021-07-19 00:00:00 -0500
categories: update em-model-geospatial em-model-manned-bayes em-pairing-uncor-importancesampling em-core degas-surveillance-jwandrews
author: Andrew Weinert
toc: true
---
Today we released two new repositories and significantly updated three others.

<!---
# <img src="https://github.com/Airspace-Encounter-Models/em-model-geospatial/blob/v1.0/doc/patterns.gif?raw=true" alt="patterns">
-->

# em-model-geospatial 🆕

A new release of MATLAB code to generate representative UAS trajectories based on open source geospatial features, such as those provided by OpenStreetMap, Natural Earth Data, the Energy Information Administration (EIA), United States Geological Survey (USGS), or Department of Homeland Security (DHS).

Our overall objective for this repository was the development of low altitude unmanned and manned aircraft encounter models to support DAA research. A public, easily accessible corpus of UAS trajectories, however, is not available since beyond visual line of sight (BVLOS) operations are not routine and there is a lack of reporting requirements. Therefore, we seek to generate representative BVLOS UAS trajectories without actual UAS flights as training data. Development is ongoing and future updates to this software are expected. This software is in the open beta / preview stage. Documentation will be a focus in future releases.

# em-model-manned-bayes

Version 1.4 brings a variety of performance improvements and introduces the correlated terminal encounter models based on terminal area radar or OpenSky Network processed tracks. Software to sample the terminal model is scheduled for an upcoming release.

# em-pairing-uncor-importancesampling

Version 1.2 is centered on a substantial performance boost. On a local windows machine, these improvements reduce the time to generate 100,000 encounters from days to hours. This release also adds basic performance benchmarking, improved repository management, and more robust cross-platform combability.

# em-core

Version 1.1 includes support for additional open datasets and more capabilities related to generating and using spatial boundaries. Similar to the other repositories, this release includes improved performance when using digital elevation models.

# degas-surveillance-jwandrews 🆕

A companion project to the airspace encounter models is the DAA Evaluation of Guidance, Alerting, and Surveillance (DEGAS) simulation framework created by MIT LL to perform simulations of Detect and Avoid (DAA) Systems. [DEGAS](https://github.com/mit-ll/degas-core) can be used to create an end-to-end simulation of typically two aircraft using MATLAB/Simulink. As part of the framework, this new repository contains the class, Simulink Model, and unit test for a surveillance model based on the J.W. Andrews mathematical model of air-to-air visual acquisition under daylight conditions. Starting in 2021, MIT Lincoln Laboratory and the FAA Center of Excellence for UAS Research, [ASSURE](https://www.assureuas.org/) are conducting research to enhance, update, and refine the visual acquisition model. Research includes investigating the assumptions of the model to determine if the original assumptions were overly optimistic or pessimistic about human pilot visual acquisition performance.
