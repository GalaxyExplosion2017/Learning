# Hadoop概述

[TOC]

### 一.产生背景及发展历程

#### 1.1 产生背景


​	●Hadoop最早起源于Nutch。

​	● Nutch的设计目标是构建一个大型的全网搜索引擎，包括网页抓取、索引、查询等功能，但随着抓取网页数量的增加，它遇到了严重的可扩展性问题，它不能解决数十亿网页的存储与索引问题。

​	● 谷歌发表了两篇论文：一篇是关于谷歌分布式文件系统（GFS）的论文；一篇是关于谷歌分布式计算框架MapReduce的论文。

​	

#### 1.2 Hadoop 发展历程


​	● 2004年Google发表MapReduce论文

​	● 2005年Nutch开发并平稳运行MapReduce

​	● 2006年1月DougCutting加入雅虎

​	● 2006年2月Apache Hadoop项目正式启动

​	● 2007年百度和中国移动开始使用Hadoop做离线处理

​	● 2008年淘宝开始投入研究基于Hadoop的系统

​	● 2008年1月Hadoop成为Apache顶级项目。

​	● 2009 年3月Cloudera推出CDH平台

​	● 2009年7月 Hadoop Core项目更名为Hadoop Common；MapReduce和HDFS成为Hadoop项目的独立子项目。

​	● 2010年5月 ，HBase脱离Hadoop项目，成为Apache顶级项目。

​	● 2010年9月，Hive( Facebook) 脱离Hadoop，成为Apache顶级项目。

​	● 2011年1月，ZooKeeper 脱离Hadoop，成为Apache顶级项目



#### 1.3 Hadoop 是什么


​	Hadoop是Apache软件基金会管理的开源软件平台，但Hadoop到底是什么呢？简单来	说，Hadoop是在分布式服务器集群上存储海量数据并运行分布式分析应用的一个开源的软件框架。

![img](http://hadoop2.dajiangtai.com/content/101/1.png)

#### 1.4 Hadoop能做什么


​	大数据时代已经到来，金融数据、电商数据、社交数据、游戏数据…….这些数据的规模、结构、增长的速度都给传统数据存储和处理技术带来巨大考验。Hadoop的简单方便、可扩展性和健壮性让其在大数据处理方面占尽优势，其主要适合的应用场景有：

​	● 搜索引擎，比如百度，Google

​	● 大数据存储，比如云存储

​	● 大数据处理，比如百度统计分析，腾讯分析

​	● 科学研究，比如Storm、Spark、Flink

#### 	1.5 为什么要使用Hadoop？

​	● 方便：Hadoop运行在由一般商用机器构成的大型集群上，或者云计算服务上，比如EC2。

​	● 健壮：Hadoop致力于在一般商用硬件上运行，其架构假设硬件会频繁失效，Hadoop可以从	容地处理大多数此类故障。

​	● 可扩展：Hadoop通过增加集群节点，可以线性地扩展以处理更大的数据集。

​	● 简单：Hadoop允许用户快速编写高效的并行代码。

​		![img](http://hadoop2.dajiangtai.com/content/101/1.png)	



### 二. Hadoop与云计算

####  2.1 Hadoop与云计算的关系

##### ● IAAS：基础设施即服务，典型实现有Amazon EC2、OpenStack、CloudStack、RackSpace等等

##### ● PAAS:平台即服务，典型的实现有Google APPEngine，Apache Hadoop

##### ● SAAS：软件即服务，它处于云计算的最上层，典型实现有：Google Apps

#### 2.2Hadoop与Spark的关系—指标对比


![img](http://hadoop2.dajiangtai.com/content/101/2.png) 			

#### 2.3 Hadoop与Spark的关系—相辅相成


![img](http://hadoop2.dajiangtai.com/content/101/3.png)	

#### 2.4 Hadoop与spark的关系—适用场景

##### ● 2.41 业务需求


​	1)公司网站每天 pv uv 统计

​	2)视屏网站电影、电视剧的评分排名、最新更新、昨日热播

​	3)电视台收视率排名

​	4)公司昨日数据统计报表

​	5)社交征婚网站昨日私信量、拆信量 等等

##### ● 2.42 成本考虑


​	1)内存

​	2)服务器

​	**面对大数据不同框架，我们该如何对待**

​	● 无需纠结谁替代谁(相互补充)

​	● 以某一个组件为突破口逐渐深入

​	● 一切以应用场景为出发点

#### 	2.5 Hadoop与传统关系数据库的关系	![img](http://hadoop2.dajiangtai.com/content/101/4.png)



### 三.Hadoop应用现状

#### 3.1 Hadoop国内外应用现状 

