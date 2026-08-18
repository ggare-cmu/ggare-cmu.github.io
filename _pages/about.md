---
layout: about
title: About
permalink: /
subtitle: >
  Ph.D. Candidate, <a href="https://www.ri.cmu.edu/" target="_blank">Robotics Institute</a>, <a href="https://www.cmu.edu/" target="_blank">Carnegie Mellon University</a>

profile:
  align: right
  image: grg_profile_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>Smith Hall 101, 5000 Forbes Avenue</p>
    <p>Pittsburgh, PA 15213</p>
    <p>ggare AT andrew DOT cmu DOT edu</p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 6 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true
  limit: 3
---

<div style="border-left: 4px solid #b31b1b; background: rgba(179, 27, 27, 0.07); padding: 0.8rem 1rem; border-radius: 4px; margin-bottom: 1.2rem;">
<strong>I am on the job market for research scientist roles</strong> (graduating late 2026).
My focus: vision-language models, inference-time adaptation and alignment, and trustworthy deployment.
<a href="/assets/pdf/Gautam_Gare_Resume.pdf">Resume</a> · <a href="https://scholar.google.com/citations?user=BX4jUxEAAAAJ">Google Scholar</a> · <a href="mailto:ggare@andrew.cmu.edu">Email me</a>
</div>

I am a Ph.D. candidate in the Robotics Institute at [Carnegie Mellon University](https://www.cmu.edu/), advised by Prof. [John Galeotti](https://www.ri.cmu.edu/ri-faculty/john-galeotti/) and Prof. [Deva Ramanan](https://www.ri.cmu.edu/ri-faculty/deva-kannan-ramanan/).

**I make frozen vision-language models do new things without touching their weights.** My research treats adaptation as an inference-time problem, in three threads:

- **Adapt.** Prompt optimization reaches state-of-the-art few-shot object detection with black-box VLMs, outperforming specialist detectors (**DetPO, ECCV 2026**). Image-conditioned attribute selection beats prompt tuning for zero-shot classification at minimal cost (**PFATCV Workshop at ECCV 2026, Oral**). Activation-space reward models align VLMs from a handful of examples (**ACL Findings 2026**).
- **Understand.** Why do models generalize or fail? Class-taxonomy distance predicts out-of-distribution generalization (**ICML 2024 Oral**). Prompt echoing resolves the question-first paradox in VLMs, up to +19 accuracy points training-free ([arXiv 2026](https://arxiv.org/abs/2607.15565)). Real-world datasets contain natural experiments that causal feature selection can exploit ([arXiv 2026](https://arxiv.org/abs/2606.03251)).
- **Deploy.** Medical imaging is my proving ground: interpretable lung-ultrasound biomarkers across five ISBI papers, a *Medical Image Analysis* journal paper, and four U.S. patents.

Next: extending inference-time adaptation to **vision-language-action models** for robotics.

Before the Ph.D., I completed my M.S. in Electrical and Computer Engineering at CMU (4.0 GPA, Dec 2020) and worked 3 years as a Senior Data Scientist and Software Engineer at [Sling Media](https://www.linkedin.com/company/sling-media/) (Dish Networks), where I led analytics for user-churn modeling and shipped a 20% app-startup-time improvement. I hold a B.E. in Electronics and Communication from [B.M.S. College of Engineering](https://www.bmsce.ac.in/), India.

My research is supported by the Liang Zhao Endowed Fellowship (2025) and the CMLH Translational Fellowship (2022). Outside the lab, I am a wildlife photographer and conservationist; see my [wildlife photos](/wildlife/).

{% include zoom_original_fix.liquid %}
