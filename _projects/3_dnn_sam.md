---
layout: page
title: DNN-SAM
description: Split-and-merge DNN execution for timely and accurate object detection.
img: assets/img/projects/dnn-sam/case_study_results.png
importance: 3
category: research
related_publications: true
---

## Split-and-merge DNN execution for real-time object detection

Multi-camera real-time object-detection systems must balance accuracy and timeliness across image regions with different criticality. DNN-SAM dynamically splits an inference task into independently scheduled subtasks:

- A **mandatory subtask** processes a cropped, safety-critical region.
- An **optional subtask** processes a down-scaled version of the complete image.
- A merge stage combines their detections into the final result.

{% include figure.liquid
  loading="eager"
  path="assets/img/projects/dnn-sam/system_overview.png"
  class="img-fluid rounded z-depth-1 project-figure-light"
  alt="DNN-SAM pipeline splitting an image into mandatory and optional networks, scheduling their subtasks on GPUs, and merging their detection results"
  caption="DNN-SAM system overview: split, independently schedule, and merge mandatory and optional DNN subtasks."
  zoomable=true
%}

The scheduler prioritizes subtasks according to criticality and adapts input scale to meet timing constraints. In evaluation, DNN-SAM:

- Improved detection accuracy in safety-critical regions by **2.0-3.7x**.
- Reduced average inference latency by **4.8-9.7x**.
- Met all evaluated timing constraints.

{% include figure.liquid
  path="assets/img/projects/dnn-sam/case_study_results.png"
  class="img-fluid rounded z-depth-1 project-figure-light"
  alt="Emergency-braking case-study comparison showing DNN-SAM stopping within the safety distance while the baseline exceeds it"
  caption="Emergency-braking case study comparing the baseline with DNN-SAM."
  zoomable=true
%}

DNN-SAM was published at IEEE RTAS 2022.

## Demo video

{% include video.liquid
  path="https://www.youtube.com/embed/x0yWktOrNhM"
  class="project-video-embed rounded z-depth-1"
  width="100%"
  title="DNN-SAM autonomous-car emergency-braking case study"
%}

<div class="caption">DNN-SAM case study using a 1/10-scale autonomous car.</div>

{% nocite kang2022dnn %}
