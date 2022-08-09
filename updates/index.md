---
layout: page
title: Updates
date: 2012-08-08 02:54:23.000000000 +09:00
type: page
parent_id: '0'
published: true
password: ''
status: publish
categories: []
author:
  login: bgchun@snu.ac.kr
  email: bgchun@snu.ac.kr
  display_name: bgchun@snu.ac.kr
  first_name: ''
  last_name: ''
permalink: "/updates/"
---

<div>
{% for post in site.posts %}
  {% assign currentdate = post.date | date: "%Y" %}
  {% if currentdate != date %}
    <h2 id="y{{currentdate}}">{{ currentdate }}</h2>
    {% assign date = currentdate %}
  {% endif %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</div>
