---
layout: post
title:  "读书笔记_Week_01"
author: xspurs
date: 2018-11-26 23:25:12 +0800
update_date: 2018-11-28 23:15:12 +0800
categories: jekyll update
tags: 读书 读书计划 读书笔记
---

## 2018-11-26_Mon

> 《Spark大数据分析_核心概念、技术及实践》
>
> [豆瓣链接](https://book.douban.com/subject/27061727/)

### Chapter_1 大数据技术一览

#### Hadoop

##### MapReduce

MapReduce是Hadoop提供的分布式计算引擎，它自动在集群中的各计算机上调度应用的执行，并处理负载均衡、节点宕机和复杂的节点内通信。

MapReduce应用的基本组成是两个函数：`map`和`reduce`，名称借鉴于函数式编程。map函数以key-value作为输入，输出中间结果(格式也为key-value)。reduce函数聚合这些值，输出最终结果。

##### Hive

Hive提供了类SQL的方式来处理HDFS或其他兼容Hadoop的存储系统(如Cassandra和Amazon S3)中的数据。SQL比Java和其他用来便携MapReduce的编程语言更易学，通过Hive引入的类SQL(HiveQL)，人们可以更方便的使用MapReduce来处理数据，即HiveQL会被转换成MapReduce作业。

Hive支持`UDF`(User Defined Function，用户自定义函数)和UDAF(User Defined Aggregation Function，用户定义聚合函数)，从而有效补充、增强HiveQL的表达能力。

#### 数据序列化

##### Avro

Avro支持多种数据格式，包括嵌套数据格式。

Avro使用一种自描述的二进制格式，使用Avro序列化数据时，模式与数据同时存储，从而写数据时没有关于值的简介开销`(?)`。Avro模式使用JSON描述。

Avro自动处理字段的添加和删除、前向和后向兼容性，这些不需要应用程序来负责。

###### Thrift

略。

##### Protocol Buffers

相对于Thrift，Protocol Buffers主要用于数据序列化，但并不限定RPC方式。

##### SequenceFile

SequenceFile是一种用于存储key-value的二进制文件格式，通常作为Hadoop的输入和输出文件格式。MapReduce也使用SequenceFile来存储map函数返回的中间结果。

SequenceFile有三种不同的格式：

- 未压缩格式
- 记录压缩格式：只压缩value
- 块压缩格式：key与value均压缩

## 2018-11-28_Tue

休息。

## 2018-11-28_Wed

加班工作。
