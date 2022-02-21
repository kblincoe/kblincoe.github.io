---
layout: default
title: Students
---
Interested in doing a PhD? Check out the <a href="https://www.auckland.ac.nz/en/study/study-options/find-a-study-option/software-engineering/doctoral.html" target="_blank">Software Engineering PhD programme</a> at the University of Auckland, where you will find details on how to apply. If you do apply and want to work with me, in the application make sure to choose Software Engineering (in the Faculty of Engineering) and put my name as the primary supervisor. You can also email me if you want to discuss your research interests and how they might fit with my group (this is optional). Also check out the <a href="https://hasel.auckland.ac.nz" target="_blank">HASEL website</a> to learn more about our team and current projects. A PhD in New Zealand typically takes 3-4 years. <br><br>

<h2 class="text-primary">Current Students</h2>
{% for item in site.data.students %}
   <div style="padding-bottom: 0px">{{item.name}}, {{item.degree}}</div>
{% endfor %}<br>

<h2 class="text-primary">Alumni</h2>
{% for item in site.data.alumni %}
   {{item.name}}, {{item.degree}}, {{item.year}}<br>
   <i>Thesis: </i>{{item.thesis}}
{% endfor %}

<h2 class="text-primary">Thesis Examination Committee Member</h2>
{% for item in site.data.examinations %}
   <div style="padding-bottom: 0px">{{ item.student }}</div>
{% endfor %}

<br>