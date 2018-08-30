---
layout: page
title: Submodular Visual Feature Selection
description: Fall 2017 Geometry-Based Vision course project
img: /assets/img/proj_feature.gif
date: 2018-08-20 10:32:20 +0300
timeline: 2017
---

My final project for the Geometry-Based Vision class is investigating ways to select a subset of visual features
from a large feature pool. The motivation is following Luca et al.'s *Attention and Anticipation in Fast Visual-Inertial Navigation*.

The paper formulates feature selections {% katex %} S {% endkatex %} from a feature pool {% katex %} F {% endkatex %} as a submodular problem with the general form:
{% katex display %}
\max_{S\subset F}\; f(S)\quad \text{subject to} \quad |S| \le \kappa
{% endkatex %}
where {% katex %} \kappa {% endkatex %} is the maximum number of features set by the user. 

The goal is to achieve accurate state estimation using the minimum resources.

The final project poster can be accessed via the image link:

[<img class="col one left" src="{{ '/assets/proj_feature/poster_ss.png' | prepend: site.baseurl | prepend: site.url }}">]({{ '/assets/proj_feature/16822_poster.pdf' | prepend: site.baseurl | prepend: site.url }})
