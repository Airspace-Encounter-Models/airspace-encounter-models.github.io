---
layout: single
title:  "Airspace Encounter Models Updates - October 2021"
date:   2021-10-01 00:00:00 -0500
categories: update em-model-manned-bayes em-pairing-uncor-importancesampling em-core em-pairing-geospatial
author: Andrew Weinert
toc: true
---
Today we updated four repositories.

<!---
<img src="https://github.com/Airspace-Encounter-Models/em-model-manned-bayes/blob/v2.1.0/doc/model_terminal_traj_fwd.png?raw=true" alt="Terminal forward trajectory model">
-->

# em-model-manned-bayes

Version 2.0 introduces object-oriented programming in MATLAB with a class for a generic encounter model and classes specific to the uncorrelated conventional aircraft and correlated terminal models. These classes enable the user to easily read in the ASCII parameter files with improved input handling. New example run scripts are included to demonstrate how to use the OOP classes. With a few lines of code, the uncorrelated and terminal model can be sampled or generate aircraft trajectories in a local Cartesian coordinate system. The uncorrelated model also supports generating tracks and translating them into a geodetic coordinate system.

{% highlight matlab %}
startup_bayes;
nSamples = 1; % Number of sample / tracks
sample_time = 210; % Duration of each sample / track
mdl = UncorEncounterModel; % Instantiate object
[inits, events, samples, ~] = mdl.sample(nSamples,sample_time); % Sample model
results_neu = mdl.track(nSamples,sample_time,'coordSys','NEU'); % Track in local relative Cartesian coordinate system
results_geo = mdl.track(nSamples,sample_time,'coordSys','geodetic'); % Track in geodetic coordinate system
{% endhighlight %}

Rejection sampling based on speed has also been improved for the uncorrelated encounter model by defining minimum and maximum permitted speeds based on the individual probability distribution of the speed bins, rather than the minimum and maximum speeds of the overall model structure. Additional improvements to rejection sampling are scheduled for a future release.

Classes are not yet available for the RADES-based correlated, ETMS-based due regard, DFDR-based HAA, and most unconventional models.

# em-pairing-uncor-importancesampling

This repository has been updated to use the uncorrelated encounter model class from em-model-manned-bayes. We also moved the 6DOF dynamics simulation to em-core, so that the dynamics simulation can be better leveraged by other encounter model repositories. The update also includes various quality of life updates, such as improved property validation.

# em-core

Version 1.2 now redistributes a third party function, allcomb, to help reduce dependences on MATLAB toolboxes and also an updated 6DOF dynamics simulation originally hosted in em-pairing-uncor-importancesampling. The dynamics simulation now has two additional inputs corresponding to dynamic limit constraints. We updated msl2agl, the function that uses digital elevation models to calculate the mean sea level (MSL) elevation of terrain or estimate the above ground level (AGL) altitude of inputted geodetic coordinates. These changes focus on improving data handling and replacing a function scheduled to be deprecated by Mathworks in the future. Furthermore, a run script has been added to help streamline compiling MATLAB mex functions.

# em-pairing-geospatial

Similar to em-pairing-uncor-importancesampling, this repository was updated to use the uncorrelated encounter model class from em-model-manned-bayes. Pre-generated files of tracks generated from the Bayesian encounter models are no longer required to create encounters; instead, tracks are now generated using the uncorrelated encounter model class at runtime. Additionally, trajectories are now formatted as Matlab Timetables for improved interpolation, smoothing, outlier detection, and time-based sampling. The use of Timetables prompted the removal or modification of functions whose capabilities were deprecated by the built-in capabilities of Timetables.
