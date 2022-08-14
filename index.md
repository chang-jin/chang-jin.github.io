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
      {% assign currentdate = post.date | date: "%B %-d, %Y" %}
      <div class="update_contents">
        <a href="{{ post.permalink }}">{{ post.title }}</a>
      </div>
      <div class="update_date">{{ currentdate }}</div>
    {% endfor %}
  </div>
</div>

<style>
.topics_title {
    color: #3366ff;
}

.main_page {
    display: flex;
    flex-direction: row;
    width: "100%";
}

.main_first_column {
    width: "65%";
}

.main_second_column {
    padding-left: 1rem;
    flex-grow: 1;
}

.reading_box {
    padding: 1rem;
    font-size: 1rem;
    background-color: #f6f6f6;
    border-left-width: 3px;
    border-left-color: #12a5f4;
    border: 0px solid #f6f6f6;
    font-size: 18px;
    font-family: Tahoma, sans-serif;
    color: #333333;
}

.update_title {
    font-family: "Montserrat", Arial, Helvetica, sans-serif;
    color: #333333;
    line-height: 27px;
}

.update_date {
    font: 12px/14px 'PTSansItalic', arial, helvetica, sans-serif;
    color: #747474;
    font-style: italic;
    margin-block-start: 1em;
    margin-block-end: 1em;
}

.update_contents {
      color: #333333;
      font-size: 13px;
      font-family: "Montserrat", Arial, Helvetica, sans-serif;
}
</style>
