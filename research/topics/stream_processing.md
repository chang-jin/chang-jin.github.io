---
layout: page
title: Stream Processing
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
permalink: "/research/stream-processing"
---
Stream processing systems are widely used to execute stream queries that extract useful information from data streams at real-time. We focus on a new stream processing system that handles excessive number of stream queries efficiently. Our approach for the efficient execution is to reduce query maintenance overhead, duplicated computations, and imbalance of loads among distributed nodes.   
MIST:
IoT-related services such as IFTTT and Fitbit, which handle user requests based on data gathered from IoT devices, are thriving these days. These services require processing of a large number of highly personalized continuous queries. Existing stream processing frameworks, such as Flink and Spark Streaming, are not suitable for handling a bunch of stream queries. Instead, they are designed to process small number of “big stream queries”, which process big data streams in distributed cluster, thus isolating each stream queries with high maintenance overheads. We design a new stream processing system, MIST, that enables processing billions of IoT stream queries. MIST provides a new execution model and various optimization techniques to achieve this goal.
[source_code](https://github.com/snuspl/mist)