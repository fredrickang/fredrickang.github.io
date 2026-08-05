---
layout: page
title: ZeroSwap
description: SSD-based GPU memory extension for real-time multi-DNN inference.
img: assets/img/projects/zeroswap/design_overview.png
importance: 1
category: research
related_publications: true
---

## Minimizing swap overhead for real-time multi-DNN inference

Real-time multi-DNN systems on embedded platforms are often constrained by limited GPU memory. Extending memory through SSD swapping can address capacity limits, but PCIe transfers and runtime memory management introduce substantial overhead.

ZeroSwap minimizes that overhead through three mechanisms:

- **Semantic-aware selective swapping** moves only inference-critical data, reducing swap volume.
- **Shared pinned allocation** removes runtime allocation overhead through physical-memory sharing.
- **Segment-level overlapping** hides PCIe transfer latency by overlapping swap operations with computation.

{% include figure.liquid
  loading="eager"
  path="assets/img/projects/zeroswap/design_overview.png"
  class="img-fluid rounded z-depth-1"
  alt="ZeroSwap architecture connecting DNN applications, shared pinned allocation, semantic-aware selective swapping, an overlap-aware scheduler, system RAM, and SSD storage"
  caption="ZeroSwap design overview: shared pinned allocation, semantic-aware selective swapping, and overlap-aware scheduling."
  zoomable=true
%}

Implemented on a state-of-the-art machine-learning framework, ZeroSwap improved DNN task-set schedulability by up to **101.7%** and achieved up to **3.2x faster response time** compared with existing approaches.

{% include figure.liquid
  path="assets/img/projects/zeroswap/results_preview.png"
  class="img-fluid rounded z-depth-1"
  alt="Runtime latency breakdown comparing RT-Swap and ZeroSwap, showing shorter execution and swap latency with ZeroSwap"
  caption="Runtime latency breakdown comparing ZeroSwap with RT-Swap."
  zoomable=true
%}

ZeroSwap was published at IEEE RTAS 2026 and received the **Best Paper Award**.

## Demo video

{% include video.liquid
  path="https://www.youtube.com/embed/HsKKCJwzqv8"
  class="project-video-embed rounded z-depth-1"
  width="100%"
  title="ZeroSwap multi-camera object-detection demo"
%}

<div class="caption">ZeroSwap case study comparing multi-camera object-detection performance with RT-Swap.</div>

{% nocite kang2026zeroswap %}
