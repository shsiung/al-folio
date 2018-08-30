---
layout: page
title: Constraint Optimization using Factor Graph
description: Fall 2017 Convex Optimization course project
img: /assets/img/proj_constraint.gif
date: 2018-08-20 10:32:20 +0300
timeline: 2017
---
My final project for the Convex Optimization class is performing constraint optimization using factor graph, in the application of joint estimation and control of a robot. The motivation is following Duy-Nguyen et al.'s *A factor graph approach to estimation and model predictive control on unmanned aerial vehicles*.

The method uses Sequential Quadratic Programming (SQP) to solve for the Lagrangian and the corresponding primal and dual problem.

This work is interesting because it combines the traditional unconstrained optimization using factor graph with Lagrange multipliers.

The final project poster can be accessed via the image link:

[<img class="col one left" src="{{ '/assets/proj_constraint/poster_ss.png' | prepend: site.baseurl | prepend: site.url }}">]({{ '/assets/proj_constraint/10725_poster.pdf' | prepend: site.baseurl | prepend: site.url }})
