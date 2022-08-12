---
layout: page
title: Research Projects
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
permalink: "/research/big-data-processing"
---

In recent years, the data processing system domain has evolved for a wide variety of resource and job characteristics. However, it is hard to evolve current data processing systems to adapt to applications with new resources and job characteristics. To address this problem, we build a flexible and extensible data processing system, and design various instantiation policies for the system.

<h3 class="topics_title">Apache Nemo</h3>
Nemo is a data processing system for flexible employment with different execution scenarios for various deployment characteristics on clusters. They include processing data on specific resource environments, like on transient resources, and running jobs with specific attributes, like skewed data. Nemo decouples the logical notion of data processing applications from runtime behaviors and expresses them on separate layers using the Nemo IR. Specifically, through a set of high-level graph pass interfaces, Nemo exposes runtime behaviors to be flexibly configured and modified at both compile-time and runtime, and the Nemo Runtime executes the Nemo IR with its modular and extensible design.
[source code](https://github.com/apache/incubator-nemo)

<h3 class="topics_title">Fast and Efficient Data Processing on Local and Global Caching Storage</h3>
Modern data analytics systems allow caching intermediate data into their local caching storage to reduce duplicate computations and improve performance. However, with the growing volumes of data, cached data eviction is inevitable when the system’s local caching storage (e.g., memory or disk) becomes full. Existing systems face performance degradations due to the large recomputation overheads caused by evicted data. We have been building a system that effectively minimizes data eviction and reduces recomputation overheads by performing to perform caching decisions on two-tiered local and global caching storage based on eviction costs.

<h3 class="topics_title">Planet-scale real-time data processing for geo-distributed data centers</h3>
We are working on a real-time data analysis infrastructure for geo-distributed data centers (e.g., OpenNetLab) in collaboration with Microsoft Research. With global IT companies expanding out to different parts of the globe, geo-distributed data are becoming more common, and the importance for processing such data is growing rapidly. Nevertheless, existing data processing systems are tailored for clusters that are connected with fast local area networks, and do not handle slow unstable wide-area networks effectively. To overcome the problems that arise with the dynamically changing environments for global stream processing workloads under heterogeneous network bandwidths, we dynamically profile and restructure data processing structures according to their network connection statuses. This acts as a basis to reconfigure our stream processing system adaptively during the execution by scheduling stream processing tasks with the consideration of the network connections to fully leverage the provided resource environments, to maximize the job throughput and minimize the job latency.

<h3 class="topics_title">Stream processing on persistent storage</h3>
Stream processing has been widely used in big data analytics because it provides real-time information on continuously incoming data streams with low latency. As the volume of data streams becomes larger and the application logic becomes more complicated, the size of internal states in stream processing applications also increases. To deal with large states efficiently, modern stream processing systems support storing internal states on solid state drives (SSDs) by utilizing persistent key-value (KV) stores. However, delegating state management to persistent KV stores degrades the performance, because the KV stores cannot optimize their state management strategies according to stream query semantics as they are not aware of the query semantics. To solve this problem, we design a persistent store customized for stream analytics that exploits window semantics.

<h3 class="topics_title">Pado</h3>
Datacenters are under-utilized, primarily due to unused resources on over-provisioned nodes of latency-critical jobs. Such idle resources can be used to run batch data analytic jobs to increase datacenter utilization, but these transient resources must be evicted whenever latency-critical jobs require them again. To solve this problem, we focus on observing the job structure and the relationships between the computations of the job. We carefully mark the computations that are most likely to cause a large number of recomputations upon evictions, to run them reliably using eviction-free reserved resources. This lets us retain corresponding intermediate results effortlessly without any additional checkpointing. We design Pado, a general data processing engine, which carries out our idea with several optimizations that minimize the number of additional reserved nodes.

<b>Publication</b>
<li>Youngseok Yang, Jeongyoon Eo, Geon-Woo Kim, Joo Yeon Kim, Sanha Lee, Jangho Seo, Won Wook Song, Byung-Gon Chun. Apache Nemo: A Framework for Building Distributed Dataflow Optimization Policies. ATC 2019, July 2019.</li>
<li>Woo-Yeon Lee, Yunseong Lee, Joo Seong Jeong, Gyeong-In Yu, Joo Yeon Kim, Ho Jin Park, Beomyeol Jeon, Wonwook Song, Gunhee Kim, Markus Weimer, Brian Cho, Byung-Gon Chun. Automating System Configuration of Distributed Machine Learning. ICDCS 2019, July 2019.</li>
<li>Gyewon Lee, Jeongyoon Eo, Jangho Seo, Taegeon Um, and Byung-Gon Chun. High-Performance Stateful Stream Processing on Solid-State Drives, ApSys, August 2018.</li>
<li>Youngseok Yang, Geon-Woo Kim, Won Wook Song, Yunseong Lee, Andrew Chung, Zhengping Qian, Brian Cho, Byung-Gon Chun. Pado: A Data Processing Engine for Harnessing Transient Resources in Datacenters, EuroSys, April 2017.</li>
