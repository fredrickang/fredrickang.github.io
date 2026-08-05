---
layout: page
title: RT-Swap
description: Real-time GPU memory management using CPU memory as swap space.
img: assets/img/projects/rt-swap/overview.png
importance: 2
category: research
related_publications: true
---

## Addressing GPU memory bottlenecks for real-time multi-DNN inference

The growing memory requirements of deep neural networks can prevent sophisticated models from running together on memory-constrained GPUs. RT-Swap is a real-time memory-management framework that transparently extends GPU capacity with CPU memory without compromising timing guarantees.

RT-Swap coordinates memory-object swapping with DNN execution, enabling multi-DNN task sets to remain schedulable even when their combined memory demand exceeds physical GPU capacity.

{% include figure.liquid
  loading="eager"
  path="assets/img/projects/rt-swap/overview.png"
  class="img-fluid rounded z-depth-1 project-figure-light"
  alt="RT-Swap architecture showing the preloaded library, scheduler, GPU and host memory, and memory-object swap-out and swap-in operations"
  caption="RT-Swap system architecture and memory-object swap-in and swap-out process."
  zoomable=true
%}

Evaluation on representative machine-learning frameworks showed that RT-Swap:

- Improved task-set schedulability by at least **72%** over existing approaches.
- Supported workloads demanding up to **96.2% more memory** than the GPU's physical capacity.
- Preserved the timing guarantees required by real-time inference workloads.

RT-Swap was published at IEEE RTAS 2024.

{% nocite kang2024rt %}
