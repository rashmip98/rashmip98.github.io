---
layout: page
title:
permalink: /projects
---

## Projects
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

## Publications
- ‘Real-Time Vein Detection and Mapping using Near-Infrared Lights’ (IEEE INDICON, [IEEE Xplore](https://ieeexplore.ieee.org/document/9342163)) <style>Dec 2021 {text-align: right}</style> 
- ‘Portable Gas Detection and Warning System for Olfactory Disabled’ (IEEE INCET, [IEEE Xplore](https://ieeexplore.ieee.org/document/9154120)) <style>Jun 2020 {text-align: right}</style>
- ‘Real-Time Asset Tracking using BLE Beacons’ (Global Conference for Advancement in Tech, [IEEE Xplore](https://ieeexplore.ieee.org/document/8978304)) <style>Oct 2019 {text-align: right}</style>
