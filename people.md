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

{% assign people_sorted = site.people | sort: 'joined' %}
{% assign role_array = "professor|postdoc|phd|ms|intern|alumni" | split: "|" %}

{% for role in role_array %}

{% assign people_in_role = people_sorted | where: 'position', role %}

<!-- Skip section if there's nobody -->
{% if people_in_role.size == 0 %}
  {% continue %}
{% endif %}

<div class="pos_header">
    {% if role == 'professor' %}
    <h3>Professor</h3>
    {% elsif role == 'postdoc' %}
    <h3>Postdocs</h3>
    {% elsif role == 'phd' %}
    <h3>Ph.D.  Students</h3>
    {% elsif role == 'ms' %}
    <h3>M.S.  Students</h3>
    {% elsif role == 'intern' %}
    <h3>Intern</h3>
    {% elsif role == 'alumni' %}
    <h3>Alumni</h3>
    {% endif %}
</div>

{% if role == 'professor' %}
{% for profile in people_sorted %}
{% if profile.position contains role %}
<div class="professor_area">
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
                <p>
                Associate Professor, Computer Science and Engineering Department, Seoul National University<br>
                Associate Director, Artificial Intelligence Institute, Seoul National University<br>
                Co-lead, SNU-Naver Hyperscale AI Center<br>
                CEO, FriendliAI<br>
                Email : <a href="mailto:{{ profile.email }}">{{ profile.email }}</a> <a href="{{ profile.pgpkey }}" target="_blank" rel="noopener noreferrer">(PGP key)</a><br>
                Homepage : <a href="{{ profile.homepage }}" target="_blank" rel="noopener noreferrer">{{ profile.homepage }}</a>
                </p>
                <p>Education<br>
                2007: Ph.D. Computer Science, University of California, Berkeley<br>
                2002: M.S. Computer Science, Stanford University<br>
                1996: M.S. Electronic Engineering, Seoul National University<br>
                1994: B.S. Electronic Engineering, Seoul National University</p>
                <p>Experience<br>
                2020: Visiting Researcher, Naver<br>
                2016: Research Scientist, Facebook Menlo Park<br>
                2012-2013: Principal Scientist, Microsoft Silicon Valley<br>
                2011-2012: Research Scientist, Yahoo! Research Silicon Valley<br>
                2008-2011: Research Scientist, Intel Research Berkeley<br>
                2007-2008: Postdoctoral Researcher, International Computer Science Institute<br>
                </p>
            </div>
        </div>
    </div>
</div>
<hr>
<div id="clear" style="clear:both;"></div>
{% endif %}
{% endfor %}
{% elsif role != 'alumni' %}
<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains role %}
      <div class="list-item-people">
        <p class="list-post-title">
          {% if profile.picture %}
            <img class="profile-thumbnail" src="{{profile.picture}}">
          {% else %}
            <img class="profile-thumbnail" src="http://evansheline.com/wp-content/uploads/2011/02/facebook-Storm-Trooper.jpg">
          {% endif %}
          {{ profile.name }}<br>
          Email :&nbsp;<a href="mailto:{{ profile.email }}">{{ profile.email }}</a>&nbsp;<a href="{{ profile.pgpkey }}" target="_blank" rel="noopener noreferrer">(PGP key)</a><br>
          Homepage :&nbsp;<a href="{{ profile.homepage }}" target="_blank" rel="noopener noreferrer">{{ profile.homepage }}</a>
        </p>
      </div>
    {% endif %}
  {% endfor %}
</div>
<hr>
<div id="clear" style="clear:both;"></div>
{% endif %}


{% endfor %}
