---
title: "Technical Documentation"
permalink: /techdoc/
layout: single
author_profile: true
toc: true
---
The encounter models are described in the brief introductory material that follows as well as in comprehensive technical reports.

Generally speaking, there are two types of encounter model: correlated and uncorrelated, where correlation is defined as a statistical dependence between conflicting aircraft due to factors before a collision avoidance system like TCAS or a UAS DAA system acts, modeling at least 60 seconds prior to a closet point of approach. If a sufficient correlation exists, then it must be modeled. One of the main causes of correlation in encounters that must be accounted for in the models is air traffic control; however, air traffic control is not directly applicable to all UAS operational concepts. It is possible that NASA prototype UTM separation services may induce a similar correlation, provided the conflict is made aware to UTM. However as of October 2019, since there are currently no accepted or widely operational UTM services, encounters with sUAS are assumed to be uncorrelated.

Citations are listed in descending chronological order, which the newest entries listed first. Clicking the arrow next the citation will display the Bibtex entry for each citation. Each Bibtex entry includes a URL to access the citation. All citations can also be found in the Zotero group, [airspace-encounter-model](https://www.zotero.org/groups/2359172/airspace-encounter-models/items).

With the exception of the uncorrelated UAS model, each encounter model of manned aircraft is a Bayesian Network, a representation of a multivariate probability distribution as a directed acyclic graph and trained using aircraft operational data derived from radar or other sensing system flight track data. With the exception of the unmanned recreational model and urban air mobility uncorrelated model which were developed in collaboration with Stanford University, all these models were originally developed by MIT Lincoln Laboratory.

# Introductory

<details> <summary> M. J. Kochenderfer, M. W. M. Edwards, L. P. Espindle, J. K. Kuchar, and J. D. Griffith, “Airspace Encounter Models for Estimating Collision Risk,” Journal of Guidance, Control, and Dynamics, vol. 33, no. 2, pp. 487–499, Apr. 2010.</summary>
<p>

{% highlight tex %}
@article{kochenderferAirspaceEncounterModels2010,
	title = {Airspace {Encounter} {Models} for {Estimating} {Collision} {Risk}},
	url = {https://doi.org/10.2514/1.44867},
	volume = {33},
	doi = {10.2514/1.44867},
	number = {2},
	journal = {Journal of Guidance, Control, and Dynamics},
	author = {Kochenderfer, Mykel J. and Edwards, Matthew W. M. and Espindle, Leo P. and Kuchar, James K. and Griffith, J. Daniel},
	month = apr,
	year = {2010},
	pages = {487--499}
}
{% endhighlight %}
</p>
</details>

<details> <summary> M. J. Kochendedrfer, L. P. Espindle, J. K. Kuchar, and J. D. Griffith, “A Comprehensive Aircraft Encounter Model of the National Airspace System,” Lincoln Laboratory Journal, vol. 17, no. 2, pp. 41–53, 2008.</summary>
<p>

{% highlight tex %}
@article{kochendedrferComprehensiveAircraftEncounter2008,
	title = {A {Comprehensive} {Aircraft} {Encounter} {Model} of the {National} {Airspace} {System}},
	volume = {17},
	url = {https://pdfs.semanticscholar.org/4086/9e6358bded8c07a7e5480facee4223fa0a29.pdf},
	language = {en},
	number = {2},
	journal = {Lincoln Laboratory Journal},
	author = {Kochendedrfer, Mykel J. and Espindle, Leo P. and Kuchar, James K. and Griffith, J. Daniel},
	year = {2008},
	pages = {41--53}
}
{% endhighlight %}
</p>
</details>
<br>

# Manned Aircraft

## Manned Correlated Extended Model

Bayesian network model trained on observed encounters between transponder-equipped (cooperative) aircraft. The training data were processed pairs of tracks of aircraft equipped with mode [Mode 3A/C](https://en.wikipedia.org/wiki/Air_traffic_control_radar_beacon_system) transponders and observed by one of over 200 ground-based primary and secondary surveillance radars managed by the RADES. The extended correlated model was trained from more than 500,000 flight hours from cooperative aircraft, and the extended uncorrelated from more than 290,000 flight hours of 1200-code aircraft.

<details> <summary> N. Underhill, E. Harkleroad, R. Guendel, D. Maki, and M. Edwards, “Correlated Encounter Model for Cooperative Aircraft in the National Airspace System; Version 2.0,” Massachusetts Institute Technology Lincoln Laboratory Lexington United States, May 2018.</summary>
<p>

{% highlight tex %}
@techreport{underhillCorrelatedEncounterModel2018,
  title = {Correlated {Encounter Model} for {Cooperative Aircraft} in the {National Airspace System}; {Version} 2.0},
  url = {https://apps.dtic.mil/docs/citations/AD1051496},
  author = {Underhill, N.K and Harkleroad, E.P and Guendel, R.E and Weinert, A.J and Maki, D.E and Edwards, M.W.M},
  type = {Project {{Report}}},
  language = {en},
  number = {ATC-440},
  institution = {Massachusetts Institute of Technology, Lincoln Laboratory},
  month = may,
  year = {2018},
  pages = {140}
}
{% endhighlight %}
</p>
</details>

<details> <summary> M. J. Kochenderfer, L. P. Espindle, J. K. Kuchar, and J. D. Griffith, “Correlated Encounter Model for Cooperative Aircraft in the National Airspace System,” Massachusetts Institute of Technology, Lincoln Laboratory, Project Report ATC-344, 2008.</summary>
<p>

{% highlight tex %}
@techreport{kochenderferCorrelatedEncounterModel2008,
	title = {Correlated {Encounter} {Model} for {Cooperative} {Aircraft} in the {National} {Airspace} {System}},
	url = {https://www.ll.mit.edu/r-d/publications/correlated-encounter-model-cooperative-aircraft-national-airspace-system-version},
	type = {Project {Report}},
	number = {ATC-344},
	institution = {Massachusetts Institute of Technology, Lincoln Laboratory},
	author = {Kochenderfer, M. J. and Espindle, Leo P. and Kuchar, James K. and Griffith, J. D.},
	year = {2008}
}
{% endhighlight %}
</p>
</details>

## Manned Correlated Terminal Model

A set of Bayesian networks tailored to address structured terminal operations, i.e., correlations between trajectories and the airfield and each other. It was specifically trained to support [RTCA SC-228](https://www.rtca.org/sc-228/) development of the [DO-365](https://my.rtca.org/nc__store?search=do-365) minimum operational performance standard (MOPS). The model is comprised to two main elements. The first component, the encounter geometry model, describes the geometrical conditions of two encounter aircraft at their point of closest approach. The second component, the trajectory generation model, then describes the flight path for each aircraft leading to and continuing from their point of closest approach.

<details> <summary> A. Weinert, N. Underhill, C. Serres, and R. Gundel, “Correlated Bayesian Model of Aircraft Encounters in the Terminal Area Given a Straight Takeoff or Landing,” Preprints, 2021.</summary>
<p>

{% highlight tex %}
@article{weinert2021correlated,
  title={Correlated Bayesian Model of Aircraft Encounters in the Terminal Area Given a Straight Takeoff or Landing},
  author={Weinert, Andrew and Underhill, Ngaire and Serres, Christine and Guendel, Randal},
  year={2021},
  doi={10.20944/preprints202111.0051.v1},
  url={https://www.preprints.org/manuscript/202111.0051/v1},
  publisher={Preprints}
}
{% endhighlight %}
</p>
</details>

## Manned Due Regard

A Bayesian network trained using using the ETMS data feed that was provided by the [Volpe Center](https://www.volpe.dot.gov/) to describe aircraft operating in international airspace. Training data included operations over the Atlantic and Pacific oceans and consisted of over 10,000 flight hours.

<details> <summary> J. D. Griffith, M. W. Edwards, R. M. Miraflor, and A. J. Weinert, “Due Regard Encounter Model Version 1.0,” Massachusetts Institute of Technology, Lincoln Laboratory, Lexington, MA, Project Report ATC-397, Aug. 2013.</summary>
<p>

{% highlight tex %}
@techreport{griffithDueRegardEncounter2013,
	title = {Due {Regard} {Encounter} {Model} {Version} 1.0},
	address = {Lexington, MA},
	type = {Project {Report}},
	number = {ATC-397},
	institution = {Massachusetts Institute of Technology, Lincoln Laboratory},
	author = {Griffith, John D. and Edwards, Matthew W. and Miraflor, Raymond M. and Weinert, Andrew J.},
	month = aug,
	year = {2013},
	url = {https://apps.dtic.mil/docs/citations/ADA589692},
	pages = {56}
}
{% endhighlight %}
</p>
</details>

## Manned Helicopter Air Ambulance Model

A Bayesian network trained from an estimated 2,526,000 observations across 758 flight hours. The training observations were sourced from FOQA DFDR data provided by a Massachusetts-based HAA provider. This model should only be used to simulate HAA rotorcraft operations, it has not been validated to be representative of other rotorcraft operations.

*Note a technical description of this model has not been publicly released yet. This model was developed to support sUAS well clear research. Until model-specific documentation is released, please cite the following paper.*

<details> <summary> A. Weinert, S. Campbell, A. Vela, D. Schuldt, and J. Kurucar, “Well-Clear Recommendation for Small Unmanned Aircraft Systems Based on Unmitigated Collision Risk,” Journal of Air Transportation, vol. 26, no. 3, pp. 113–122, 2018.</summary>
<p>

{% highlight tex %}
@article{weinertWellClearRecommendationSmall2018,
	title = {Well-{Clear} {Recommendation} for {Small} {Unmanned} {Aircraft} {Systems} {Based} on {Unmitigated} {Collision} {Risk}},
	volume = {26},
	url = {https://doi.org/10.2514/1.D0091},
	doi = {10.2514/1.D0091},
	number = {3},
	urldate = {2019-01-09},
	journal = {Journal of Air Transportation},
	author = {Weinert, Andrew and Campbell, Scot and Vela, Adan and Schuldt, Dieter and Kurucar, Joel},
	year = {2018},
	pages = {113--122}
}
{% endhighlight %}
</p>
</details>

## Manned Uncorrelated-Conventional Models

Uncorrelated models assume aircraft behavior is not dependent on air traffic services or nearby aircraft. While trained using observations of cooperative aircraft equipped with transponders, they are often used as surrogates to model noncooperative aircraft not equipped with transponders. Uncorrelated models have been trained using either observations of 1200-code aircraft equipped with [Mode 3A/C](https://en.wikipedia.org/wiki/Air_traffic_control_radar_beacon_system) transponders observed by a radar managed by the RADES or from observations by the [OpenSky Network](https://github.com/openskynetwork) of [ADS-B](https://www.faa.gov/nextgen/programs/adsb/) equipped aircraft.

*Note that Appendix C in CASSATT-2 describes a revised process from the early encounter models for initializing uncorrelated encounters and estimating metrics.*

<details> <summary> N. Underhill, and A. Weinert, "Applicability and Surrogacy of Uncorrelated Airspace Encounter Models at Low Altitudes." Journal of Air Transportation, 2021, pp. 1-5, doi: 10.1109/HPEC43674.2020.9286229.</summary>
<p>

{% highlight tex %}
@article{underhill2021applicability,
  title={Applicability and Surrogacy of Uncorrelated Airspace Encounter Models at Low Altitudes},
  author={Underhill, Ngaire and Weinert, Andrew},
  journal={Journal of Air Transportation},
  volume = {29},
  number = {3},
  pages = {137-141},
  year = {2021},
  publisher={American Institute of Aeronautics and Astronautics},
  url={https://doi.org/10.2514/1.D0254},
  doi={10.2514/1.D0254}
}
{% endhighlight %}
</p>
</details>

<details> <summary> A. Weinert, N. Underhill, B. Gill, and A. Wicks, “Processing of Crowdsourced Observations of Aircraft in a High Performance Computing Environment,”2020 IEEE High Performance Extreme Computing Conference (HPEC), 2020, pp. 1-6, doi: 10.1109/HPEC43674.2020.9286229.</summary>
<p>

{% highlight tex %}
@article{weinertProcessingCrowdsourcedObservations2020,
	author={Weinert, Andrew and Underhill, Ngaire and Gill, Bilal and Wicks, Ashley},
  	booktitle={2020 IEEE High Performance Extreme Computing Conference (HPEC)}, 
  	title={Processing of Crowdsourced Observations of Aircraft in a High Performance Computing Environment}, 
  	year={2020},
  	volume={},
  	number={},
  	pages={1-6},
  	doi={10.1109/HPEC43674.2020.9286229}}
}
{% endhighlight %}
</p>
</details>

<details> <summary> A. Weinert, N. Underhill, and A. Wicks, “Developing a Low Altitude Manned Encounter Model Using ADS-B Observations,” in 2019 IEEE Aerospace Conference, Big Sky, MT, 2019, pp. 1-8, doi: 10.1109/AERO.2019.8741848.</summary>
<p>

{% highlight tex %}
@inproceedings{weinertDevelopingLowAltitude2019,
	title = {Developing a {Low} {Altitude} {Manned} {Encounter} {Model} {Using} {ADS}-{B} {Observations}},
	url = {https://doi.org/10.1109/AERO.2019.8741848},
	doi = {10.1109/AERO.2019.8741848},
	address = {Big Sky, MT},
	language = {en},
	title={Developing a Low Altitude Manned Encounter Model Using ADS-B Observations}, 
	author = {Weinert, Andrew and Underhill, Ngaire and Wicks, Ashley},
	month = mar,
	year = {2019},
	pages = {1--8}
}
{% endhighlight %}
</p>
</details>

<details> <summary> A. J. Weinert, E. P. Harkleroad, J. D. Griffith, M. W. Edwards, and M. J. Kochenderfer, “Uncorrelated Encounter Model of the National Airspace System Version 2.0,” Massachusetts Institute of Technology, Lincoln Laboratory, Lexington, MA, Project Report ATC-404, Aug. 2013.</summary>
<p>

{% highlight tex %}
@techreport{weinertUncorrelatedEncounterModel2013,
	address = {Lexington, MA},
	type = {Project {Report}},
	title = {Uncorrelated {Encounter} {Model} of the {National} {Airspace} {System} {Version} 2.0},
	copyright = {All rights reserved},
	number = {ATC-404},
	institution = {Massachusetts Institute of Technology, Lincoln Laboratory},
	author = {Weinert, Andrew J. and Harkleroad, Eric P. and Griffith, John D. and Edwards, Matthew W. and Kochenderfer, Mykel J.},
	month = aug,
	url = {https://apps.dtic.mil/docs/citations/ADA589697},
	year = {2013},
	pages = {93}
}
{% endhighlight %}
</p>
</details>

<details> <summary> A. J. Weinert, E. Harkleroad, J. Griffith, M. W. Edwards, and C. C. Chen, “Extended Airspace Encounter Models for Unmanned Aircraft Sense and Avoid Safety Evaluation,” in AIAA Infotech@Aerospace (I@A) Conference, Boston, MA, 2013.</summary>
<p>

{% highlight tex %}
@inproceedings{weinertExtendedAirspaceEncounter2013,
	address = {Boston, MA},
	title = {Extended {Airspace} {Encounter} {Models} for {Unmanned} {Aircraft} {Sense} and {Avoid} {Safety} {Evaluation}},
	url = {http://arc.aiaa.org/doi/abs/10.2514/6.2013-5049},
	doi = {10.2514/6.2013-5049},
	urldate = {2013-08-23},
	booktitle = {AIAA {Infotech}@{Aerospace} ({I}@{A}) {Conference}},
	publisher = {American Institute of Aeronautics and Astronautics},
	author = {Weinert, Andrew J. and Harkleroad, Eric and Griffith, John and Edwards, Matthew W. and Chen, Christine C.},
	month = aug,
	year = {2013}
}
{% endhighlight %}
</p>
</details>

<details> <summary> M. W. Edwards, “Encounter Models for the Littoral Regions of the National Airspace System” Massachusetts Institute of Technology, Lincoln Laboratory, CASSATT-2, Sep. 2010.</summary>
<p>

{% highlight tex %}
@techreport{edwardsEncounterModelsLittoral2010,
	title = {Encounter {Models} for the {Littoral} {Regions} of the {National} {Airspace} {System}},
	url = {https://apps.dtic.mil/docs/citations/ADA529083},
	language = {en},
	number = {CASSATT-2},
	urldate = {2019-01-16},
	institution = {Massachusetts Institute of Technology, Lincoln Laboratory},
	author = {Edwards, Matthew W.},
	month = sep,
	year = {2010}
}
{% endhighlight %}
</p>
</details>

<details> <summary> M. J. Kochenderfer, J. K. Kuchar, L. P. Espindle, and J. D. Griffith, “Uncorrelated Encounter Model of the National Airspace System version 1.0,” MIT Lincoln Laboratory, Lexington, Massachusetts, Project Report ATC-345, 2008.</summary>
<p>

{% highlight tex %}
@techreport{kochenderferUncorrelatedEncounterModel2008,
	type = {Project {Report}},
	title = {Uncorrelated {Encounter} {Model} of the {National} {Airspace} {System} version 1.0},
	number = {ATC-345},
	institution = {Massachusetts Institute of Technology, Lincoln Laboratory},
	author = {Kochenderfer, M. J. and Kuchar, J. K. and Espindle, L. P. and Griffith, J. D.},
	url = {https://www.ll.mit.edu/r-d/publications/uncorrelated-encounter-model-national-airspace-system-version-10},
	year = {2008}
}
{% endhighlight %}
</p>
</details>

## Manned Uncorrelated-Unconventional Model

A set of nine individual Bayesian network models encompassing ultralights, gliders, balloons, and airships. This model is based on more than 96,000 unconventional aircraft tracks. These models were developed developed in response to the uncorrelated-conventional model not being sufficiently representative all types of noncooperative aircraft.

<details> <summary> M. W. Edwards, M. J. Kochendedrfer, J. K. Kuchar, and L. P. Espindle, “Encounter Models for Unconventional Aircraft, Version 1.0,” Massachusetts Institute of Technology, Lincoln Laboratory, Project Report ATC-348, 2009.</summary>
<p>

{% highlight tex %}
@techreport{edwardsEncounterModelsUnconventional2009,
	type = {Project {Report}},
	title = {Encounter {Models} for {Unconventional} {Aircraft}, {Version} 1.0},
	number = {ATC-348},
	institution = {Massachusetts Institute of Technology, Lincoln Laboratory},
	author = {Edwards, Matthew W. and Kochendedrfer, Mykel J. and Kuchar, James K. and Espindle, Leo P.},
	url = {https://www.ll.mit.edu/r-d/publications/encounter-models-unconventional-aircraft-version-10},
	year = {2009}
}
{% endhighlight %}
</p>
</details>
<br>

# Unmanned Aircraft

## Unmanned Uncorrelated Model

This discriminative model takes into account the operational intent of UAS commercial operations and generates trajectories based on open source maps of infrastructure, recreational regions, and other common sUAS surveillance targets. This model is not a generative Bayesian Network like the others.
  
This model is applicable for some commercial operations, such as long linear infrastructure inspection, governed by 14 CFR Part 107 (sUAS rule) or 14 CFR Part 135 (air carrier). It is not applicable for sUAS recreational and amateur operations governed by 14 CFR Part 101 or 49 U.S.C. 44809.

<details> <summary> A. J. Weinert, M. Edwards, L. Alvarez, and S. M. Katz, “Representative Small UAS Trajectories for Encounter Modeling,” presented at the AIAA Scitech 2020 Forum, Orlando, FL, Jan. 2020.</summary>
<p>

{% highlight tex %}
@inproceedings{weinertRepresentativeSmallUAS2020,
  url = {https://doi.org/10.2514/6.2020-0741},
  address = {Orlando, FL},
  title = {Representative {Small UAS Trajectories} for {Encounter Modeling}},
  booktitle = {AIAA Scitech 2020 Forum},
  publisher = {American Institute of Aeronautics and Astronautics},
  doi = {10.2514/6.2020-0741},
  author = {Weinert, Andrew J. and Edwards, Matthew and Alvarez, Luis and Katz, Sydney Michelle},
  month = jan,
  year = {2020}
}

{% endhighlight %}
</p>
</details>

<details> <summary> A. Weinert and N. Underhill, “Generating Representative Small UAS Trajectories using Open Source Data,” in 2018 IEEE/AIAA 37th Digital Avionics Systems Conference (DASC), 2018, pp. 1–10.</summary>
<p>

{% highlight tex %}
@inproceedings{weinertGeneratingRepresentativeSmall2018,
	title = {Generating {Representative} {Small} {UAS} {Trajectories} using {Open} {Source} {Data}},
	url = {https://ieeexplore.ieee.org/document/8569745},
	doi = {10.1109/DASC.2018.8569745},
	booktitle = {2018 {IEEE}/AIAA 37th {Digital} {Avionics} {Systems} {Conference} ({DASC})},
	author = {Weinert, Andrew and Underhill, Ngaire},
	month = sep,
	year = {2018},
	keywords = {Aircraft, Atmospheric modeling, FAA, Monte Carlo methods, Standards, Surveillance, Trajectory},
	pages = {1--10}
}
{% endhighlight %}
</p>
</details>

## Unmanned Recreational Model

A Bayesian network model trained on data from DroneShare, which was a website in which hobbyists could upload their telemetry log files. DroneShare is no longer active but data for download by the public was previously avaiable for over 75,000 flights.

<details> <summary>  Eric R Mueller and Mykel J Kochenderfer. Simulation comparison of collision avoidancealgorithms for small multi-rotor aircraft. In AIAA Modeling and Simulation Technologies Conference, page 3674, 2016.</summary>
<p>

{% highlight tex %}
@inproceedings{mueller2016simulation,
  title={Simulation Comparison of Collision Avoidance Algorithms for Small Multi-Rotor Aircraft},
  author={Mueller, Eric R and Kochenderfer, Mykel J},
  booktitle={AIAA Modeling and Simulation Technologies Conference},
  pages={3674},
  year={2016}
}
{% endhighlight %}

</p>
</details>

<details> <summary>   Eric  R.  Mueller. Multi-rotor  aircraft  collision  avoidance  using  partially  observable Markov decision processes.  PhD thesis, Stanford University, 2016. </summary>
<p>

{% highlight tex %}
@PhdThesis{Mueller2016thesis,
Title = {Multi-rotor aircraft collision avoidance using partially observable {M}arkov decision processes},
Author = {Mueller, Eric R.},
School = {Stanford University},
Year = {2016},
Url = {http://purl.stanford.edu/rv444dz2833}
}
{% endhighlight %}

</p>
</details>

## Urban Air Mobility Uncorrelated Model

Model for Urban Air Mobility (UAM) trajectories at low altitudes (mostly takeoff and landing trajectories). Trajectories are generated by sampling trajectory features and using them to constain a convex optimization problem that selects the position at each time step.

# Encounter Categories

This section describes the different encounter categories when pairing trajectories from the models. Generally speaking, encounters can be correlated (e.g. ATC involvement) or uncorrelated (e.g. aircraft blunder into close proximity).

This section describes the encounter categories for different pairing of aircraft. The first column denotes the aircraft of interest (ownship) while the first row denotes the intruder aircraft. These are the primary encounter categories:

- C = correlated, assumes ATC involvement
- D = uncorrelated, due regard oceanic state aircraft without ATC involvement
- U = uncorrelated aircraft likely equipped with transponders but without ATC involvement
- V = uncorrelated unconventional aircraft likely without transponders and without ATC involvement
- X = not required or applicable
- ? = unknown, in development or has not been defined

## Manned vs Manned

&nbsp; | Discrete code | 1200 Mode C / VFR | Noncooperative conventional | Noncooperative Unconventional | Helicopter Air Ambulance | UAM
:---  | :---:  | :---:  | :---:  | :---:  | :---: | :---:
**Discrete code / IFR** | C | C | U | V | C | ?
**1200 Mode C / VFR** | C | U | U | V | U | ?
**Due Regard** | U | U | U | V | X | ?
**UAM** | ? | ? | ? | ? | ? | ?

## Unmanned vs Manned

&nbsp; | Discrete code | 1200 Mode C / VFR | Noncooperative conventional | Noncooperative Unconventional | Helicopter Air Ambulance | UAM
:---  | :---:  | :---:  | :---:  | :---:  | :---: | :---:
**sUAS - Commercial** | ? | U | U | V | U | ?
**sUAS - Recreational** | ? | U | U | U | U | ?
**UAM** | ? | ? | ? | ? | ? | ?

## Unmanned vs Unmanned

The aviation community is currently focused on enabling UAS airspace integration and unmanned vs manned encounters.
