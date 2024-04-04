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


| Source        | Processor     | Sink  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |
