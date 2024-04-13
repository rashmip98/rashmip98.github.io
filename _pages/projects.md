---
layout: page
permalink: /projects
---

## Projects
<div class="posts">
  {% for tag in site.tags %}
    {% for post in tag[1] %}
    <article class="post">
      <a href="{{ site.baseurl }}{{ post.url }}">
        <h1>{{ post.title }}</h1>

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
- ‘Real-Time Vein Detection and Mapping using Near-Infrared Lights’ (IEEE INDICON, [IEEE Xplore](https://ieeexplore.ieee.org/document/9342163)) <p style='text-align: right;'> Dec 2021 </p>
- ‘Portable Gas Detection and Warning System for Olfactory Disabled’ (IEEE INCET, [IEEE Xplore](https://ieeexplore.ieee.org/document/9154120)) <p style='text-align: right;'> Jun 2020 </p>
- ‘Real-Time Asset Tracking using BLE Beacons’ (Global Conference for Advancement in Tech, [IEEE Xplore](https://ieeexplore.ieee.org/document/8978304)) <p style='text-align: right;'> Oct 2019 </p>
