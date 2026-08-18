---
layout: page
title: When Can Models Trust Their Training Data?
description: Diagnosing when and why multimodal models generalize, and turning the diagnosis into fixes.
img:
importance: 2
category:
---

**Problem.** Models learn whatever correlations the training distribution offers, including shortcuts that fail under distribution shift. Knowing when a learned correlation can be trusted is the difference between a demo and a deployable system.

**Findings across three works:**

- **LCA-on-the-Line** (ICML 2024, **Oral**): class-taxonomy distance (LCA) predicts out-of-distribution generalization across model families, turning label hierarchies into a practical model-selection signal. [Project page](https://elvishelvis.github.io/papers/lca/)
- **Natural experiments in real-world data** ([arXiv 2026](https://arxiv.org/abs/2606.03251)): real-world datasets contain naturally occurring interventions; treating them as such, via Markov-blanket-based causal feature selection, improves downstream performance over purely observational treatment.
- **The question-first paradox** ([arXiv 2026](https://arxiv.org/abs/2607.15565)): logit-lens and attention probes show that placing a question before the image guides perception but starves answer generation of the question. Prompt echoing, restating the question on both sides of the image, fixes it training-free, up to +19 accuracy points across NaturalBench, POPE, Winoground, and VQAv2.

**Why it matters.** Mechanistic diagnosis turns "the model fails sometimes" into a specific, fixable cause, and each diagnosis above shipped with its fix.

See the [publications page](/publications/) for the papers.
