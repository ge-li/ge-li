---
title: "Computer Vision Analysis of Surgical Footage"
subtitle: "Automated real-time monitoring and assessment of cataract surgical videos."
excerpt: "I engineered *Mask R-CNN* to automate the real-time monitoring and assessment of cataract surgery in collaboration with the Department of Ophthalmology and Visual Sciences. This model achieved outstanding performance in tracking the pupil and twelve different surgical tools."
date: 2019-12-06
author: "Li Ge"
draft: false
# tags:
# - hugo-site
categories:
  - Machine Learning
  - Computer Vision
# layout options: single or single-sidebar
layout: single
links:
- icon: file-powerpoint
  icon_pack: fas
  name: slides
  url: /project/cataract/li_ge_cataract.pdf
# - icon: github
#   icon_pack: fab
#   name: code
#   url: 
# - icon: newspaper
#   icon_pack: far
#   name: Blog post
#   url: https://education.rstudio.com/blog/2020/07/palmerpenguins-cran/
---

Rotation advisor: [Yin Li, PhD](https://www.biostat.wisc.edu/~yli/).

In collaboration with: [Stephen K. Sauer, MD](https://www.uwhealth.org/providers/stephen-k-sauer-md).

### Motivation

* Cataracts are the leading cause of blindness in the world, according to the World Health Organization.

* Cataracts Surgeries are the most common surgical interventions performed in the world (~19M interventions / year).

* Cataract cases are estimated to increase 78% by 2050. 

* Ophthalmology residents spend a large portion of their training in learning cataract surgery. 

* A key challenge in the training is to develop a systematic and objective assessment of the surgical competency of the residents. 

### Results

* The trained Mask R-CNN model achieves outstanding performance detecting pupils and twelve different surgical tools.
* We are able to monitor important metrics such as pupil deviation and pupil magnification in real-time. 

Pupil | mAP (IoU=0.50:0.95) | AP50 | AP75
:---:|:---:|:---:|:---:|
Segmentation |81.13 |96.98 |86.19 |


![Full Video Metrics](surgical_metrics_vis_2.png)

Surgery Clip               |  Real-Time Monitoring
:-------------------------:|:-------------------------:
![](surgery_clip.gif)  |  ![](real_time_monitoring.gif)

### Dataset 

* [CaDIS](https://cataracts.grand-challenge.org/CaDIS/)
* 4738 images extracted from 25 videos with corresponding semantic annotation.
* Training: 3582, Validation: 542, Testing: 614. 

### Method

* [Mask R-CNN](https://arxiv.org/abs/1703.06870)
* [Detectron2](https://github.com/facebookresearch/detectron2)




