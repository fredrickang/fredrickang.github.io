---
layout: post
title: LaLaRAND accepted at IEEE RTSS 2021
date: 2021-10-19 12:00:00+0900
inline: false
related_posts: false
---

Our paper [“LaLaRAND: Flexible Layer-by-Layer CPU/GPU Scheduling for Real-Time DNN Tasks”](/projects/4_lalarand/) was accepted at the 42nd IEEE Real-Time Systems Symposium.

{% include figure.liquid
  loading="eager"
  path="assets/img/projects/lalarand/system_overview.png"
  class="img-fluid rounded z-depth-1 project-figure-light"
  alt="LaLaRAND architecture showing layer-level CPU and GPU execution coordinated by a system-wide runtime scheduler"
  caption="LaLaRAND coordinates layer-level CPU/GPU execution through a system-wide scheduler."
  zoomable=true
%}

LaLaRAND coordinates DNN execution at layer granularity across heterogeneous CPU and GPU resources. It combines quantization-aware execution with system-wide scheduling to improve schedulability while limiting accuracy loss.

The paper is available from [IEEE Xplore](https://ieeexplore.ieee.org/document/9622325/).

Source: [RTCL@DGIST announcement](https://rtcl.dgist.ac.kr/index.php/news/a-paper-got-accepted-at-rtss-2021/)
