# Spark 概述

## 一.Spark 是什么？

● 官方文档解释：Apache Spark™ is a fast and general engine for large-scale data processing.

通俗的理解：Spark是基于内存计算的大数据并行计算框架。Spark基于内存计算，提高了在大数据环境下数据处理的实时性，同时保证了高容错性和高可伸缩性，允许用户将Spark 部署在大量廉价硬件之上，形成集群。

● 扩展了MapReduce计算模型；相比与MapReduce编程模型，Spark提供了更加灵活的DAG（Directed Acyclic Graph） 编程模型， 不仅包含传统的map、reduce接口， 还增加了filter、flatMap、union等操作接口，使得编写Spark程序更加灵活方便。

● 高效支持多种计算模式；Spark 不仅可以做离线运算，还可以做流式运算以及迭代式运算。

## 二.Spark 组成---大一统软件栈

![img](http://ke.dajiangtai.com/content/1901/1.png)

#### 2.1 Spark Core

● Spark Core 实现了Spark 的基本功能，包含任务调度、内存管理、错误恢复、与存储系统交互等模块。

● RDD（resilient distributed dataset，弹性分布式数据集）的API 定义。RDD是一个抽象的数据集，提供对数据并行和容错的处理。初次使用RDD时，其接口有点类似Scala的Array，提供map，filter，reduce等操作。但是，不支持随机访问。刚开始不太习惯，但是逐渐熟悉函数编程和RDD 的原理后，发现随机访问数据的场景并不常见。

#### 2.2 Spark SQL

● Spark SQL 是Spark 用来操作结构化数据的程序包。

● Spark SQL 直接兼容Hive SQL。

● 多数据源（Hive表、Parquet、JSON等）；Spark SQL 可以操作Hive表，可以读取Parquet文件(列式存储结构)，可以读取JSON文件，还可以处理hdfs上面的文件。

● SQL与RDD编程结合使用。

● 从Shark演变到Spark SQL。

#### 2.3 Spark Streaming

● Spark 提供的对实时数据进行流式计算的组件。

● 微批处理(Storm、Flink)—从批处理到流处理

#### 2.4 Spark MLlib

● Spark 提供的包含常见机器学习（ML）功能的库。

● 分类、回归、聚类、协同过滤等

● 模型评估、数据导入等额外的支持功能

● Mahout(Runs on distributed Spark, H2O, and Flink)

#### 2.5 GraphX

● GraphX是Spark 提供的图计算和图挖掘的库。

● 与Spark Streaming 和Spark SQL 类似，GraphX 也扩展了Spark 的RDD API，能用来创建一个顶点和边都包含任意属性的有向图

● GraphX还支持针对图的各种计算和常见的图算法。

## 三.Spark与Hadoop的关系

#### 3.1 Spark与Hadoop的关系---青于于蓝

![img](http://ke.dajiangtai.com/content/1901/2.png)

#### 3.2 Spark与Hadoop的关系---相辅相成

![img](http://ke.dajiangtai.com/content/1901/3.png)

#### 3.3 Spark的竞争对手---Flink

![img](http://ke.dajiangtai.com/content/1901/4.png)

![img](http://ke.dajiangtai.com/content/1901/5.png)

● Flink是先有流处理后有批处理

● Pipeline vs Stage

● http://note.youdao.com/share/?id=f3b0a1832e4ee43e3e3635913d5e00e1&type=note

#### 3.4 Spark的竞争对手---Storm/JStorm

![img](http://ke.dajiangtai.com/content/1901/6.png)

![img](http://ke.dajiangtai.com/content/1901/7.jpg)

● Storm仅限于流计算(topology)

● JStorm参照Flink改进了Storm

#### 3.5 Spark的竞争对手---Hadoop3.x

http://news.cnw.com.cn/news-international/htm2016/20160603_327510.shtml