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
tags: []
meta:
  pyre_portfolio_category: '0'
  pyre_slider: '0'
  pyre_email: ''
  pyre_address: ''
  pyre_phone: ''
  pyre_gmap: ''
  _wp_page_template: full-width.php
  avada_post_views_count: '0'
  pyre_page_title: 'no'
  pyre_slider_type: 'no'
  pyre_wooslider: '0'
  pyre_sidebar_position: right
  pyre_fallback: ''
  pyre_elasticslider: '0'
  pyre_revslider: '0'
  pyre_flexslider: '0'
  pyre_page_bg_color: ''
  pyre_page_bg: ''
  pyre_page_bg_full: 'no'
  pyre_page_bg_repeat: repeat
  pyre_page_title_bar_bg: ''
  pyre_full_width: 'no'
  pyre_page_title_bar_bg_color: ''
  pyre_portfolio_excerpt: ''
  pyre_portfolio_full_width: 'yes'
  pyre_portfolio_sidebar_position: default
  pyre_portfolio_filters: 'yes'
  pyre_page_bg_layout: default
  pyre_wide_page_bg: ''
  pyre_wide_page_bg_color: ''
  pyre_wide_page_bg_full: 'no'
  pyre_wide_page_bg_repeat: repeat
  pyre_header_bg: ''
  pyre_header_bg_color: ''
  pyre_header_bg_full: 'no'
  pyre_header_bg_repeat: repeat
  pyre_page_title_text: 'yes'
  pyre_page_title_bar_bg_retina: ''
  pyre_page_title_bar_bg_full: 'no'
  pyre_image_rollover_icons: linkzoom
  pyre_link_icon_url: ''
  slide_template: default
  _oembed_e4bedd07bb4eabc3c300a2d035ff9aec: "{{unknown}}"
  _oembed_d2f63908ece0e5c64864ca1caf380d6a: "{{unknown}}"
  _edit_last: '1'
  pyre_main_top_padding: ''
  pyre_main_bottom_padding: ''
  pyre_hundredp_padding: ''
  pyre_page_title_custom_text: ''
  pyre_page_title_custom_subheader: ''
  pyre_page_title_height: ''
  pyre_page_title_bg_parallax: default
  _intelliwidget_widget_page_id: '0'
  _oembed_aca1f122200e7c12cc7edc8d219ff574: "{{unknown}}"
  sbg_selected_sidebar_replacement: a:1:{i:0;s:1:"0";}
  sbg_selected_sidebar: a:1:{i:0;s:1:"0";}
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
    <img src="./assets/resources/spl_landing_logo.png">SPL Landing Logo</img>
    <section
      class="reading-box "
      style="">
        At Software Platform Lab (SPL), we work on machine learning systems and algorithms, and data processing systems. We publish our research work at top venues in systems, database, and artificial intelligence. We also contribute to open-source software projects actively.
    </section>
  </div>
  <div class="main_second_column">
    <h2>Latest Updates</h2>
    {% for post in site.posts limit: 6 %}
      {{ post.content }}
    {% endfor %}
  </div>
</div>
