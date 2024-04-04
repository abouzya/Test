# Stream Applications

In this repository, you will find a collection of components that can meet various data integration use cases and requirements.

The repository's primary focus is to provide a set of standalone Java functions that can be useful in the end-user applications as-is.

Besides, this repository builds on the Java functions to generate standalone Spring Cloud Stream applications that can run against Spring Cloud Stream's RabbitMQ or Apache Kafka binder implementations.
It is also possible to extend the generator to bundle the Java functions with the other supported binder implementations.

These applications can run standalone or as part of a data flow, such as the one orchestrated using Spring Cloud Data Flow.

## Project Structure

The repository includes two major sections - `Functions` and `Applications`.
The former hosts the various Java functions, and the latter is for generating the standalone Spring Cloud Stream applications and hosting their related components.

The following are the various components of this repository.

- [Standalone Java Functions](https://github.com/spring-cloud/stream-applications/tree/master/functions)
- [Common Core Components for Applications](https://github.com/spring-cloud/stream-applications/tree/master/applications/stream-applications-core)
- [Spring Cloud Stream Applications](https://github.com/spring-cloud/stream-applications/tree/master/applications)
- [Build Parent](https://github.com/spring-cloud/stream-applications/tree/master/stream-applications-build)
- [Release Train](https://github.com/spring-cloud/stream-applications/tree/master/stream-applications-release-train)

## Reusable Functions


| `java.util.Supplier`                                                 | `java.util.Function`                                         | `java.util.Consumer`                                      |
| -------------------------------------------------------------------- |:------------------------------------------------------------:| ---------------------------------------------------:|
| [Debezium supplier](functions/supplier/debezium-supplier/README.adoc)| [Debezium supplier](functions/supplier/debezium-supplier/README.adoc) | [Analytics](functions/consumer/analytics-consumer/README.adoc)| 
| [File](functions/supplier/file-supplier/README.adoc)| [Filter](functions/function/filter-function/README.adoc) | [Cassandra](functions/consumer/cassandra-consumer/README.adoc)|
| [FTP](functions/supplier/ftp-supplier/README.adoc) | [Header-Enricher](functions/function/header-enricher-function/README.adoc) | [Elasticsearch](functions/consumer/elasticsearch-consumer/README.adoc)|
|    |[Header-Filter](functions/function/header-filter-function/README.adoc)|[File](functions/consumer/file-consumer/README.adoc)|
|[HTTP](functions/supplier/http-supplier/README.adoc) | [HTTP Request](functions/function/http-request-function/README.adoc) | [FTP](functions/consumer/ftp-consumer/README.adoc)|
|[Grnry-JDBC](functions/supplier/grnry-jdbc-supplier/README.adoc)|    |    |
|[JDBC](functions/supplier/jdbc-supplier/README.adoc) | [Image Recognition(Tensorflow)](functions/function/image-recognition-function/README.adoc)|   |
|[JMS](functions/supplier/jms-supplier/README.adoc) |   |   |
|     | [Object Detection(Tensorflow)](functions/function/object-detection-function/README.adoc)|[JDBC](functions/consumer/jdbc-consumer/README.adoc)
|[Mail](functions/supplier/mail-supplier/README.adoc)|   |    |
|    |[Semantic Segmentation(Tensorflow)](functions/function/semantic-segmentation-function/README.adoc)|[Log](functions/consumer/log-consumer/README.adoc)
|[MongoDB](functions/supplier/mongodb-supplier/README.adoc)|   |    |
|  |[SpEL](functions/function/spel-function/README.adoc)| [MongoDB](functions/consumer/mongodb-consumer/README.adoc)|
|[MQTT](functions/supplier/mqtt-supplier/README.adoc)|   |   |
|    |[Splitter](functions/function/splitter-function/README.adoc)|[MQTT](functions/consumer/mqtt-consumer/README.adoc)|
|[RabbitMQ](functions/supplier/rabbit-supplier/README.adoc)|[Task Launch Request](functions/function/task-launch-request-function/README.adoc)|[RabbitMQ](functions/consumer/rabbit-consumer/README.adoc)
|[AWS S3](functions/supplier/s3-supplier/README.adoc)|   |    |
|    |    |[Redis](functions/consumer/redis-consumer/README.adoc)|
|[SFTP](functions/supplier/sftp-supplier/README.adoc)|  |   |
|    |    |[RSocket](functions/consumer/rsocket-consumer/README.adoc)|
|[Syslog](functions/supplier/syslog-supplier/README.adoc)|    |    |
|    |    |[AWS S3](functions/consumer/s3-consumer/README.adoc)|
|[TCP](functions/supplier/tcp-supplier/README.adoc)|    |    |
|    |    |[SFTP](functions/consumer/sftp-consumer/README.adoc)|
|[Time](functions/supplier/time-supplier/README.adoc)|    |    |
|    |    |[TCP](functions/consumer/tcp-consumer/README.adoc)|
|[Twitter](functions/supplier/twitter-supplier/README.adoc)|[Twitter](functions/function/twitter-function/README.adoc)|[Twitter](functions/consumer/twitter-consumer/README.adoc)|
|[Websocket](functions/supplier/websocket-supplier/README.adoc)|     |[Websocket](functions/consumer/websocket-consumer/README.adoc)|
|    |    |[Wavefront](functions/consumer/wavefront-consumer/README.adoc)|
|[XMPP](functions/supplier/xmpp-supplier/README.adoc)|    |[XMPP](functions/consumer/xmpp-consumer/README.adoc)|


## Reusable Spring Cloud Stream Applications

| Source                                                                    | Processor                                                                  | Sink                         |                      
| ------------------------------------------------------------------------- |:--------------------------------------------------------------------------:| ----------------------------:|
|[Debezium supplier](applications/source/debezium-source/README.adoc)   |[Aggregator](applications/processor/aggregator-processor/README.adoc)|[Analytics](applications/sink/analytics-sink/README.adoc)|
|[File](applications/source/file-source/README.adoc)|[Bridge](applications/processor/bridge-processor/README.adoc)|[Cassandra](applications/sink/cassandra-sink/README.adoc)|
|[FTP](applications/source/ftp-source/README.adoc)|[Filter](applications/processor/filter-processor/README.adoc)|[Elasticsearch](applications/sink/elasticsearch-sink/README.adoc)|
|    |[Groovy](applications/processor/groovy-processor/README.adoc)|[File](applications/sink/file-sink/README.adoc)|
|[HTTP](applications/source/http-source/README.adoc)|[Header-Enricher](applications/processor/header-enricher-processor/README.adoc)|[FTP](applications/sink/ftp-sink/README.adoc)|
|[JDBC](applications/source/jdbc-source/README.adoc)|[HTTP Request](applications/processor/http-request-processor/README.adoc)|    |
|[JMS](applications/source/jms-source/README.adoc)|[Image Recognition(Tensorflow)](applications/processor/image-recognition-processor/README.adoc)|[JDBC](applications/sink/jdbc-sink/README.adoc)|
|[Load-Generator](applications/source/load-generator-source/README.adoc)|[Object Detection(Tensorflow)](applications/processor/object-detection-processor/README.adoc)|[Log](applications/sink/log-sink/README.adoc)|
|[Mail](applications/source/mail-source/README.adoc)|      |[MongoDB](applications/sink/mongodb-sink/README.adoc)|
|[MongoDB](applications/source/mongodb-source/README.adoc)|[Semantic Segmentation(Tensorflow)](applications/processor/semantic-segmentation-processor/README.adoc)|[MQTT](applications/sink/mqtt-sink/README.adoc)|
|[MQTT](applications/source/mqtt-source/README.adoc)|[Script](applications/processor/script-processor/README.adoc)|[Pgcopy](applications/sink/pgcopy-sink/README.adoc)|
|[RabbitMQ](applications/source/rabbit-source/README.adoc)|[Splitter](applications/processor/splitter-processor/README.adoc)|[RabbitMQ](applications/sink/rabbit-sink/README.adoc)|

|






|link:applications/source/s3-source/README.adoc[AWS S3]
|link:applications/processor/transform-processor/README.adoc[Transform]
|link:applications/sink/redis-sink/README.adoc[Redis]
|link:applications/source/sftp-source/README.adoc[SFTP]
|link:applications/processor/twitter-trend-processor/README.adoc[Twitter Trend]
|link:applications/sink/router-sink/README.adoc[Router]
|link:applications/source/syslog-source/README.adoc[Syslog]
|
|link:applications/sink/rsocket-sink/README.adoc[RSocket]
|link:applications/source/tcp-source/README.adoc[TCP]
|
|link:applications/sink/sftp-sink/README.adoc[SFTP]
|link:applications/source/time-source/README.adoc[Time]
|
|link:applications/sink/tasklauncher-sink/README.adoc[Task Launcher]
|link:applications/source/twitter-message-source/README.adoc[Twitter Message]
|
|link:applications/sink/tcp-sink/README.adoc[TCP]
|link:applications/source/twitter-search-source/README.adoc[Twitter Search]
|
|link:applications/sink/throughput-sink/README.adoc[Throughput]
|link:applications/source/twitter-stream-source/README.adoc[Twitter Stream]
|
|link:applications/sink/twitter-message-sink/README.adoc[Twitter Message]
|link:applications/source/websocket-source/README.adoc[Websocket]
|
|link:applications/sink/twitter-update-sink/README.adoc[Twitter Update]
|link:applications/source/xmpp-source/README.adoc[XMPP]
|
|link:applications/sink/wavefront-sink/README.adoc[Wavefront]
|
|
|link:applications/sink/websocket-sink/README.adoc[Websocket]
|
|
|link:applications/sink/xmpp-sink/README.adoc[XMPP]
|===











