# The Introduction of Kafka Connect

### Kafka基本介绍

- kafka是一个分布式的流平台，可以发布和订阅信息流，类似于一个消息队列或企业消息系统、以容错的方式存储消息流、在消息流发生时处理它们。

![kafkaå¥é¨ä"ç"](https://img.orchome.com/group1/M00/00/01/KmCudlf7DXiAVXBMAAFScKNS-Og538.png)

### Kafka Connect 概述

kafka Connect 是一个可靠性高的、可扩展的在Kafka和其他系统之间流传输的数据工具。它可以通过Connector简单、快速的将大集合数据导入导出Kafka。Kafka Connect可以接收整个数据库或从所有应用程序收集消息到Kafka Topic。 这些数据可用于低延迟流处理。 导出可以将Topic的数据发送到Secondary Storage，查询系统或批处理系统以进行离线分析。 Kafka Connect功能包括：

- A common framework for Kafka connectors - Kafka Connect 规范了Kafka与其他数据系统集成，简化了Connector的开发、部署与管理
- Distributed and standalone modes - 向上扩展到支持整个组织的大型集中管理服务，或向下扩展到开发、测试和小型生成场景的部署
- REST interface - 使用REST API来提交并管理Kafka Connect集群
- Automatic offset management - 因为只有少量的信息来自Connector，Kafka Connect 可以自动化地管理offset commit 过程
- Distributed and scalable by default - Kafka Connect 建立在现有的组管理协议上，可以将更多的工作添加扩展到Kafka Connect集群中
- Streaming / batch integration -  利用现有的能力，Kafka Connect可以用来构建一个桥接流和批量数据系统



​	Kafka Connect提供的是以数据管道为中心的业务抽象。在Kafka Connect里有两个核心概念：Source和Sink。Source负责导入数据到Kafka，Sink负责从kafka中导出数据，他们分别称为Source Connector，Sink Connector，该方法提供了数据读取和写入的高度业务抽象，能够简化许多生命周期的管理。

### Kafka Connect 源码设计分析

Kafka connect源码部分分成6个模块，





### Kafka Connect JDBC Connector Demo



#### 创建SQLite数据库并读取数据

1. 在命令行中创建SQLite数据库

```sqlite3 test.db
sqlite3 test.db
```

​	然后登录得到类似信息：

```
SQLite version 3.23.1 2018-04-10 17:39:29
Enter ".help" for usage hints.
```

2. 在SQLite命令行中，创建一个table并输入一些数据：

```sqlite
sqlite> CREATE TABLE accounts(id INTEGER PRIMARY KEY AUTOINCREMENT NOT NULL, name VARCHAR(255));
sqlite> INSERT INTO accounts(name) VALUES('alice');
sqlite> INSERT INTO accounts(name) VALUES('bob');
```



#### 加载JDBC Source Connector



code

- consumer.bat 

.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic test --from-beginning

- producer

   .\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic test

- connect

.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic connect-test --from-beginning

- jdbc connect 启动

.\bin\windows\connect-standalone.bat .\etc\schema-registry\connect-avro-standalone.properties .\etc\kafka-connect-jdbc\sink-quickstart-sqlite.properties























![img](https://www.confluent.io/wp-content/uploads/Kafka_connect-1024x436.jpg)

​		

