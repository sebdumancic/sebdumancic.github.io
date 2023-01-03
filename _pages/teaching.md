---
layout: page
permalink: /teaching/
title: teaching
description: 
nav: true
nav_order: 5
display_categories: [course, tutorial]
---


<!-- pages/projects.md -->
<div class="projects">
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.courses | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include course.html %}
    {%- endfor %}
  </div>
  {% endfor %}

</div>
<br><br>

## Supervised Master theses



## Science popularisation
For years I've been involved with the [Summer School of Science](http://drustvo-evo.hr/s3/){:target="\_blank"} in Croatia - a science-popularisation project for high-school students. If you know, or have, a high-schooler interested in science, please check this program out!

