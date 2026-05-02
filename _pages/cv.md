---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* Ph.D, The Hong Kong Polytechnic University, Hong Kong
  * Supervisor: Prof. Kainam Thomas Wang

Work Experience
======
* July 2022 – 2026: Lead Data Scientist
  * C3.ai, Singapore

* 2016 – 2022: Senior Research Fellow
  * Nanyang Technological University, Singapore
  * Supervisor: Prof. Tay Wee Peng

* 2014 – 2016: Postdoctoral Researcher
  * University of Paderborn, Germany
  * Supervisor: Prof. Peter Schreier

Publications
======
  <ul>{% for post in site.publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
