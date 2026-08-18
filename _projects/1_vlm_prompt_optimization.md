---
layout: page
title: Inference-Time Adaptation of Vision-Language Models
description: State-of-the-art few-shot detection, zero-shot classification, and alignment with frozen, black-box VLMs.
img:
importance: 1
category:
---

**Problem.** Adapting vision-language models to new tasks usually means fine-tuning, which requires weight access, task-specific data, and compute. Practitioners with 10 labeled images and an API key have no good option.

**Finding.** The model's inputs and internals carry enough signal to close the gap; the weights can stay frozen. Three complementary results:

- **DetPO** (ECCV 2026): an iterative prompt-optimization framework that mines false-positive and false-negative feedback to rewrite detection prompts. With contemporary VLMs (e.g., Qwen3, Gemini3) it reaches state-of-the-art few-shot detection on the RF20 benchmark, outperforming specialist models such as GroundingDINO, entirely in a black-box setting. [Code](https://github.com/ggare-cmu/DetPO) · [Project page](https://ggare-cmu.github.io/DetPO/)
- **Distribution-conditioned attribute selection** (PFATCV Workshop at ECCV 2026, **Oral**): LLM-generated class descriptors are label-conditioned, not image-conditioned; removing class names collapses ImageNet accuracy from 59.5% to 15.5%. Selecting attributes directly from target images in CLIP's embedding space recovers 23.8% without class names, beats CoOp at minimal cost, and yields interpretable dataset summaries. [arXiv](https://arxiv.org/abs/2607.18695) · [Project page](https://ggare-cmu.github.io/AttributeSelect/)
- **Activation Reward Models** (ACL Findings 2026): reward models built from VLM activations align model behavior from a handful of examples. [Paper](https://aclanthology.org/2026.findings-acl.1709/)
- **Soft-prompt tuning** (ongoing): learned continuous prompt embeddings match or exceed LoRA fine-tuning in the 10-shot setting.

**Why it matters.** Adaptation becomes an inference-time problem rather than a training problem: cheaper to deploy, auditable, and usable with closed-weight models.

See the [publications page](/publications/) for the papers.
