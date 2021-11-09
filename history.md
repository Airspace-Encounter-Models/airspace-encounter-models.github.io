---
title: "History"
permalink: /history/
layout: single
author_profile: true
toc: true
---
A historical perspective and example applications of the encounter models for the TCAS and UAS well clear are presented here.

Clicking the arrow next the citation will display the Bibtex entry for each citation. Each Bibtex entry includes a URL to access the citation. All citations can also be found in the Zotero group, [airspace-encounter-model](https://www.zotero.org/groups/2359172/airspace-encounter-models/items).

# Historical Perspective

Airspace encounter models have evolved significantly over the past 35 years. Starting in the 1980s with a model of aircraft equipped with transponders that are cooperatively sharing information and allowed only two-dimensional (vertical plane motion). It was built by the MITRE Corporation from 12 radar sites and supported the development and certification of the TCAS. The 1990s saw the International Civil Aviation Organization (ICAO) and Eurocontrol and lead development of simplified models with three-dimensional motion. Notably, the lowest altitude considered by the Eurocontrol model version 2.1 was 1,000-5,000 ft. AGL. This was indicative of the encounter models support for large manned aircraft avoidance.

The next major encounter model advancement started in 2006, with recognizing the need for three-dimension models with multiple acceleration points to support manned and unmanned safety analysis. In response starting in 2008, MIT Lincoln Laboratory started developing more advanced encounter models to represent a wider range of encounters.

<img src="/assets/images/encountermodelhistory.png" alt="Encounter model history">

The following are recommended seminal citations for  the original encounter model development in the 1980s up to the early 2000s, immediately prior to the development of the MIT Lincoln Laboratory encounters models.

<details> <summary> A. Zeitlin, A. Lacher, J. Kuchar, and A. Drumm, “Collision Avoidance for Unmanned Aircraft: Proving the Safety Case,” The MITRE Corporation and Massachusetts Institute of Technology, Lincoln Laboratory, MP-060219, Oct. 2006.</summary>
<p>

{% highlight tex %}
@techreport{zeitlinCollisionAvoidanceUnmanned2006,
	title = {Collision {Avoidance} for {Unmanned} {Aircraft}: {Proving} the {Safety} {Case}},
	shorttitle = {Collision {Avoidance} for {Unmanned} {Aircraft}},
	url = {https://apps.dtic.mil/docs/citations/ADA474336},
	language = {en},
	number = {MP-060219},
	urldate = {2019-01-16},
	institution = {The MITRE Corporation and Massachusetts Institute of Technology, Lincoln Laboratory},
	author = {Zeitlin, Andrew and Lacher, Andrew and Kuchar, James and Drumm, Ann},
	month = oct,
	year = {2006},
	pages = {12}
}
{% endhighlight %}
</p>
</details>

<details> <summary> T. Miquel and K. Thierry, “European Encounter Model: specifications and probability tables,” CENA/Sofréavia and QinetiQ, Technical Report ACASA/WP1/186 version 2.1, Dec. 2001.</summary>
<p>

{% highlight tex %}
@techreport{miquelEuropeanEncounterModel2001,
	type = {Technical {Report}},
	title = {European {Encounter} {Model}: specifications and probability tables},
	number = {ACASA/WP1/186 version 2.1},
	institution = {CENA/Sofréavia and QinetiQ},
	author = {Miquel, Thierry and Thierry, Kevin},
	month = dec,
	year = {2001}
}
{% endhighlight %}
</p>
</details>

<details> <summary> M. P. McLaughlin, “Safety study of the Traffic Alert and Collision Avoidance System (TCAS II),” MITRE Corporation, MITRE Technical Report MTR 97W32, Jun. 1997.</summary>
<p>

{% highlight tex %}
@techreport{mclaughlinSafetyStudyTraffic1997,
	type = {MITRE {Technical} {Report}},
	title = {Safety study of the {Traffic} {Alert} and {Collision} {Avoidance} {System} ({TCAS} {II})},
	number = {MTR 97W32},
	institution = {MITRE Corporation},
	author = {McLaughlin, Michael P.},
	month = jun,
	year = {1997}
}
{% endhighlight %}
</p>
</details>

<details> <summary> J. Lebron, “System Safety Study of Minimum TCAS II,” The MITRE Corporation, Final Report MTR-83W241, Dec. 1983.</summary>
<p>

{% highlight tex %}
@techreport{lebronSystemSafetyStudy1983,
	type = {Final {Report}},
	title = {System {Safety} {Study} of {Minimum} {TCAS} {II}},
	url = {https://apps.dtic.mil/docs/citations/ADA138674},
	number = {MTR-83W241},
	institution = {The MITRE Corporation},
	author = {Lebron, John},
	month = dec,
	year = {1983},
	pages = {376}
}
{% endhighlight %}
</p>
</details>
<br>

# Well Clear for UAS

The UAS ExCOM SARP supported the initial development of the discriminative uncorrelated UAS model to support sUAS research, while also primarily leveraging the predating uncorrelated manned model. The SARP paired and simulated the UAS with manned aircraft trajectories, sampled from the manned models, to evaluate various candidates and subsequently recommend quantitative means to remain well clear for sUAS. These recommendations have been transitioned to standards developing organizations for when considering tactical DAA performance requirements.

<details> <summary> E. T. Lester and A. Weinert, “Three Quantitative Means to Remain Well Clear for Small UAS in the Terminal Area,” in 2019 Integrated Communications, Navigation and Surveillance Conference (ICNS), Herndon, VA, USA, USA, 2019, pp. 1–17.</summary>
<p>

{% highlight tex %}
@inproceedings{lesterThreeQuantitativeMeans2019,
	address = {Herndon, VA, USA},
	title = {Three {Quantitative} {Means} to {Remain} {Well} {Clear} for {Small} {UAS} in the {Terminal} {Area}},
	url = {https://doi.org/10.1109/ICNSURV.2019.8735171},
	doi = {10.1109/ICNSURV.2019.8735171},
	booktitle = {2019 {Integrated} {Communications}, {Navigation} and {Surveillance} {Conference} ({ICNS})},
	author = {Lester, Edward Ted and Weinert, Andrew},
	month = apr,
	year = {2019},
	pages = {1--17}
}
{% endhighlight %}
</p>
</details>

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

<details> <summary> S. P. Cook, D. Brooks, R. Cole, D. Hackenberg, and V. Raska, “Defining Well Clear for Unmanned Aircraft Systems,” in AIAA Infotech @ Aerospace, Kissimmee, Florida, 2015.</summary>
<p>

{% highlight tex %}
@inproceedings{cookDefiningWellClear2015,
	address = {Kissimmee, Florida},
	series = {AIAA {SciTech} {Forum}},
	title = {Defining {Well} {Clear} for {Unmanned} {Aircraft} {Systems}},
	url = {https://arc.aiaa.org/doi/10.2514/6.2015-0481},
	doi = {10.2514/6.2015-0481},
	urldate = {2019-01-09},
	booktitle = {AIAA {Infotech} @ {Aerospace}},
	publisher = {American Institute of Aeronautics and Astronautics},
	author = {Cook, Stephen P. and Brooks, Dallas and Cole, Rodney and Hackenberg, Davis and Raska, Vincent},
	month = jan,
	year = {2015}
}
{% endhighlight %}
</p>
</details>

<br>
Other well clear efforts that also leveraged the encounter models include the following:

<details> <summary> C. Chen et al., “Defining Well Clear Separation for Unmanned Aircraft Systems Operating with Noncooperative Aircraft,” in AIAA Aviation 2019 Forum, Dallas, Texas, 2019.</summary>
<p>

{% highlight tex %}
@inproceedings{chenDefiningWellClear2019,
	address = {Dallas, Texas},
	title = {Defining {Well} {Clear} {Separation} for {Unmanned} {Aircraft} {Systems} {Operating} with {Noncooperative} {Aircraft}},
	url = {https://arc.aiaa.org/doi/abs/10.2514/6.2019-3512},
	doi = {10.2514/6.2019-3512},
	language = {en},
	urldate = {2019-08-20},
	booktitle = {AIAA {Aviation} 2019 {Forum}},
	publisher = {American Institute of Aeronautics and Astronautics},
	author = {Chen, Christine and Edwards, Matthew W. and Gill, Bilal and Smearcheck, Samantha and Adami, Tony and Calhoun, Sean and Wu, Minghong G. and Cone, Andrew and Lee, Seung Man},
	month = jun,
	year = {2019}
{% endhighlight %}
</p>
</details>

<details> <summary> R. E. Weibel, M. W. M. Edwards, and C. S. Fernandes, “Establishing a Risk-Based Separation Standard for Unmanned Aircraft Self Separation,” in Ninth USA/Europe Air Traffic Management Research & Development Seminar, 2011.</summary>
<p>

{% highlight tex %}
@inproceedings{weibelEstablishingRiskBasedSeparation2011,
	title = {Establishing a {Risk}-{Based} {Separation} {Standard} for {Unmanned} {Aircraft} {Self} {Separation}},
	doi = {10.2514/6.2011-6921},
	booktitle = {Ninth {USA}/{Europe} {Air} {Traffic} {Management} {Research} \& {Development} {Seminar}},
	publisher = {American Institute of Aeronautics and Astronautics},
	author = {Weibel, Roland E. and Edwards, Matthew W. M. and Fernandes, Caroline S.},
	url = {https://doi.org/10.2514/6.2011-6921},
	month = sep,
	year = {2011}
}
{% endhighlight %}
</p>
</details>
<br>

# Evaluation of TCAS II Version 7.1

The modern encounter models were first used for a safety study, funded by the TCAS program office. These generative models evaluated and validated the upgrade of TCAS II to Version 7.1. The success of this evaluation laid the groundwork for subsequent safety studies.

<details> <summary> L. P. Espindle, J. D. Griffith, and J. K. Kuchar, “Safety Analysis of Upgrading to TCAS Version 7.1 Using the 2008 U.S. Correlated Encounter Model,” Massachusetts Institute of Technology, Lincoln Laboratory, Project Report ATC-349, 2009.</summary>
<p>

{% highlight tex %}
@techreport{espindleSafetyAnalysisUpgrading2009,
	type = {Project {Report}},
	title = {Safety {Analysis} of {Upgrading} to {TCAS} {Version} 7.1 {Using} the 2008 {U}.{S}. {Correlated} {Encounter} {Model}},
	number = {ATC-349},
	institution = {Massachusetts Institute of Technology, Lincoln Laboratory},
	author = {Espindle, L. P. and Griffith, J. D. and Kuchar, J. K.},
	url = {https://www.ll.mit.edu/r-d/publications/safety-analysis-upgrading-tcas-version-71-using-2008-us-correlated-encounter-model},
	year = {2009}
}
{% endhighlight %}
</p>
</details>

<details> <summary> B. J. Chludzinski, “Evaluation of TCAS II Version 7.1 Using the FAA Fast-Time Encounter Generator Model,” Massachusetts Institute of Technology, Lincoln Laboratory, Project Report ATC-346 Volume 1, Apr. 2009.</summary>
<p>

{% highlight tex %}
@techreport{chludzinskiEvaluationTCASII2009,
	type = {Project {Report}},
	title = {Evaluation of {TCAS} {II} {Version} 7.1 {Using} the {FAA} {Fast}-{Time} {Encounter} {Generator} {Model}},
	number = {ATC-346 Volume 1},
	institution = {Massachusetts Institute of Technology, Lincoln Laboratory},
	author = {Chludzinski, Barbara J.},
	url = {https://www.ll.mit.edu/r-d/publications/evaluation-tcas-ii-version-71-using-faa-fast-time-encounter-generator-model-volume},
	month = apr,
	year = {2009}
}
{% endhighlight %}
</p>
</details>

<details> <summary>B. J. Chludzinski, “Evaluation of TCAS II Version 7.1 Using the FAA Fast-Time Encounter Generator Model-Appendix,” Massachusetts Institute of Technology, Lincoln Laboratory, Project Report ATC-346 Volume 2, Apr. 2009.</summary>
<p>

{% highlight tex %}
@techreport{chludzinskiEvaluationTCASII2009a,
	type = {Project {Report}},
	title = {Evaluation of {TCAS} {II} {Version} 7.1 {Using} the {FAA} {Fast}-{Time} {Encounter} {Generator} {Model}-{Appendix}},
	number = {ATC-346 Volume 2},
	institution = {Massachusetts Institute of Technology, Lincoln Laboratory},
	author = {Chludzinski, Barbara J.},
	url = {https://www.ll.mit.edu/r-d/publications/evaluation-tcas-ii-version-71-using-faa-fast-time-encounter-generator-model},
	month = apr,
	year = {2009}
}
{% endhighlight %}
</p>
</details>
