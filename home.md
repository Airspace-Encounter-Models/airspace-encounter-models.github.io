---
layout: splash
permalink: /
hidden: true
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/mm-home-page-feature.jpg
excerpt: >
  Statistical models of how aircraft behave during close encounters.<br />
feature_row:
  - alt: "blog"
    title: "Blog"
    excerpt: "Updates and whats new"
    url: /blog/
    btn_class: "btn--primary"
    btn_label: "Learn more"
  - alt: "contribute"
    title: "Contribute"
    excerpt: "Contributing guidelines, workflow, and style"
    url: /contribute/
    btn_class: "btn--primary"
    btn_label: "Learn more"
  - alt: "Documentation"
    title: "Technical reports"
    excerpt: "References, citations"
    url: /techdoc/
    btn_class: "btn--primary"
    btn_label: "Learn more"      
---

{% include feature_row %}

For many aviation safety studies, aircraft behavior is represented using encounter models, which are statistical models of how aircraft behave during close encounters. They are used to provide a realistic representation of the range of encounter flight dynamics where an aircraft collision avoidance system would be likely to alert. Encounter models represent the encounter geometry, but also the aircraft behavior (accelerations) during the course of the encounter. Encounter models have been developed for many different manned operational contexts, but there are new considerations for unmanned aircraft operations including the lower operating altitudes and interactions with service providers and other users.

This GitHub organization and associated repositories are intended to eventually supersede the legacy [MIT Lincoln Laboratory hosted encounter model website](https://topa.atc.ll.mit.edu/lldata/) and align encounter model development with modern community driven software practices. As of 2019, this original MIT Lincoln Laboratory-hosted website has not been deprecated by this GitHub organization yet. Not all encounter model content is available on GitHub. *Note that the legacy website is currently down for extended maintenance.*

To enable assessment of aviation safety systems such as collision avoidance or detect and avoid systems, these models are designed with the following requirements:

- Be built using aircraft operational data;
- Have dependence on geographic region, airspace class, and altitude layer;
- Have a representative time period for different evaluations;
- Reflect realistic aircraft flight dynamics;
- Realistically capture relative aircraft geometry; and
- Enable fast-time simulation.
  