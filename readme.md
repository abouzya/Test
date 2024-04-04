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


| Source                                                                    | Processor                                                                  | Sink                                                |
| ------------------------------------------------------------------------- |:--------------------------------------------------------------------------:| ---------------------------------------------------:|
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
|[[Websocket](functions/supplier/websocket-supplier/README.adoc)|     |[Websocket](functions/consumer/websocket-consumer/README.adoc)|
|    |    |[Wavefront](functions/consumer/wavefront-consumer/README.adoc)|
|[XMPP](functions/supplier/xmpp-supplier/README.adoc)|    |[XMPP](functions/consumer/xmpp-consumer/README.adoc)|












