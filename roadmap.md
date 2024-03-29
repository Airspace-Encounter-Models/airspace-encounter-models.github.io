---
title: "The Airspace Encounter Models Roadmap"
permalink: /Roadmap/
layout: single
author_profile: false
toc: true
share: true
---

# Overview

Our roadmap looks out 12-18 months and we establishes topics we intend to work on. We develop it based on the findings we made over the course of the last year, community feedback, and in face-to-face discussions. Discussions with the community were held in December 2022 and January 2023 to inform updates to the roadmap. 

Our roadmap uses the [Visual Studio Code Roadmap as a template](https://github.com/microsoft/vscode/wiki/Roadmap). Since most of the team are staff at [MIT Lincoln Laboratory](https://www.ll.mit.edu/), a federally funded research and development center (FFRDC), execution of this roadmap is dependent on resources and funding provided by MIT Lincoln Laboratory's sponsors, such as the [Federal Aviation Administration (FAA)](https://www.faa.gov/) and [National Aeronautics and Space Administration (NASA)](https://www.nasa.gov/). Please coordinate with Deepak Chauhan from FAA ANG regarding resources provided by the FAA A11L.UAS.2 research task. 

When we execute our roadmap, we keep learning and our assessment of some of the topics listed may change. As a result, we may add or drop topics as we go. After around 12 months we come together to develop the next roadmap.

We describe some initiatives as "investigations" or "explorations" which means our goal in the next few months is to better understand the problem and potential solutions before scheduling actual feature work. Once an investigation is done, we will update our plans, either deferring the initiative or committing to it.

## Legend of annotations

Mark | Description
------------ | -------------
bullet | work not started
check mark | work completed
🏃‍♀️ | on-going work
💪 | stretch goal
🔴 | missing link

## Values

Before we go into the details, let's start with our values that guide development. They have pretty much remained the same since the early days of model development and we don't have any intention to change them.

- Develop comprehensive evaluation capabilities to ensure that remain well clear and collision avoidance systems are safe
- Support the needs of the applicable standards developing organizations, such as [ASTM](https://www.astm.org/) and [RTCA](https://www.rtca.org/), with direction from the Federal Aviation Administration
- Emphasize software to be freely available and easily accessible
- Promote transparency, and reduce barriers to collaboration
- Models should realistically capture relative aircraft geometry and dynamics
- Enable fast-time and big data simulations

## Themes for 2023

For 2023, we'll particularly focus in the following themes.

- Continue on our journey to develop the best statistical models of aircraft behavior for large scale safety simulations
- Promote community development and contributions outside of MIT Lincoln Laboratory
- Improve software and technical documentation
- Reduce dependencies on closed source software or restricted datasets
- Improve DevOps (e.g., [GitHub Actions](https://github.com/features/actions), continuous integration, etc.)
- Focus model development on the complex airspace over metropolitan areas

# DevOps

- [ ] Prototype unit testing using [GitHub actions for MATLAB](https://github.com/matlab-actions)
- [ ] Improve unit testing, including developing across multiple repositories unit tests for the first time
- [ ] In preparation for future Python development, update contributing guidelines with Python specific guidance

# Models

## Design and Training

- [ ] 🏃‍♀️ Expand the scope of the correlated terminal model to support Class B airports and metropolitan airspaces. Specifically, train a Dynamic Bayesian Network to model the geometry of two or more aircraft at the start, conclusion, and closest point of approach of a correlated encounter
- [ ] Release the dataset used to train the updated correlated terminal model, along with supplemental metadata and machine annotated features
- [ ] 🏃‍♀️ Publicly release a prototype MATLAB parser for the [FAA 28 Day NASR subscription](https://www.faa.gov/air_traffic/flight_info/aeronav/Aero_Data/NASR_Subscription/) to support model development and track classification
- [ ] Train a new uncorrelated model of glider aircraft using data collected from the [OpenSky Network](https://opensky-network.org/)
- [ ] 🏃‍♀️ Reduce the [`em-processing-opensky`](https://github.com/Airspace-Encounter-Models/em-processing-opensky) repository dependency on the MATLAB mapping toolbox
- [ ] Streamline relationship and workflow between [`em-download-opensky`](https://github.com/Airspace-Encounter-Models/em-download-opensky) and [`em-processing-opensky`](https://github.com/Airspace-Encounter-Models/em-processing-opensky)
- [ ] Add support for air navigation obstacles identified by the [Irish Aviation Authority (IAA)](https://www.iaa.ie/commercial-aviation/airspace/air-navigation-obstacles)
- [ ] 💪 Add support for long linear infrastructure information provided by [Transpower in New Zealand](https://data-transpower.opendata.arcgis.com/)
- [ ] 💪 Explore support for obstacles and features of interest data provided by [Ordnance Survey Ireland](https://data-osi.opendata.arcgis.com/)
- [ ] 💪 Investigate training a model based on latitude, longitude, and altitude information sourced from imagery metadata in the [Low Altitude Disaster Imagery (LADI) Dataset](https://github.com/ladi-dataset)

## Sampling

- [ ] Release prototype Python code to sample models using [`pgmpy`](https://pgmpy.org/index.html)
- [ ] Release more baseline encounter sets of sampled encounters
- [ ] Publish guidelines and a checklist on how to leverage the encounter models based on best practices established for RTCA and the Department of Defense
- [ ] 🏃‍♀️ Minimize the use of rejection sampling to generate trajectories
- [ ] 🏃‍♀️ Update the `UncorEncounterModel` MATLAB class in [`em-model-manned-bayes`](https://github.com/airspace-Encounter-Models/em-model-manned-bayes) to support unconventional (e.g. balloons, hang gliders, etc.) models
- [ ] 💪 Investigate prototyping a MATLAB class for the helicopter air ambulance uncorrelated model
- [ ] 💪 Investigate prototyping a MATLAB class for the RADES-based correlated en route model

# Install / Update

- [ ] 💪 Improve cross platform XML parsing in shell scripts
- [ ] 💪 Explore containerizing multiple repositories into a single package

# Website

- [ ] 🏃‍♀️ Improve communication of best practices and development updates through blog posts
- [ ] 🏃‍♀️ Refresh technical documentation and remove outdated links
- [ ] 🏃‍♀️ Refresh Zotero [airspace-encounter-models group library](https://www.zotero.org/groups/2359172/airspace-encounter-models/library)
- [ ] Continue to incrementally improve presentation and discoverability
- [ ] Archive and mark for deprecation the `em-overview` repository once the GitHub pages website has been sufficiently updated and established

# Community Support and OSS Project

- [ ] Build a good collection of issues labeled `help wanted` and `good first issue`
- [ ] Update repositories to all have a [`CITATION.cff`](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-citation-files)
