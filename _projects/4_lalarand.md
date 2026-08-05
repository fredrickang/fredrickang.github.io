---
layout: page
title: LaLaRAND
description: Fine-grained CPU/GPU scheduling for real-time DNN layers.
img: assets/img/projects/lalarand/system_overview.png
importance: 4
category: research
related_publications: true
---

## Flexible layer-by-layer CPU/GPU scheduling for real-time DNN tasks

Conventional machine-learning frameworks commonly assign each DNN task to a single processor, limiting their ability to exploit heterogeneous embedded CPU/GPU platforms. LaLaRAND introduces fine-grained, layer-level resource allocation for real-time DNN execution.

The framework combines CPU-friendly quantization with schedulability-aware CPU/GPU allocation while mitigating inference-accuracy loss. Its system-wide scheduler makes runtime decisions using DNN profile data and current resource availability.

{% include figure.liquid
  loading="eager"
  path="assets/img/projects/lalarand/system_overview.png"
  class="img-fluid rounded z-depth-1 project-figure-light"
  alt="LaLaRAND architecture showing layer-level CPU and GPU kernel execution coordinated by a system-wide runtime scheduler"
  caption="LaLaRAND system overview: layer-level CPU/GPU execution coordinated by a system-wide scheduler."
  zoomable=true
%}

Compared with prior approaches, LaLaRAND:

- Improved schedulability by **56%** over an existing approach.
- Improved schedulability by **80%** over vanilla PyTorch.
- Limited the inference-accuracy difference to at most **0.4%**.

LaLaRAND was published at IEEE RTSS 2021.

{% nocite kang2021lalarand %}
