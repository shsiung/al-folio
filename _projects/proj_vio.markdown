---
layout: page
title: Visual-Inertial Odometry (VIO)
description: My master thesis at CMU, which leads to two publications
img: /assets/img/proj_vio.gif
timeline: 2016 - Present
date: 2018-08-16 13:32:20 +0300
---

Visual-inertial odometry (VIO) is an algorithm that provides a robot's odometry by fusing both *visual* and *inertial* information. Visual information is provided by cameras, and inertial information is provided by an <a href="https://en.wikipedia.org/wiki/Inertial_measurement_unit">inertial measurement unit (IMU)</a>. Below video shows an example of my VIO algorithm running on an autel X-star drone in real-time:
<div class="img_row">
    <img class="col three left" src="{{ site.baseurl }}/assets/gif/vio_outdoor.gif" alt="" title="VIO example"/>
</div>
<div class="col three caption">
    My VIO algorithm running on an Autel X-star drone in real-time.
</div>

Typically, the existing methods employ either a *filtering* method based on the extended Kalman filter (EKF), or an *optimization* method. My research focuses on the **fixed-lag optimization-based** method (or fixed-lag smoothing) using **factor graph**[^fn1], which is the state-of-the-art method in solving a VIO problem. 

A fixed-lag smoother estimate a fixed window of variables at a given time, so the optimization size is constant as shown in below graphs. Below are two graphs that illustrate a fixed-lag smoother is employed in estimating a robot trajectory. The left graph shows the blue active window of states being estimated, the right graph shows the correcponding factor graph.

<div class="img_row">
    <img class="col one left" src="{{ site.baseurl }}/assets/gif/window_traj.gif" alt="" title="example image"/>
    <img class="col two left" src="{{ site.baseurl }}/assets/gif/fixed-lag-smoother.gif" alt="" title="VIO example"/>
</div>

[^fn1]: [Factor Graph for Robot Perception Book](https://www.nowpublishers.com/article/Details/ROB-043){:target="\_blank"}  

In my thesis, I address two challenges in the fixed-lag smoothing framework --- Efficiency and Nonlinearity. In particular, there are two major contributions:

  1. Employing information sparsification to address the efficiency issue.
  2. Employing group affine property to address the consistency problem

For more details, please check my <a href="{{ '/assets/pdf/Hsiung18thesis.pdf' | prepend: site.baseurl | prepend: site.url }}">Master Thesis</a>  and my 2018 <a href="{{ '/assets/pdf/Hsiung18thesis.pdf' | prepend: site.baseurl | prepend: site.url }}">IROS paper</a>.

<!-- 

Every project has a beautiful feature shocase page. It's easy to include images, in a flexible 3-column grid format. Make your photos 1/3, 2/3, or full width.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: Project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---


<div class="img_row">
    <img class="col one left" src="{{ site.baseurl }}/assets/img/1.jpg" alt="" title="example image"/>
    <img class="col one left" src="{{ site.baseurl }}/assets/img/2.jpg" alt="" title="example image"/>
    <img class="col one left" src="{{ site.baseurl }}/assets/img/3.jpg" alt="" title="example image"/>
</div>
<div class="col three caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="img_row">
    <img class="col three left" src="{{ site.baseurl }}/assets/img/5.jpg" alt="" title="example image"/>
</div>
<div class="col three caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images. Say you wanted to write a little bit about your project before you posted the rest of the images. You describe how you toiled, sweated, *bled* for your project, and then.... you reveal it's glory in the next row of images.


<div class="img_row">
    <img class="col two left" src="{{ site.baseurl }}/assets/img/6.jpg" alt="" title="example image"/>
    <img class="col one left" src="{{ site.baseurl }}/assets/img/11.jpg" alt="" title="example image"/>
</div>
<div class="col three caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>


<br/><br/>


The code is simple. Just add a col class to your image, and another class specifying the width: one, two, or three columns wide. Here's the code for the last row of images above:

<div class="img_row">
    <img class="col two left" src="/assets/img/6.jpg"/>
    <img class="col one left" src="/assets/img/11.jpg"/>
</div>
 -->