​	**Hadoop作为大数据存储及计算领域的一颗明星，目前已经得到越来越广泛的应用。不管是国外的著名公司Google、Yahoo!、微软、亚马逊、 EBay、FaceBook、Twitter、LinkedIn等和初创公司Cloudera、Hortonworks等，又还是国内的著名公司中国移动、阿里巴巴、华为、腾讯、百度、网易、京东商城等，都在使用Hadoop及相关技术解决大规模化数据问题，以满足公司需求和创造商业价值。**

以下是列举几个国内外知名企业在大数据领域应用情况：

● 百度：数据挖掘与分析、日志分析平台、数据仓库系统、推荐引擎系统、用户行为分析系统

![img](http://hadoop2.dajiangtai.com/content/101/5.png)

● 阿里巴巴：数据平台系统、量子统计、搜索支撑、淘数据、广告系统、推荐引擎系统、数据魔方、搜索排行榜

![img](http://hadoop2.dajiangtai.com/content/101/6.png)

● 腾讯：腾讯社交广告平台、搜搜、拍拍网、腾讯微博、QQ会员、腾讯游戏支撑、QQ空间、朋友网、腾讯开放平台、财付通、手机QQ、QQ音乐

![img](http://hadoop2.dajiangtai.com/content/101/7.png)

● Yahoo：支持广告系统、反垃圾邮件系统、用户行为分析、会员反滥用、支持Web搜索、个性化推荐

![img](http://hadoop2.dajiangtai.com/content/101/8.png)

● Facebook：Facebook使用Hadoop存储内部日志与多维数据，并以此作为报告、分析和机器学习的数据源。

![img](http://hadoop2.dajiangtai.com/content/101/9.png)

**我们通过下图了解更多企业大数据领域的应用情况，小讲想说的是，信息可能有变化，同学们有个大概的了解即可，无须深究。**

|                                          | [![img](http://hadoop2.dajiangtai.com/content/101/360.jpg) ]() | [![img](http://hadoop2.dajiangtai.com/content/101/a9.png) ]() |                                          | [![img](http://hadoop2.dajiangtai.com/content/101/adobe.jpg) ]() | [![img](http://hadoop2.dajiangtai.com/content/101/alibaba.png) ]() |                                          |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| [![img](http://hadoop2.dajiangtai.com/content/101/baidu.png) ]() | [![img](http://hadoop2.dajiangtai.com/content/101/chinamobile.png) ]() | [![img](http://hadoop2.dajiangtai.com/content/101/Datagraph.png) ]() |                                          | [![img](http://hadoop2.dajiangtai.com/content/101/ebay.jpg) ]() | [![img](http://hadoop2.dajiangtai.com/content/101/facebook.jpg) ]() | [![img](http://hadoop2.dajiangtai.com/content/101/HollandComputingCenter.gif) ]() |
| [![img](http://hadoop2.dajiangtai.com/content/101/huawei.jpg) ]() | [![img](http://hadoop2.dajiangtai.com/content/101/yahoo.png)]() |                                          |                                          |                                          | [![img](http://hadoop2.dajiangtai.com/content/101/worldlingo.png) ]() | [![img](http://hadoop2.dajiangtai.com/content/101/IBM.jpg) ]() |
|                                          | [![img](http://hadoop2.dajiangtai.com/content/101/LastFm.png) ]() | [![img](http://hadoop2.dajiangtai.com/content/101/visibleMeasures.jpg) ]() | [![img](http://hadoop2.dajiangtai.com/content/101/terrier-team.png) ]() | [![img](http://hadoop2.dajiangtai.com/content/101/tencent.jpg) ]() | [![img](http://hadoop2.dajiangtai.com/content/101/LinkedIn.jpg) ]() |                                          |
|                                          |                                          | [![img](http://hadoop2.dajiangtai.com/content/101/mobileAnalytic.png) ]() | [![img](http://hadoop2.dajiangtai.com/content/101/quantcast.jpg) ]() | [![img](http://hadoop2.dajiangtai.com/content/101/openstat.png) ]() |                                          |                                          |
|                                          |                                          |                                          | [![img](http://hadoop2.dajiangtai.com/content/101/pangusousuo.jpg)]() |                                          |                                          |                                          |

#### 3.2 Hadoop 发展趋势

![img](http://hadoop2.dajiangtai.com/content/101/10.png)



### 四. Hadoop生态

#### 4.1 Hadoop 生态系统简介

![img](http://hadoop2.dajiangtai.com/content/101/19.png)

#### 4.2 Hadoop 技术选型和架构设计

![img](http://hadoop2.dajiangtai.com/content/101/20.png)

![img](http://hadoop2.dajiangtai.com/content/101/21.png)