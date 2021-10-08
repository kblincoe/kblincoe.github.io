---
layout: default
title: Service
---

<h2>Journal Board Memberships</h2>
{% for item in site.data.service_journals %}
  <div style="padding-bottom: 10px"><b> {{ item.name }} </b><br>
  {% for entry in item.venues %}
    <i>{{entry.venue}}</i>, {{entry.tenure}}<br>
  {% endfor %}
  </div>
{% endfor %}

<h2>Executive Committee Memberships</h2>
{% for item in site.data.service_exec %}
  <div style="padding-bottom: 10px"><b> {{ item.name }} </b><br>
  {% for entry in item.venues %}
    <i>{{entry.venue}}</i>, {{entry.tenure}}<br>
  {% endfor %}
  </div>
{% endfor %}

<h2>Organizing Committee Memberships</h2>
{% for item in site.data.service_oc %}
  <div style="padding-bottom: 10px"><b> {{ item.name}} </b><br>
  {% for entry in item.venues %}
    <i>{{entry.venue}}</i>, {{entry.tenure}}<br>
  {% endfor %}
  </div>
{% endfor %}

<h2>Program Committee Memberships</h2>
{% for item in site.data.service_pc %}
  <div style="padding-bottom: 10px"><b> {{ item.name}} </b><br>
  {% for entry in item.venues %}
    <i>{{entry.venue}}</i>, {{entry.tenure}}<br>
  {% endfor %}
  </div>
{% endfor %}

<h2>Reviewing</h2>
{% for item in site.data.service_reviewing %}
  <div style="padding-bottom: 0px">{{item.venue}}</div>
{% endfor %}

<br>