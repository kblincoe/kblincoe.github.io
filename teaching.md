---
layout: default
title: Teaching
---
<div class="readable">

<p>I teach Software Engineering at the University of Auckland. My courses cover topics mostly related to collaborative software development and software requirements engineering. Below is a list of courses that I have taught in my current and previous academic positions. </p>

<h2 class="text-primary">Courses Taught</h2>
{% for item in site.data.teaching %}
  <div style="padding-bottom: 10px"> <b>{{item.name}}</b><br>
  <i>{{item.place}}</i><br>
  {{item.years}}</div>
{% endfor %}

</div>