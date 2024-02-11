---
title: "Sharded KV Storage and Distributed Transactions"
description: "Implemented the concept of sharding and two-phase locking"
dateString: Sep 2019 - Oct 2019
draft: false
tags: ["C++", "Sharding", "Two-Phase Commit", "Two-Phase Locking", "Optimistic Concurrency Control", "Cross-Shard Transactions"]
showToc: false
weight: 203
cover:
    image: "projects/shard/shard1.png"
--- 
## Description

I designed and built a **sharded** and **distributed key-value storage system** in **C++** for horizontal scalability. The data is partitioned across multiple shards, each comprised of replica groups managed by a shard master using **Raft consensus** for fault tolerance. I implemented Join, Leave, Move and Query RPCs to handle dynamic reconfiguration and data migration when scaling capacity. The system provides **linearizability** and continuity during shard migrations.

![](/projects/shard/shard2.png)

A key innovation was enabling **cross-shard distributed transactions** using **two-phase commit** and **optimistic concurrency control**. The client coordinates the 2PC process across shards, obtaining locks in the prepare phase to ensure **atomicity** and **isolation**. Versions are attached to values to detect conflicting concurrent writes. This provides strong consistency guarantees for operations spanning multiple shards.

![](/projects/shard/occ.png)

This project demonstrates my expertise in distributed systems and large-scale datastores. The sharded architecture, fault tolerance, and cross-shard transactions allow the key-value store to provide high availability, strong consistency, and seamless scaling to meet demand. I leveraged modern C++ along with systems design patterns to deliver a robust and production-ready datastore.
