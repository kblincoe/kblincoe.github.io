---
layout: default
title: Service
---
Part of my job includes national and international service. I hold many leadership positions in the software engineering research community.

<h2 class="text-primary">Journal Board Memberships</h2>
{% for item in site.data.service_journals %}
  <div style="padding-bottom: 10px"><b> {{ item.name }} </b><br>
  {% for entry in item.venues %}
    <i>{{entry.venue}}</i>, {{entry.tenure}}<br>
  {% endfor %}
  </div>
{% endfor %}

<h2 class="text-primary">Executive Committee Memberships</h2>
{% for item in site.data.service_exec %}
  <div style="padding-bottom: 10px"><b> {{ item.name }} </b><br>
  {% for entry in item.venues %}
    <i>{{entry.venue}}</i>, {{entry.tenure}}<br>
  {% endfor %}
  </div>
{% endfor %}

<h2 class="text-primary">Organizing Committee Memberships</h2>
{% for item in site.data.service_oc %}
  <div style="padding-bottom: 10px"><b> {{ item.name}} </b><br>
  {% for entry in item.venues %}
    <i>{{entry.venue}}</i>, {{entry.tenure}}<br>
  {% endfor %}
  </div>
{% endfor %}

<h2 class="text-primary">Program Committee Memberships</h2>
{% for item in site.data.service_pc %}
  <div style="padding-bottom: 10px"><b> {{ item.name}} </b><br>
  {% for entry in item.venues %}
    <i>{{entry.venue}}</i>, {{entry.tenure}}<br>
  {% endfor %}
  </div>
{% endfor %}

<h2 class="text-primary">Reviewing</h2>
{% for item in site.data.service_reviewing %}
  <div style="padding-bottom: 0px">{{item.venue}}</div>
{% endfor %}