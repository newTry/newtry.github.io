---
title: 大数据平台
date: 2016-11-26 15:06:03
tags: [大数据,hadoop,数据仓库]
categories: 
- 大数据
---

    这篇文章是5月份写的。
进入 [`有赞`](https://www.youzan.com) 已经2个多月了。目前待在大数据组，虽然还没有开始接触数据开发相应的工作，但在这样的部门中，对数据开发多少有些涉猎，且接下来会慢慢接触到真正的数据开发工作。最近在赶项目的同时，抽空恶补大数据的知识，略有所得，今天就来谈谈我对大数据的认识。

# 数据的产生

当系统到达一定的程度时，会有大量的数据产生，针对这些数据的存储，读取，分析，挖掘等都需要有一套机制。这个就是现在比较火的大数据。

# 系统数据的分类

在大型系统中，数据来源主要有两部分，一部分是系统的业务数据，另一部分是用户的行为数据。针对这两种不同的数据，有相应的两种存储形式，对于业务数据，一般来说是存放在数据库中，如关系型数据库mysql、oracle，非关系型数据库mongodb、redis等，而对于用户的行为数据则是以日志的形式进行存储。


## 业务数据

业务数据一般来说，是用户在使用系统时，需要并产生的一些数据。如创建一个店铺，在店铺中上架商品，商品卖出去会有订单，根据订单进行发货会产生物流信息等等，这些都是用户在使用过程中产生的业务数据。这部分数据会存放在数据库中。

## 用户行为数据

用户在访问网站时留下的行为轨迹数据。如从一个页面跳到另一个页面，访问页面过程中的点击行为，浏览行为等等。这部分数据以日志形式存在，保留和使用。

## 大数据平台组件

做的更多的事情是 olap 。

hadoop - hdfs、MapReduce

数据仓库 - hive

列式数据库 - hbase

日志搜集组件 - flume logstash

分布式消息系统 - kafka

流数据处理 - storm spark kylin

nosql数据库 - redis、mongodb

## 业务线
`搜索`
`风控`
`算法`
`报表`

线上数据中心

# 平台架构

- 数据来源 （数据源，mysql、日志、binlog）
- 数据统一接入（kafka）
- 数据etl与计算
- 数据存储 （hdfs）
- 数据计算（离线hive等，实时storm、kylin、spark等）
- 数据服务层 （对外提供服务）
- 数据应用（业务层）