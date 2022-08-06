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
tags: []
meta:
  pyre_portfolio_filters: 'yes'
  pyre_portfolio_sidebar_position: default
  pyre_portfolio_full_width: 'yes'
  pyre_portfolio_excerpt: ''
  pyre_full_width: 'no'
  pyre_fallback: ''
  pyre_elasticslider: '0'
  pyre_main_top_padding: ''
  avada_post_views_count: '3'
  pyre_wide_page_bg: ''
  pyre_wide_page_bg_full: 'no'
  pyre_page_bg_layout: default
  pyre_wide_page_bg_color: ''
  pyre_wide_page_bg_repeat: repeat
  pyre_header_bg: ''
  pyre_header_bg_color: ''
  pyre_header_bg_full: 'no'
  pyre_header_bg_repeat: repeat
  pyre_page_title_text: 'yes'
  pyre_page_title_bar_bg_retina: ''
  pyre_page_title_bar_bg_color: ''
  pyre_page_title_bar_bg_full: 'no'
  pyre_image_rollover_icons: linkzoom
  pyre_link_icon_url: ''
  _wp_page_template: default
  pyre_gmap: ''
  pyre_sidebar_position: right
  pyre_slider: '0'
  pyre_page_title: 'yes'
  pyre_slider_type: 'no'
  pyre_wooslider: '0'
  pyre_flexslider: '0'
  pyre_revslider: '0'
  pyre_page_bg_color: ''
  pyre_page_bg: ''
  pyre_page_bg_full: 'no'
  pyre_page_bg_repeat: repeat
  pyre_page_title_bar_bg: ''
  slide_template: default
  sbg_selected_sidebar_replacement: a:1:{i:0;s:12:"Blog Sidebar";}
  _edit_last: '1'
  pyre_main_bottom_padding: ''
  pyre_hundredp_padding: ''
  pyre_page_title_custom_text: ''
  pyre_page_title_custom_subheader: ''
  pyre_page_title_height: ''
  pyre_page_title_bg_parallax: default
  sbg_selected_sidebar: a:1:{i:0;s:1:"0";}
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
