# Real Time Large Scale Data Processing

In the SaaS platform, we usually need to process large scale data on the real time,  have the artificial intelligent engine to analyze the data on the fly and visualize the analysis result dynamically. 

Real Time data processing is a key part of the SaaS artificial intelligent platform.  While the distributed stream system and AI platform architectures are evolving, it is good to evaluate the different solutions with pros and cons and try to find the "fit" for particular business needs. 

In this project,  I am going to evaluate the real time data stream processing using different platforms. That includes Kafka, Spark, Data-bricks, Managed Service on Azure vs. Moses on DC/OS

## Getting Started

To get start, let's take a look at what Kafka, Spark and Databricks do. 

https://kafka.apache.org/

https://spark.apache.org/

### Kafka

Kafka Concepts:

- Kafka is run as a cluster on one or more servers that can span multiple datacenters.
- The Kafka cluster stores streams of *records* in categories called *topics*.
- Each record consists of a key, a value, and a timestamp.

Kafka Retention Policy:

- Configurable retention period.
- All records will be purged after the retention period no matter that has been consumed or not.
- Data volume won't impact performance so keeping longer retention period should not impact the Kafka performance but just need more space for keeping the data. 

Kafka Fault Tolerance:

- "Leader" and "Follower" architecture for each partition.  "Leader" handle all the read and write. If a "Leader" down, a new leader will be elected from the "Followers". 
- All partitions are replicated to multiple nodes with configurable number of replication nodes. 
- Each of the node server as one or multiple partitions "Leader" node so the load could be balanced.

Kafka Geo-Replication:

- Kafka MirrorMaker support active/active and active/passive replication.  Active / passive is for backup and replication. Active / active - for putting to a location closer to some users.

Kafka Topics:

- Partition-able
- Multiple subscribers
- Consumer has off-set meta data in the log

Kafka Core APIs:

- The [Producer API](https://kafka.apache.org/documentation.html#producerapi) allows an application to publish a stream of records to one or more Kafka topics.
- The [Consumer API](https://kafka.apache.org/documentation.html#consumerapi) allows an application to subscribe to one or more topics and process the stream of records produced to them.
- The [Streams API](https://kafka.apache.org/documentation/streams) allows an application to act as a *stream processor*, consuming an input stream from one or more topics and producing an output stream to one or more output topics, effectively transforming the input streams to output streams.
- The [Connector API](https://kafka.apache.org/documentation.html#connect) allows building and running reusable producers or consumers that connect Kafka topics to existing applications or data systems. For example, a connector to a relational database might capture every change to a table.

![img](assets/kafka-apis.png)

[Source: https://kafka.apache.org/intro]

### Spark

Spark concepts:

- 



## Part I - Kafka Spark on Azure Managed Service



## Part II - Data-bricks on Azure Managed Service



## Part III - Kafka Spark on  DC/OS





## References

[1] https://lenadroid.github.io/posts/kafka-hdinsight-and-spark-databricks.html

[2] https://github.com/lenadroid/kafka-spark-azure

[3] https://www.youtube.com/watch?v=tDAoIzF-7q0

