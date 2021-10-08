---
layout: default
title: Students
---
<h2>Current Students</h2>
{% for item in site.data.students %}
   <div style="padding-bottom: 0px">{{item.name}}, {{item.degree}}</div>
{% endfor %}

<h2>Alumni</h2>
{% for item in site.data.alumni %}
   {{item.name}}, {{item.degree}}, {{item.year}}<br>
   <i>Thesis: </i>{{item.thesis}}
{% endfor %}

<h2>Thesis Examination Committee Member</h2>
{% for item in site.data.examinations %}
   <div style="padding-bottom: 0px">{{ item.student }}</div>
{% endfor %}

<br>