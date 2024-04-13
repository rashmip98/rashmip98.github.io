---
layout: post
title:  Efficient Panoptic Segmentation with SOLOv2
tag: project
---

Panoptic segmentation is a scene understanding problem recently introduced in that combines the prediction from both instance and semantic segmentation into a general
unified output. The project implements and modifies the state-of-the-art EfficientPS model by changing the instance segmentation head from Mask-RCNN to SOLOv2. 

The basis of the experimentation is to use a location-based instance segmentation for panoptic segmentation to evaluate its effect on the performance metrics, training time and inference time with this modification. The overall performance of the baseline
EfficientPS and the modified version is compared with the Panoptic Quality metric.

View the code -> [GitHub](https://github.com/rashmip98/Efficient-Panoptic-Segmentation-with-SOLOv2)

Read the report -> [Google Drive](https://drive.google.com/file/d/1MWChm9MHwgJZV0jmAEzvYVXIt4zXPKe_/view)
