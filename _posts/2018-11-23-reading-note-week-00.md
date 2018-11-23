---
layout: post
title:  "读书笔记_Week_00"
author: xspurs
date: 2018-11-23 23:45:12 +0800
update_date: 2018-11-23 23:45:12 +0800
categories: jekyll update
tags: 读书 读书计划 读书笔记
---

## 2018-11-23

> 《Spark大数据分析_核心概念、技术及实践》

### Chapter_1 大数据技术一览

#### Hadoop

Hadoop Component:

	集群管理器 - YARN(Yet Another Resource Negotiator)
	分布式计算引擎 - MapReduce
	分布式文件系统 - HDFS(Hadoop Distributed File System)

Hadoop由`Doug Cutting`和`Mike Cafarella`在Google三驾马车的其中两篇论文——MapReduce和GFS——的开源实现。

#### HDFS

HDFS将文件分成固定大小的块，默认的块大小为`128M`(可配置)。如果可能，HDFS会把一个文件的各个块分布在不同的机器上，从而可以并行进行读写操作。通过对文件块做副本降低机器宕机风险，默认的副本数量为`3`个。

一个HDFS集群包含两种类型的节点：

	NameNode: 管理元数据
	DataNode: 以block的形式存储实际文件内容

`TODO`:

补充NameNode DataNode之间的交互方式，图
