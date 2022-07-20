---
layout: default
title: Invited Talks
---

<h2 class="text-primary">Invited Talks</h2>
{% for item in site.data.talks %}
  <div style="padding-bottom: 10px"> <b>{{item.title}}</b><br>
  <i>{{item.venue}}</i><br>
  {{item.type}}, {{item.year}}<br>
  {% if item.slides %}
  <span><a href="{{ item.slides }}" target="_blank">Slides</a></span>
  {% endif %}
  {% if item.video %}
  <span>&nbsp;&middot;&nbsp;&nbsp;<a href="{{ item.video }}" target="_blank">Video</a></span>
  {% endif %}
  </div>
{% endfor %}