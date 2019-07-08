# Kafka Connect 源码分析

### API

Fold:D:\GSoC\kafka\connect\api\src\main\java\org\apache\kafka\connect

this fold has some functions that components, connector, data, errors, header, health, rest, sink, source, storage, transforms, util.



- components:

  - Versioned.java

    *interface*  Versioned: get the version of this component.

- connector:

  - Connector.java

    抽象类connector 继承 versioned。

    initialize: 初始化这个connector, 用所提供的ConnectorContext去通知runtime的输入配置的改变。

    start:  开启这个连接器，这个方法只能在干净的连接器上条用，即要么以及实例化并初始化，要不然已经被调用了。

    reconfigure: 更改配置

    validate：根据配置定义验证连接器的配置值

  - ConnectorContext.java

    *interface*: ConnectorContext,

  - ConnectRecord.java

    topic, kafkapartition, key, valueSchema, value, timestamp, headers

    int {hashCode},equals,tostring.

  - Task.java

    version：获取task的版本信息

    start，stop

- data:

  - CoonectSchema.java: 继承自Schema

    Maps Schema.Types :SCHEMA_TYPE_CLASSES, LOGICAL_TYPE_CLASSES, JAVA_CLASS_SCHEMA_TYPES

errors:

header:

health:

rest:

sink:

source:

storage:

transforms:

util







- runtime: 

  - Cli

    - ConnectDistributed.java
