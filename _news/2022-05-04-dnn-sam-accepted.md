---
layout: post
title: DNN-SAM accepted at IEEE RTAS 2022
date: 2022-05-04 12:00:00+0900
inline: false
related_posts: false
---

Our paper [“DNN-SAM: Split-and-Merge DNN Execution for Real-Time Object Detection”](/projects/3_dnn_sam/) was accepted at the 28th IEEE Real-Time and Embedded Technology and Applications Symposium.

{% include figure.liquid
  loading="eager"
  path="assets/img/projects/dnn-sam/system_overview.png"
  class="img-fluid rounded z-depth-1 project-figure-light"
  alt="DNN-SAM pipeline splitting an image into mandatory and optional networks, scheduling their subtasks, and merging their results"
  caption="DNN-SAM splits, independently schedules, and merges mandatory and optional DNN subtasks."
  zoomable=true
%}

DNN-SAM separates object-detection inference into mandatory and optional subtasks, schedules them according to criticality, and merges their outputs. This design improves responsiveness and accuracy in safety-critical image regions while meeting timing constraints.

The paper is available from [IEEE Xplore](https://ieeexplore.ieee.org/document/9804671/).

Source: [RTCL@DGIST announcement](https://rtcl.dgist.ac.kr/index.php/news/a-paper-got-accepted-at-rtas-2022/)
