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
|[JDBC](functions/supplier/jdbc-supplier/README.adoc) | [Image Recognition(Tensorflow)](functions/function/image-recognition-function/README.adoc)|   |
|[JMS](functions/supplier/jms-supplier/README.adoc) |   |   |





|link:functions/function/object-detection-function/README.adoc[Object Detection(Tensorflow)]
|link:functions/consumer/jdbc-consumer/README.adoc[JDBC]

|link:functions/supplier/mail-supplier/README.adoc[Mail]

|link:functions/function/semantic-segmentation-function/README.adoc[Semantic Segmentation(Tensorflow)]
|link:functions/consumer/log-consumer/README.adoc[Log]

|link:functions/supplier/mongodb-supplier/README.adoc[MongoDB]

|link:functions/function/spel-function/README.adoc[SpEL]
|link:functions/consumer/mongodb-consumer/README.adoc[MongoDB]

|link:functions/supplier/mqtt-supplier/README.adoc[MQTT]

|link:functions/function/splitter-function/README.adoc[Splitter]
|link:functions/consumer/mqtt-consumer/README.adoc[MQTT]

|link:functions/supplier/rabbit-supplier/README.adoc[RabbitMQ]
|link:functions/function/task-launch-request-function/README.adoc[Task Launch Request]
|link:functions/consumer/rabbit-consumer/README.adoc[RabbitMQ]
