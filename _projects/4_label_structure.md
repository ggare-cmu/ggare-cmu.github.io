---
layout: page
title: Learning with Label Structure and Uncertainty
description: Getting more out of imperfect labels, from coarse annotations to class taxonomies to RF waveforms.
img:
importance: 4
category:
---

**Problem.** Real-world labels are coarse, noisy, and structured; standard one-hot training throws that structure away.

**Findings across four works:**

- **LEARNER** (ISBI 2026): contrastive learning recovers granular labels from coarse ones, cutting annotation requirements for fine-grained medical tasks.
- **Label uncertainty for ultrasound segmentation** (ISBI 2026): modeling annotator uncertainty directly improves segmentation quality.
- **LCA-on-the-Line** (ICML 2024): class-taxonomy distance (LCA) predicts out-of-distribution generalization, turning label hierarchies into a model-selection signal.
- **W-Net** (Medical Image Analysis 2022) and **confidence labels** (arXiv 2021): incorporating ultrasound RF waveform data and probabilistic class-similarity labels improves dense segmentation of subcutaneous and breast tissue; both are patented (US20240177000A1, US20240177445A1).

**Why it matters.** Label structure is free supervision. Exploiting it improves accuracy, calibration, and out-of-distribution robustness without new data collection.

See the [publications page](/publications/) for the papers.
