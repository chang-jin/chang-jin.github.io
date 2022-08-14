---
title: People
date: 2013-01-19 20:28:10.000000000 +09:00
author:
  login: bgchun@snu.ac.kr
  email: bgchun@snu.ac.kr
  display_name: bgchun@snu.ac.kr
  first_name: ''
  last_name: ''
permalink: /people/
---

<!-- TODO : sort as joined for students -->
{% assign people = site.people %}
{% assign role_array = "professor|postdoc|phd|ms|intern|alumni" | split: "|" %}

{% for role in role_array %}

{% assign people_in_role = people | where: 'position', role %}

<!-- Skip section if there's nobody -->
{% if people_in_role.size == 0 %}
  {% continue %}
{% endif %}

<div class="pos_header">
  {% if role == 'professor' %}
  <h3 class="people-title">Professor</h3>
  {% elsif role == 'postdoc' %}
  <h3 class="people-title">Postdocs</h3>
  {% elsif role == 'phd' %}
  <h3 class="people-title">Ph.D.  Students</h3>
  {% elsif role == 'ms' %}
  <h3 class="people-title">M.S.  Students</h3>
  {% elsif role == 'intern' %}
  <h3 class="people-title">>Intern</h3><
  {% elsif role == 'alumni' %}
  <h3 class="people-title">Alumni</h3>
  {% endif %}
  <div class="title-sep-container">
    <div class="title-sep"></div>
  </div>
</div>

{% if role == 'professor' %}
  {% assign people_in_role_sorted = people_in_role | sort: 'joined' %}
  {% for profile in people_in_role_sorted %}
<div class="professor_area">
  <p class="list-post-title">
    <div class="one_fourth">
      <img src="{{ profile.picture }}" alt="">
    </div>
    <div class="three_fourth last">
      <div class="person-desc">
        <div class="person-author person-author-dark clearfix">
          <div class="person-author-wrapper">
            <span class="person-name">{{ profile.name }}</span>
            <span class="person-title"></span>
          </div>
          <div class="clear"></div>
        </div>
        <div class="person-content">
          {{ profile.content }}
        </div>
      </div>
    </div>
  </p>
</div>
  {% endfor %}
{% elsif role != 'alumni' %}
<div class="content list people">
  {% assign people_in_role_sorted = people_in_role | sort: 'joined' %}
  {% for profile in people_in_role_sorted %}
    <div class="list-item-people">
      <p class="list-post-title">
        <img class="profile-thumbnail" src="{{profile.picture}}">
        {{ profile.name }}<br><br>
        Email : <a href="mailto:{{ profile.email }}">{{ profile.email }}</a><br>
        {% if profile.pgpkey %}
          <a href="{{ profile.pgpkey }}" target="_blank" rel="noopener noreferrer">(PGP key)</a><br>
        {% endif %}
        {% if profile.homepage %}
          Homepage : <a href="{{ profile.homepage }}" target="_blank" rel="noopener noreferrer">{{ profile.homepage }}</a><br>
        {% endif %}
      </p>
    </div>
  {% endfor %}
</div>
{% elsif role == 'alumni' %}
<div class="content list people">
  {% assign people_in_role_sorted = people_in_role | sort: 'order' | reverse %}
  {% for profile in people_in_role_sorted %}
    <div class="list-item-people">
      <p class="list-post-title">
        <img class="profile-thumbnail" src="{{ profile.picture }}">
        <span class="person-name">{{ profile.name }}</span><br><br>
        {{ profile.content }}
        Email : <a href="mailto:{{ profile.email }}">{{ profile.email }}</a><br>
        {% if profile.pgpkey %}
          <a href="{{ profile.pgpkey }}" target="_blank" rel="noopener noreferrer">(PGP key)</a><br>
        {% endif %}
        {% if profile.homepage %}
          Homepage : <a href="{{ profile.homepage }}" target="_blank" rel="noopener noreferrer">{{ profile.homepage }}</a><br>
        {% endif %}
      </p>
    </div>
  {% endfor %}
</div>
{% endif %}
<div class="space"></div>
{% endfor %}
