---
layout: page
title: Projects
permalink: /projects
---

<div class="posts">
  {% for tag in site.tags %}
    {% for post in tag[1] %}
    <article class="post">
      <a href="{{ site.baseurl }}{{ post.url }}">
        <h4>{{ post.title }}</h4>

        <div>
          <p class="post_date">{{ post.date | date: "%B %e, %Y" }}</p>
        </div>
      </a>
      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
  {% endfor %}
</div>

## Code Implementations 
GitHub repos with implementations of classic models and techniques spanning topics like computer vision, deep learning, perception, robotics

#### Deep Learning Models for Computer Vision
This contains the implementation and training of deep learning models for computer vision tasks like object detection, image segmentation, classification, image generation. The following models are implemented:
- [YOLO](https://github.com/rashmip98/DLforComputerVision/tree/main/YOLO)
- [SOLO](https://github.com/rashmip98/DLforComputerVision/tree/main/SOLO)
- [VAE & GAN](https://github.com/rashmip98/DLforComputerVision/tree/main/VAE-GAN)
- [Faster-RCNN](https://github.com/rashmip98/DLforComputerVision/tree/main/Faster-RCNN)

#### Concepts in Perception
This contains the implementation of classical methods in perception for tasks like 3D reconstruction, two-view & plane-sweep stereo, depth estimation, camera pose estimation. Code links for few of the tasks mentioned:
- [3D reconstruction](https://github.com/rashmip98/perception/tree/main/3d_recon-from-2d_images)
- [Two-view & Multi-view Stereo](https://github.com/rashmip98/perception/tree/main/2view_and_multiview_stereo)
- [Depth Estimation](https://github.com/rashmip98/perception/tree/main/depth_estimation_using_optical_flow)
- [P3P & PnP Camera Pose](https://github.com/rashmip98/perception/tree/main/p3p-pnp-for-camera_pose)

#### Robotics
This contains non-DL and DL techniques in robotics such as SLAM, reinforcement learning, various filters.
- [Bayes Filter](https://github.com/rashmip98/learning_in_robotics/tree/main/bayes_filter_and_HMM) to track the position of a robot operating in a 2D grid world
- [Particle Filter based SLAM](https://github.com/rashmip98/learning_in_robotics/tree/main/SLAM) for humanoid robot
- [Extended & Unscented Kalman Filter](https://github.com/rashmip98/learning_in_robotics/tree/main/unscented_kalman_filter)
- [Q-Learning](https://github.com/rashmip98/learning_in_robotics/tree/main/Q_Learning) on the Cartpole Problem

# Publications
- ‘Real-Time Vein Detection and Mapping using Near-Infrared Lights’ (IEEE INDICON, [IEEE Xplore](https://ieeexplore.ieee.org/document/9342163)) <style>Dec 2021 {text-align: right}</style> 
- ‘Portable Gas Detection and Warning System for Olfactory Disabled’ (IEEE INCET, [IEEE Xplore](https://ieeexplore.ieee.org/document/9154120)) <style>Jun 2020 {text-align: right}</style>
- ‘Real-Time Asset Tracking using BLE Beacons’ (Global Conference for Advancement in Tech, [IEEE Xplore](https://ieeexplore.ieee.org/document/8978304)) <style>Oct 2019 {text-align: right}</style>
