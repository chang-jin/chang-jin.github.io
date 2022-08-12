---
layout: page
title: Home
date: 2012-07-30 23:32:32.000000000 +09:00
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
permalink: "/"
---

<div class="main_page">
  <div class="main_first_column">
    <img src="./assets/resources/spl_landing_logo.png">
    <div class="reading_box">
        At Software Platform Lab (SPL), we work on machine learning systems and algorithms, and data processing systems. We publish our research work at top venues in systems, database, and artificial intelligence. We also contribute to open-source software projects actively.
    </div>
  </div>
  <div class="main_second_column">
    <h3>Latest Updates</h3>
    {% for post in site.posts limit: 6 %}
      {% assign currentdate = post.date | date: "%d %B, %Y" %}
      <div class="update_contents">{{ post.title }}</div>
      <div class="update_date">{{ currentDate }}</div>
    {% endfor %}
  </div>
</div>

<style>
.topics_title {
    color: #3366ff;
}

.main_page {
    flex-direction: row;
    width: 100%;
}

.main_first_column {
    width: 65%;
}

.main_second_column {
}

.reading_box {
    margin: 3px;
    font-size: 1.2rem;
    background-color: #f6f6f6;
    border-left-width: 3px;
    border-left-color: #12a5f4;
    border: 0px solid #f6f6f6;
}
</style>