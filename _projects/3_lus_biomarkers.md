---
layout: page
title: Interpretable Lung Ultrasound Biomarkers
description: Clinician-understandable biomarkers that decouple feature learning from downstream clinical tasks.
img:
importance: 3
category:
---

**Problem.** Every new clinical task (diagnosis, severity, S/F ratio) traditionally requires assembling a labeled dataset and training a new end-to-end network, at high annotation cost and with opaque features.

**Finding.** A biomarker classification pre-task learns an informative, concise, and interpretable feature space from ultrasound videos with only weak video-level supervision. Downstream expert models built on these biomarker features match end-to-end models in accuracy at a fraction of the training cost (ISBI 2026). The same biomarker vocabulary supports severity scoring via weakly supervised contrastive learning (ISBI 2025) and improves model reliability under distribution shift (BIAS 2023).

**Why it matters.** Clinicians reason in biomarkers, not activations. A shared, interpretable feature space makes model behavior checkable and new clinical tasks cheap.

This line of work was developed with clinical collaborators at LSU Health and featured in CMU SCS's LINK Magazine (["Seeing Beneath The Surface"](https://magazine.cs.cmu.edu/seeing-beneath-the-surface), 2022). It also produced my earlier COVID-19 work: dense pixel-labeling for reverse-transfer diagnostic learning (ISBI 2021) and the role of pleura and adipose in lung ultrasound AI (LL-COVID19 workshop, MICCAI 2021).

See the [publications page](/publications/) for the papers.
