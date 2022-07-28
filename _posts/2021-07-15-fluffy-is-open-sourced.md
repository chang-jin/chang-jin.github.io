---
layout: post
title: Fluffy is open sourced!
date: 2021-07-15 17:19:48.000000000 +09:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories: []
tags: []
meta:
  pyre_header_bg_repeat: repeat
  avada_post_views_count: '462'
  slide_template: default
  sbg_selected_sidebar: a:1:{i:0;s:1:"0";}
  sbg_selected_sidebar_replacement: a:1:{i:0;s:1:"0";}
  pyre_header_bg_full: 'no'
  pyre_header_bg_color: ''
  pyre_header_bg: ''
  pyre_wide_page_bg_repeat: repeat
  pyre_wide_page_bg_full: 'no'
  pyre_wide_page_bg_color: ''
  pyre_wide_page_bg: ''
  pyre_page_bg_repeat: repeat
  pyre_page_bg_full: 'no'
  pyre_page_bg_color: ''
  pyre_page_bg: ''
  pyre_page_bg_layout: default
  pyre_fallback: ''
  pyre_elasticslider: '0'
  pyre_revslider: '0'
  pyre_flexslider: '0'
  pyre_wooslider: '0'
  pyre_slider: '0'
  pyre_slider_type: 'no'
  pyre_related_posts: 'yes'
  pyre_link_icon_url: ''
  pyre_image_rollover_icons: linkzoom
  pyre_fimg_height: ''
  pyre_fimg_width: ''
  pyre_sidebar_position: default
  pyre_full_width: 'no'
  pyre_video: ''
  pyre_page_title_text: 'yes'
  pyre_page_title: 'yes'
  _edit_last: '1'
  pyre_page_title_custom_text: ''
  pyre_page_title_custom_subheader: ''
  pyre_page_title_height: ''
  pyre_page_title_bar_bg: ''
  pyre_page_title_bar_bg_retina: ''
  pyre_page_title_bar_bg_full: default
  pyre_page_title_bar_bg_color: ''
  pyre_page_title_bg_parallax: default
  _intelliwidget_widget_page_id: '0'
author:
  login: bgchun@snu.ac.kr
  email: bgchun@snu.ac.kr
  display_name: bgchun@snu.ac.kr
  first_name: ''
  last_name: ''
permalink: "/2021/07/15/fluffy-is-open-sourced/"
---
<p>We made Fluffy publicly available at <a href="https://github.com/snuspl/fluffy">https://github.com/snuspl/fluffy</a>. Fluffy is a multi-transaction differential fuzzer for finding consensus bugs in Ethereum. Fluffy mutates and executes multi-transaction test cases to find consensus bugs which cannot be found using existing fuzzers for Ethereum. Fluffy found two new consensus bugs, the shallow copy bug (CVE-2020-26241) and the tranfer-after-destruct bug, in the most popular Geth Ethereum client which were exploitable on the live Ethereum mainnet. Four months after we reported the bugs to Geth developers, one of the bugs was triggered on the mainnet, and caused nodes using a stale version of Geth to hard fork the Ethereum blockchain. The blockchain community considers this hard fork the greatest challenge since the infamous 2016 DAO hack. For details, please refer to our OSDI 2021 paper.</p>
