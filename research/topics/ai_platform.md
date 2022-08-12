---
layout: page
title: Artificial Intelligence Platform and Algorithm
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
permalink: "/research/artificial-intelligence-platform"
---

<h3 class="topics_title">Nimble: Lightweight and Efficient GPU Task Scheduling for Deep Learning</h3>
<p>
Deep learning (DL) frameworks take advantage of GPUs to improve performance of DL inference and training. We observe that as DL operations take less time on a GPU, the framework overhead affects the overall running time more significantly. We propose Nimble, a system that automatically avoids such framework overheads and parallelizes GPU kernels using multiple streams for static DL models. Nimble introduces ahead-of-time (AoT) scheduling with automatic multi-stream assignment. Nimble automates applying these techniques by capturing the GPU kernel call trace and running only GPU kernel calls for execution. Our evaluations on various deep neural networks show that Nimble improves the speed of inference and training by up to 22.34× and 3.61× compared to PyTorch, respectively. Furthermore, Nimble outperforms TensorRT by up to 2.8x for inference. We are working to enhance Nimble to further optimize DNN execution on GPUs.</p>