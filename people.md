---
title: People
layout: page
title: People
date: 2013-01-19 20:28:10.000000000 +09:00
type: page
author:
  login: bgchun@snu.ac.kr
  email: bgchun@snu.ac.kr
  display_name: bgchun@snu.ac.kr
  first_name: ''
  last_name: ''
permalink: /people/
---

{% assign people_sorted = site.people | sort: 'joined' %}
{% assign role_array = "postdoc|phd|ms|intern|alumni" | split: "|" %}

{% for role in role_array %}

{% assign people_in_role = people_sorted | where: 'position', role %}

<!-- Skip section if there's nobody -->
{% if people_in_role.size == 0 %}
  {% continue %}
{% endif %}

<div class="pos_header">
{% if role == 'postdoc' %}
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

{% if role != 'alumni' %}
<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains role %}
      <div class="list-item-people">
        <p class="list-post-title">
          {% if profile.picture %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="{{site.baseurl}}/images/people/{{profile.avatar}}"></a>
          {% else %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="http://evansheline.com/wp-content/uploads/2011/02/facebook-Storm-Trooper.jpg"></a>
          {% endif %}
          <a class="name" href="{{ site.baseurl }}{{ profile.url }}">{{ profile.name }}</a>
        </p>
      </div>
    {% endif %}
  {% endfor %}
</div>
<hr>

{% endif %}
{% endfor %}