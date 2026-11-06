---
layout: default
title: Home
---
<div class="home">
    <div class="row">
      <div class="col-md-5">
        <img class="rounded img-fluid" src="./imgs/Kelly_Blincoe.jpg" alt="Prof Kelly Blincoe"><br>
      </div>
      <div class="col-md-7">    
      <h1 class="text-primary mb-4">Kia ora, I'm Kelly Blincoe</h1>

      <p>I study how people create and maintain software systems. I am a Rutherford Discovery Fellow and a Professor of Software Engineering at the University of Auckland, New Zealand in the <a href="https://hasel.auckland.ac.nz/" target="_blank">Human Aspects of Software Engineering Lab (HASEL)</a>, in the Department of Electrical, Computer, and Software Engineering. I lead the <a href="https://engclusion.nz" target="_blank">ENGclusion</a> research programme.</p>

      <div style="text-align: center;"><a href="/about.html" style="font-family: 'Homemade Apple', cursive; font-size: 150%;">More about me</a></div>
  </div>

  <h2 class="h4 mt-5">Recent news</h2>
  <ul class="news list-unstyled">
  {% for item in site.data.news limit: 5 %}
    <li class="mb-2">
      <span class="text-muted">{{ item.date | date: "%b %Y" }}</span>
      <span>
        {{ item.text | markdownify | remove: '<p>' | remove: '</p>' }}
        {% if item.pub %}<a href="/publications.html#{{ item.pub }}">Details.</a>{% endif %}
      </span>
    </li>
  {% endfor %}
  </ul>

</div>