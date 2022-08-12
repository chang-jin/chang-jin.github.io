---
layout: page
title: Security Analysis and Architecture
date: 2017-04-07 11:50:56.000000000 +09:00
type: page
parent_id: '0'
published: true
password: ''
status: publish
categories: []
author:
  login: sychoi
  email: alicia.sychoi@gmail.com
  display_name: sychoi
  first_name: ''
  last_name: ''
permalink: "/research/security-analysis-and-architecture"
---

We perform research on analyzing mobile applications and malware and coming up with new security architecture for improving mobile security.<br>


<b>App Security Analysis: SMP</b><br>
This project aims to find potential attack vectors and effective solutions for financial applications. As part of our exeperimental study, We apply reverse engineering techniques to apps in order to understand their designs. Based on the insights we gain from the analysis, we study automated tools for generating exploits and defense mechanisms to address such exploits.<br>


<b>App-Centric Security Architecture: ASA</b><br>
Commercial security solutions aim to solve security problems, but have fundamental limitations because the Android security model enforces them as apps running on the platform. In this research, we build the Android App-Centric Security Architecture (ASA), which enables powerful security checks such as scanning app private data and checking URLs before accessing them without compromising the current Android security model. In ASA, apps ask security checks to the mobile security solution (MSS) right before they perform security critical operations to protect themselves. ASA executes the MSS code in an isolated sandbox, thus not exposing apps’ private data to MSS. With ASA, security vendors can deploy more state-of-the-art security techniques and app developers can equip their app a safety catch.<br>


<b>ARM Native Code Information-Flow Tracking: TaintDroid++</b><br>
TaintDroid is an efficient system-wide dynamic taint tracking and analysis system capable of simultaneously tracking multiple sources of sensitive data. TaintDroid leverages Android’s virtualized execution environment and provides taint tracking at the bytecode interpreter level, but there is no support for taint tracking of native code. However, many real-world apps come with third-party native libraries, which TaintDroid cannot handle. TaintDroid++ addresses this limitation by adding native library taint tracking in TaintDroid. The main challenge is how to efficiently track taint flows at the ARM binary level.<br>

