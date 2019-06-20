# SoC
This repository is to restore the code of my Alibaba Summer of Code project about RocketMQ Openmessaging Connector. This repository will be finished on August 24.



# Implementation plan

（List your implementation steps to solve the problem）

1. Develop the Apache Connect JDBC Connector including Source Connector and Sink Connector. (essential)

2. Do the Unit test for the JDBC Connector (essential)

3. Write Dialect to support more JDBC connection driver for various databases

 

# Deliverables

（List the results you expect to deliver  in your Alibaba Summer of Code）

Milestones: 

1. Write a message connect connector to connect JDBC-Compatible databases and other databases

2.  Standardize the code style and complementary code structure 

3. Modify some of the runtime‘s code and write new function

4. Configure information to synchronize between the cluster of source

5. Add message connect support for ACL message authentication 

Documentation: Write the documentation about RocketMQ Connector and how to connect to JDBC and Other data source

Tests: Unit test openmessaging runtime code and the Functions about RmqTask and RmqConnector 



# Timeline

| Date               | Work                                                         |
| :----------------- | ------------------------------------------------------------ |
| June 10- June 20   | Get familiar with the RocketMQ, Openmessaging and message   connect refer to relevant information about connector, databases.   Keep diving into Rocket’s code by fixing issues. |
| June 21 – June 30  | Time for community Bonding, dive into the   architecture of RocketMQ, set up a development environment for coding and   debugging.   Discuss with   mentors about the implementation of the project.    Refer to   related work to get some ideas. |
| July 1 – July 14   | Write these functions of RocketMQ Connect   JDBC Source Connector:   Incremental Query Modes, Mapping Column   Types |
| July 15 – July 28  | Develop other functions of Connect JDBC   Source Connector:   JDBC Drivers, Message Keys, etc. |
| July 29 - August 4 | Develop these functions of RocketMQ JDBC   Sink Connector:   Data mapping, Key handling, etc. |
| August 5 - 11      | Develop other functions of RocketMQ JDBC   Sink Connector:   Idempotent writes, Auto-creation and   Auto-evolution, etc. |
| August 12 – 18     | Write the JDBC driver connection and   dialect with various databases   Do the Unit test for the JDBC Connector ’s   Component. |
| August 19 – 26     | Do the Unit test for the connector   Write the document for project. |