# Changelog

## Unreleased

## Version 1.25.1 (2023-04-27)

- Fix apache pulsar instrumentation missing from the Java agent
  ([#8378](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8378))

## Version 1.25.0 (2023-04-13)

### Migration notes

- Apache Pulsar instrumentation name is changed from `io.opentelemetry.apache-pulsar-2.8` to
  `io.opentelemetry.pulsar-2.8` and Apache Camel instrumentation name is changed from
  `io.opentelemetry.apache-camel-2.20` to `io.opentelemetry.camel-2.20`
  ([#8195](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8195))
- Mojarra instrumentation suppression key has changed from `mojarra` to `jsf-mojarra`
  and MyFaces instrumentation suppression key has changed from `myfaces` to `jsf-myfaces`
  ([#7811](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7811))

### 🌟 New javaagent instrumentation

- R2DBC
  ([#7977](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7977))
- Add JFR streaming metrics gatherer
  ([#7886](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7886))
- ZIO 2.0 instrumentation
  ([#7980](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7980))

### 🌟 New library instrumentation

- R2DBC
  ([#7977](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7977))
- Add JFR streaming metrics gatherer
  ([#7886](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7886))
- Add library instrumentation for java http client
  ([#8138](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8138))

### 📈 Enhancements

- Move X-Ray Env Variable propagation to span link instead of parent
  ([#7970](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7970))
- Reduce memory usage for ClassLoaderHasClassesNamedMatcher
  ([#7866](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7866))
- Remove password from db.user parsed from JDBC url
  ([#8106](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8106))
- Ignore appd agent classes
  ([#8065](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8065))
- Add http client metrics to apache http library instrumentation
  ([#8128](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8128))
- Instrument additional pulsar receive methods
  ([#8171](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8171))
- Support latest Hibernate 6 version
  ([#8189](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8189))
- Support spring boot service name detector when spring boot application is packaged in one jar
  ([#8101](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8101))
- Support parsing Spring boot service name when more than one yaml is defined
  ([#8006](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8006))
- Add option to capture logback key value pairs
  ([#8074](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8074))
- Bridge agent logs into application's slf4j logger
  ([#7339](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7339),
  [#8228](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8228))
- Better container ID parsing
  ([#8206](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8206))
- Pulsar batch receive instrumentation
  ([#8173](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8173))
- Improve compatibility with SecurityManager
  ([#7983](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7983))
- Instrument akka-http bindAndHandle
  ([#8174](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8174))
- Spring scheduling: run error handler with the same context as task
  ([#8220](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8220))
- Switch from http.flavor to net.protocol.*
  ([#8131](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8131),
  [#8244](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8244))
- Support latest Armeria release
  ([#8247](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8247))
- Populate `process.command_args` for Java 9+ and improve `process.command_line` for Java 8
  ([#8130](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8130))

### 🛠️ Bug fixes

- Fix TracingCqlSession ClassCastException
  ([#8041](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8041))
- Kafka: avoid registering duplicate metrics reporter
  ([#8099](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8099))
- Prefix baggage key not value when adding it to logback mdc
  ([#8066](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8066))
- Fix error when using shardingsphere
  ([#8110](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8110))
- Fix order of cxf handlers to enable symmetric tracing around jaxws handler chain
  ([#8160](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8160))
- Fix javaagent armeria server instrumentation
  ([#8281](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8281))

### 🧰 Tooling

- Add HttpServerResponseCustomizer support for various servers
  ([#8094](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8094),
  [#8095](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8095),
  [#8265](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8265),
  [#8264](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8264),
  [#8273](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8273),
  [#8263](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8263),
  [#8274](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8274),
  [#8272](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8272))
- Add `removeJarVersionNumbers` build setting
  ([#8116](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8116))
- Add `disableShadowRelocate` build setting
  ([#8117](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8117))

## Version 1.24.0 (2023-03-15)

### Migration notes

### 🌟 New javaagent instrumentation

- Add Apache Pulsar client instrumentation
  ([#5926](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5926),
  [#7999](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7999),
  [#7943](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7943),
  [#8007](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8007))
- Add Jodd-Http instrumentation
  ([#7868](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7868))

### 🌟 New library instrumentation

- Add Ktor client instrumentation
  ([#7982](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7982),
  [#7997](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7997))
- Add Spring Webflux server instrumentation
  ([#7899](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7899))

### 📈 Enhancements

- Implement `messaging.kafka.*` attributes spec
  ([#7824](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7824),
  [#7860](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7860))
- Make RxJava2 instrumentation Android-friendly
  ([#7895](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7895))
- Support more semantic convention for RocketMQ trace
  ([#7871](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7871))
- Instrumenting cassandra executeReactive method
  ([#6441](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6441))
- Make the OpenTelemetry Logback appender work with GraalVM native images
  ([#7989](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7989))
- Add baggage to Logback MDC; controlled by a configuration flag
  ([#7892](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7892))
- Make the Spring Boot autoconfigure module work with Spring Boot 3
  ([#8028](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8028),
  [#8051](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8051))

### 🛠️ Bug fixes

- Handle JMX MBean attributes with embedded dots
  ([#7841](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7841))
- Fix `ClassCastException` when using `-Dotel.jmx.target.system=tomcat`
  ([#7884](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7884))
- Fix NPE in the AWS SDK 2 instrumentation when request instrumentation is suppressed
  ([#7953](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7953))
- Fix Kotlin coroutine context propagation
  ([#7879](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7879))
- Fix the JAX-RS annotation instrumentation on Open Liberty
  ([#7890](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7890))
- Fix an `AbstractMethodError` in the Logback instrumentation
  ([#7967](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7967))
- Fix NPE in the RabbitMQ instrumentation
  ([#8021](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8021))
- Fix JMX metrics usage examples
  ([#7877](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7877))

### 🧰 Tooling

- Remove deprecated `instrumentation-api-semconv` code
  ([#7838](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7838))
- Look up helper class bytes when they are needed
  ([#7839](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7839))
- Run smoke tests using Open Liberty 21.0.0.12 and 22.0.0.12
  ([#7878](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7878),
  [#7857](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7857))
- Add additional groovy script classloaders to ignore list.
  ([#7460](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7460))
- Make AggregationTemporality configurable for `OtlpInMemoryMetricExporter` in
  the `agent-for-testing` module
  ([#7904](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7904))
- Upgrade to gradle 8.0.2
  ([#7910](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7910),
  [ 7978](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7978))
- Replace the test-sets plugin with Gradle test suites
  ([#7930](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7930),
  [#7933](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7933),
  [#7932](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7932),
  [#7931](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7931),
  [#7929](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7929),
  [#7946](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7946),
  [#7945](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7945),
  [#7944](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7944),
  [#7943](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7943),
  [#7942](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7942),
  [#7928](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7928),
  [#7951](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7951))
- Add a utility for tracking HTTP resends
  ([#7986](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7986))
- Remove deprecated `messaging.url` attribute from messaging getter
  ([#8008](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8008))
- Add protocol name&version to net attribute getters
  ([#7994](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7994))
- Test http client captured headers
  ([#7993](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7993))
- Improve compatibility with other agents
  ([#7916](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7916))
- Share timer class used by messaging instrumentations
  ([#8009](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8009))
- Convert groovy tests to java
  ([#7976](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7976),
  [#7975](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7975),
  [#7912](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7912))
- Check that extracting extension jar doesn't escape designated directory
  ([#7908](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7908))
- Assert user agent when it is present in HTTP client tests
  ([#7918](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7918))
- Update the OpenTelemetry SDK version to 1.24.0
  ([#8027](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/8027))
- Provide ability to add HTTP server response headers, with Tomcat implementation
  ([#7990](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7990))

## Version 1.23.0 (2023-02-16)

### Migration notes

- HTTP span names are now `"{http.method} {http.route}"` instead of just `"{http.route}"`,
  reflecting the recent change in the HTTP semantic conventions
  ([#7730](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7730))
- Added the base version into library package names to make room for other base versions
  without breaking backwards compatibility in the future once these artifacts are declared stable
  ([#7608](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7608),
  [#7752](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7752),
  [#7764](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7764))
  - `io.opentelemetry.instrumentation.spring.web.SpringWebTelemetry`
    → `io.opentelemetry.instrumentation.spring.web.v3_1.SpringWebTelemetry`
  - `io.opentelemetry.instrumentation.spring.webflux.SpringWebfluxTelemetry`
    → `io.opentelemetry.instrumentation.spring.webflux.v5_0.SpringWebfluxTelemetry`
  - `io.opentelemetry.instrumentation.spring.integration.SpringIntegrationTelemetry`
    → `io.opentelemetry.instrumentation.spring.integration.v4_1.SpringIntegrationTelemetry`
  - `io.opentelemetry.instrumentation.logback.v1_0.OpenTelemetryAppender`
    → `io.opentelemetry.instrumentation.logback.mdc.v1_0.OpenTelemetryAppender`
  - `io.opentelemetry.instrumentation.apachedbcp.ApacheDbcpTelemetry`
    → `io.opentelemetry.instrumentation.apachedbcp.v2_0.ApacheDbcpTelemetry`
  - `io.opentelemetry.instrumentation.c3p0.C3p0Telemetry`
    → `io.opentelemetry.instrumentation.c3p0.v0_9.C3p0Telemetry`
  - `io.opentelemetry.instrumentation.graphql.GraphQLTelemetry`
    → `io.opentelemetry.instrumentation.graphql.v12_0.GraphQLTelemetry`
  - `io.opentelemetry.instrumentation.guava.GuavaAsyncOperationEndStrategy`
    → `io.opentelemetry.instrumentation.guava.v10_0.GuavaAsyncOperationEndStrategy`
  - `io.opentelemetry.instrumentation.hikaricp.HikariTelemetry`
    → `io.opentelemetry.instrumentation.hikaricp.v3_0.HikariTelemetry`
  - `io.opentelemetry.instrumentation.kafkaclients.KafkaTelemetry`
    → `io.opentelemetry.instrumentation.kafkaclients.v2_6.KafkaTelemetry`
  - `io.opentelemetry.instrumentation.oracleucp.OracleUcpTelemetry`
    → `io.opentelemetry.instrumentation.oracleucp.v11_2.OracleUcpTelemetry`
  - `io.opentelemetry.instrumentation.ratpack.RatpackTelemetry`
    → `io.opentelemetry.instrumentation.ratpack.v1_7.RatpackTelemetry`
  - `io.opentelemetry.instrumentation.reactor.ContextPropagationOperator`
    →` io.opentelemetry.instrumentation.reactor.v3_1.ContextPropagationOperator`
  - `io.opentelemetry.instrumentation.viburdbcp.ViburTelemetry`
    → `io.opentelemetry.instrumentation.viburdbcp.v11_0.ViburTelemetry`
- Several instrumentation scope names have been fixed
  ([#7632](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7632))
  - `io.opentelemetry.cxf-jaxrs-3.2` → `io.opentelemetry.jaxrs-2.0-cxf-3.2`
  - `io.opentelemetry.jersey-2.0` → `io.opentelemetry.jaxrs-2.0-jersey-2.0`
    or `io.opentelemetry.jaxrs-3.0-jersey-3.0` as appropriate
  - `io.opentelemetry.resteasy-3.0` → `io.opentelemetry.jaxrs-2.0-resteasy-3.0`
  - `io.opentelemetry.resteasy-3.1` → `io.opentelemetry.jaxrs-2.0-resteasy-3.1`
  - `io.opentelemetry.resteasy-6.0` → `io.opentelemetry.jaxrs-3.0-resteasy-6.0`
  - `io.opentelemetry.jws-1.1` → `io.opentelemetry.jaxws-jws-api-1.1`
  - `io.opentelemetry.vertx-kafka-client-3.5` → `io.opentelemetry.vertx-kafka-client-3.6`
  - `io.opentelemetry.hibernate-4.3` → `io.opentelemetry.hibernate-procedure-call-4.3`
- All methods in all `*Getter` classes in `instrumentation-api-semconv` have been renamed
  to use the `get*()` naming scheme
  ([#7619](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7619))
- Return interfaces instead of concrete implementations in `instrumentation-api-semconv`
  ([#7658](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7658))

### 📈 Enhancements

- Support Spring Web 6 in library instrumentation
  ([#7551](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7551))
- Add gRPC request metadata instrumentation
  ([#7011](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7011))
- Pass context to content length http metrics meters
  ([#7506](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7506))
- Update SQL span name for procedures
  ([#7557](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7557))
- Ratpack services OpenTelemetry
  ([#7477](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7477))
- Ignore janino classloader
  ([#7710](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7710))
- Improve type resolution cache for classes in java package
  ([#7714](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7714))
- End netty client span before callbacks
  ([#7737](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7737))
- Support slf4j to log4j2
  ([#7656](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7656))
- Add `net.host.port` to the `http.server.active_requests` metric
  ([#7757](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7757))
- Allow JDBC library instrumentation to use a custom OpenTelemetry instance to be more DI
  (e.g. Spring Boot) friendly
  ([#7697](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7697))
- Dubbo: don't create spans for calls inside the same jvm
  ([#7761](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7761))
- Bridge OpenTelemetry metrics batch API
  ([#7762](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7762))
- Support Spring Boot 3 in autoconfigure module
  ([#7784](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7784))
- Change Spring Scheduling to not capture span for one-time jobs (only repeated jobs)
  ([#7760](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7760))
- Add instrumentation for hibernate 6
  ([#7773](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7773))
- Put `http.route` attribute onto `http.server.duration` on Play framework request processing
  ([#7801](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7801))
- Add Jakarta JSF 3.0+ instrumentation
  ([#7786](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7786))
- Capture `net.sock.peer.addr` more reliably in grpc client instrumentation
  ([#7742](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7742))

### 🛠️ Bug fixes

- Fix potential startup failure
  ([#7567](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7567))
- Fix NoClassDefFoundError happening when snakeyaml is used on a custom JRE
  ([#7598](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7598))
- Fix inconsistent handling of `net.peer.port` in HTTP instrumentations
  ([#7618](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7618))
- Fix concurrency issue in OpenTelemetryDriver
  ([#7628](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7628))
- Fix ClassCastException with redisson batch with atomic write option
  ([#7743](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7743))
- Ensure kafka configuration remains serializable
  ([#7754](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7754),
  [#7789](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7789))

## Version 1.22.1 (2023-01-14)

- Fix potential startup failure
  ([#7567](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7567))

## Version 1.22.0 (2023-01-12)

### 📈 Enhancements

- Add resource injection for getResourceAsStream
  ([#7476](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7476))
- GRPC: Adds peer socket address when the client call is ready
  ([#7451](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7451))
- Make OpenTelemetryAppender.Builder public
  ([#7521](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7521))
- Disable internal TaskScheduler spans in Spring Kafka instrumentation
  ([#7553](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7553))
- Support Spring Web MVC in library instrumentation
  ([#7552](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7552))
- Instrument JMS 3.0 (Jakarta)
  ([#7418](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7418))
- Shade `application.io.opentelemetry` in agent extension class loader
  ([#7519](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7519))
- Use new reactor contextWrite when available (from reactor 3.4.0)
  ([#7538](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7538))
- Make config file available in early agent initialization phase
  ([#7550](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7550))
- Support Spring JMS 6.0
  ([#7438](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7438))

### 🛠️ Bug fixes

- Preserve original exception in jetty http client wrappers
  ([#7455](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7455))
- Propagate original exception through kafka wrapper
  ([#7452](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7452))
- Fix class file load error when using spring-guice together with spring-web instrumentation
  ([#7447](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7447))
- Fix NPE in servlet AsyncListener on OpenLiberty
  ([#7498](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7498))

### 🧰 Tooling

- Muzzle logs should be logged using the io.opentelemetry.* logger name
  ([#7446](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7446))

## Version 1.21.0 (2022-12-13)

### 📈 Enhancements

- Remove deprecated HTTP semconv code
  ([#7259](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7259))
- Rocketmq 5: set context for async callback
  ([#7238](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7238))
- HTTP semconv: filter out default peer/host ports
  ([#7258](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7258))
- Allow multiple YAML configuration files for JMX rules
  ([#7284](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7284))
- OpenTelemetryDriver better support for native images
  ([#7089](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7089))
- Support Spring Kafka 3
  ([#7271](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7271))
- Add instrumentation for opentelemetry-extension-kotlin
  ([#7341](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7341))
- Populate `messaging.kafka.message.offset` in all kafka instrumentations
  ([#7374](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7374))
- More flexible cgroupv2 container id parsing (and podman support)
  ([#7361](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7361))
- Instrument spring-web 6 & spring-webmvc 6
  ([#7366](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7366))
- Change log4j MapMessage attribute names
  ([#7397](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7397))
- Don't call Thread#setContextClassLoader()
  ([#7391](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7391))

### 🛠️ Bug fixes

- Webflux instrumentation doesn't capture `http.status_code` in some cases
  ([#7251](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7251))
- Clean WeakConcurrentMap from background thread
  ([#6240](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6240))
- Update gwt rpc span from INTERNAL to SERVER
  ([#7342](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7342))
- JMXMetricInsight should log nothing at INFO level
  ([#7367](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7367))
- Fix NullPointerException when uri is null
  ([#7387](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7387))
- Agent context storage wrapper should not override other wrappers
  ([#7355](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7355))
- Do not install GC metrics when GarbageCollectionNotificationInfo is not available
  ([#7405](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7405))
- Fix connection pool timeouts unit
  ([#7404](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7404))

### 🧰 Tooling

- Allow disabling muzzle checks for specific methods
  ([#7289](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7289))

## Version 1.20.2 (2022-11-22)

### 🛠️ Bug fixes

- Fix the boms
  ([#7252](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7252))

## Version 1.20.1 (2022-11-19)

### 📈 Enhancements

- Update SDK version from 1.19.0 to 1.20.1
  ([#7223](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7223))

## Version 1.20.0 (2022-11-17)

Instrumentation annotations module is declared stable in this release
(`io.opentelemetry.instrumentation:opentelemetry-instrumentation-annotations:1.20.0`).

### Migration notes

- Renamed configuration property `otel.instrumentation.kafka.client-propagation.enabled` to
  `otel.instrumentation.kafka.producer-propagation.enabled` and update code so that it only affects
  producer propagation
  ([#6957](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6957))
- Deprecated RocketMQ configuration property `otel.instrumentation.rocketmq-client.propagation`
  ([#6958](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6958))
- Deprecated `HttpServerAttributesExtractor#create(HttpServerAttributesGetter)` and
  `HttpServerAttributesExtractor#builder(HttpServerAttributesGetter)`
  ([#7020](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7020))
- Renamed annotation instrumentation property name for the recent
  `opentelemetry-instrumentation-annotations` package from
  `otel.instrumentation.opentelemetry-annotations.exclude-methods` to
  `otel.instrumentation.opentelemetry-instrumentation-annotations.exclude-methods`
  ([#7196](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7196))

### 🌟 New javaagent instrumentation

- OpenSearch 1.x and 2.x
  ([#6998](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6998))
- JMX Metric Insight
  ([#6573](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6573))

### 📈 Enhancements

- Add meter version to runtime metrics
  ([#6874](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6874))
- Auto-detect service name based on the jar name
  ([#6817](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6817))
- okhttp: run our interceptor before other interceptors
  ([#6997](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6997))
- Implement producer part of RocketMQ new client instrumentation
  ([#6884](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6884))
- Ignore presto-jdbc shaded okhttp3 connection pool.
  ([#7031](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7031))
- Record memory usage after garbage collection
  ([#6963](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6963))
- Ignore trino shaded okhttp pool
  ([#7114](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7114))
- Ignore Nashorn's class loader for performance reasons
  ([#7116](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7116))
- Add gRPC library configuration for additionalServerExtractors
  ([#7155](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7155))
- Implement consumer part of rocketmq new client instrumentation
  ([#7019](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7019))
- Support cgroup v2
  ([#7167](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7167))
- Replace `runtime.jvm.gc.time` / `runtime.jvm.gc.count` metrics with
  `process.runtime.jvm.gc.duration` histogram
  ([#6964](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6964))

### 🛠️ Bug fixes

- End reactor-netty HTTP client span properly on `Mono#timeout()`
  ([#6891](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6891))
- Capture net.host.name for netty
  ([#6892](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6892))
- 6929 - fixing unit for runtime.jvm.gc.count
  ([#6930](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6930))
- fix spring-webflux cast to PathPattern throws ClassCastException
  ([#6872](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6872))
- Fix metric units
  ([#6931](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6931))
- Fix RocketMQ ClassCastException on hook conflict
  ([#6940](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6940))
- Handle UnsupportedClassVersionError in ServiceLoader on jdk9
  ([#7090](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7090))
- Avoid NPE when DirectWithAttributesChannel class is not available
  ([#7133](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7133))

### 🧰 Tooling

- Revert removing the mavenCentral repo from the muzzle check plugin
  ([#6937](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6937))
- Make java.sql classes available to the agent and extensions
  ([#7038](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7038))

## Version 1.19.2 (2022-11-02)

### 🛠️ Bug fixes

- Bring back two public methods in `opentelemetry-instrumentation-api-semconv` that were mistakenly
  removed in v1.19.1 without a deprecation cycle
  ([#7020](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/7020))

## Version 1.19.1 (2022-10-19)

### 🛠️ Bug fixes

- Capture `net.host.name` on netty SERVER spans
  ([#6892](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6892))

## Version 1.19.0 (2022-10-13)

### Migration notes

- Deprecated `HttpServerAttributesGetter.serverName()`, and removed `http.host` and
  `http.server_name` attributes
  ([#6709](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6709))
- Removed previously deprecated configuration flags (see previous release notes for deprecations)
  ([#6771](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6771))
- The restlet-1 instrumentation name has changed from `restlet-1.0` to `restlet-1.1`
  ([#6106](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6106))

### 🌟 New library instrumentation

- Netty 4.1
  ([#6820](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6820))

### 📈 Enhancements

- Move in resource providers from core repo
  ([#6574](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6574))
- Propagate client span context in doOnRequest
  ([#6621](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6621))
- Update attribute key of rocketmq's message tag to use name from semantic conventions
  (`messaging.rocketmq.message_tag`)
  ([#6677](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6677))
- Avoid muzzle matcher warning for the spring-boot-actuator-autoconfigure instrumentation
  ([#6695](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6695))
- Add marker attribute for Log4j 2
  ([#6680](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6680))
- Add marker attribute for Logback
  ([#6652](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6652))
- Add daemon attribute to process.runtime.jvm.threads.count
  ([#6635](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6635))
- Link JMS receive span with the producer span
  ([#6804](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6804))
- Link RabbitMQ receive span with the producer span
  ([#6808](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6808))
- Run context customizers before span start instead of after
  ([#6634](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6634))
- Strip sensitive data from the url
  ([#6417](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6417))
- Extract `net.peer.{name,port}` on start for CLIENT spans
  ([#6828](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6828))

### 🛠️ Bug fixes

- Fix scheduled job experimental attributes property
  ([#6633](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6633))
- Fix AutoConfigurationCustomizer.addPropertiesSupplier not taking into account configuration-file
  ([#6697](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6697))
- Fix Dubbo NPE and trace propagation issue
  ([#6640](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6640))
- Fix directory separator in ProcessResource attributes
  ([#6716](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6716))
- Fix instrumentation for tomcat 10.1.0
  ([#6766](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6766))
- Fix instrumentation name for jaxrs-2.0-annotations
  ([#6770](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6770))
- Fix instrumentation for vert.x 4.3.4
  ([#6809](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6809))
- Fix Restlet v2 `Message#getAttributes` calls
  ([#6796](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6796))
- Guard against null HttpContext
  ([#6792](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6792))

## Version 1.18.0 (2022-09-14)

The `opentelemetry-instrumentation-api` artifact is declared stable in this release.

### Migration notes

- There were a few late-breaking changes in `opentelemetry-instrumentation-api`, prior to it being
  declared stable:
  * `InstrumenterBuilder.addAttributesExtractors(AttributesExtractor...)` was removed, use instead
    `addAttributesExtractors(AttributesExtractor)` or
    `addAttributesExtractors(Iterable<AttributesExtractor>)`
  * `SpanLinksExtractor.extractFromRequest()` was removed, use instead manual extraction
  * `ErrorCauseExtractor.jdk()` was renamed to `ErrorCauseExtractor.getDefault()`
  * `ClassNames` utility was removed with no direct replacement
- The deprecated `io.opentelemetry.instrumentation.api.config.Config` and related classes
  have been removed
  ([#6501](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6501))
- Net attributes getters were updated to reflect latest specification changes
  ([#6503](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6503))
- The deprecated `Ordered` interface was removed from the `opentelemetry-javaagent-extension-api`,
  use instead the `Ordered` interface from `opentelemetry-sdk-extension-autoconfigure-spi`
  ([#6589](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6589))

### 📈 Enhancements

- Add Spring Boot service name guesser / ResourceProvider
  ([#6516](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6516))
- Move micrometer shim library instrumentation back
  ([#6538](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6538))
- Add grpc status code to metrics attrs
  ([#6556](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6556))
- Add mongo sanitization configuration
  ([#6541](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6541))
- Add kafka client metrics to the javaagent instrumentation
  ([#6533](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6533))
- Add experimental span attribute job.system
  ([#6586](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6586))
- Add code attributes for Logback
  ([#6591](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6591))
- Reactor instrumentation: do not make root context current
  ([#6593](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6593))

### 🛠️ Bug fixes

- Fix default-enabled config
  ([#6491](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6491))
- Fix new jdbc javaagent config
  ([#6492](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6492))
- Fix jaxrs async instrumentation race
  ([#6523](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6523))
- Fix spring webmvc instrumentation name
  ([#6557](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6557))
- Fix spring boot `@WithSpan` handling
  ([#6619](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6619))

## Version 1.17.0 (2022-08-18)

### Migration notes

- The `@WithSpan` and `@SpanAttribute` annotations has been moved from the
  `io.opentelemetry:opentelemetry-extension-annotations` artifact to the
  `io.opentelemetry.instrumentation:opentelemetry-instrumentation-annotations` in order to live and
  evolve alongside the instrumentation itself. The instrumentation will continue to support the old
  artifact for backwards compatibility, but new annotation-based features will only be built out and
  supported with the new annotation artifact.
- `InstrumenterBuilder.newInstrumenter()` is renamed to `InstrumenterBuilder.buildInstrumenter()`
  ([#6363](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6363))
- `io.opentelemetry.instrumentation.api.config.Config` is deprecated
  ([#6360](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6360))
- `HttpCommonAttributesGetter.requestContentLengthUncompressed()` and
  `responseContentLengthUncompressed` are deprecated
  ([#6383](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6383))
- Ktor 2.0 instrumentation name is changed from `io.opentelemetry.ktor-1.0` to
  `io.opentelemetry.ktor-2.0`
  ([#6452](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6452))
- `io.opentelemetry.opentelemetry-annotations-1.0` instrumentation name is changed to
  `io.opentelemetry.opentelemetry-instrumentation-annotations-1.16`
  ([#6450](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6450))
- Liberty instrumentation names are changed from `io.opentelemetry.liberty` and
  `io.opentelemetry.liberty-dispatcher` to `io.opentelemetry.liberty-20.0` and
  `io.opentelemetry.liberty-dispatcher-20.0`
  ([#6456](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6456))
- The 2-arg variant of HttpCommonAttributesGeter#statusCode() is deprecated
  ([#6466](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6466))
- The `opentelemetry-spring-starter` artifact has been renamed to
  `opentelemetry-spring-boot-starter`, the `opentelemetry-zipkin-exporter-starter` artifact has been
  renamed to `opentelemetry-zipkin-spring-boot-starter`, and the
  `opentelemetry-zipkin-exporter-starter` artifact has been renamed to
  `opentelemetry-zipkin-spring-boot-starter`
  ([#6453](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6453))
- Update net semantic convention changes based on recent specification changes:
  `net.peer.ip` renamed to `net.sock.peer.addr`, `net.host.ip` renamed to `net.sock.host.addr`,
  `net.peer.name` renamed to `net.sock.peer.name` for socket-level instrumentation,
  and `NetClientAttributesGetter.peerIp()`, `NetServerAttributesGetter.peerIp()`, and
  `NetServerAttributesGetter.peerPort()` are deprecated
  ([#6268](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6268))

### 📈 Enhancements

- Move buffer pool metrics out of experimental
  ([#6370](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6370))
- Add code attributes to several instrumentations
  ([#6365](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6365))
- Add http.client|server.request|response.size metrics
  ([#6376](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6376))
- Add Kafka instrumentation to the Spring Boot starter
  ([#6371](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6371))
- Extract HTTP request & response content length from headers
  ([#6415](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6415))
- Support DataDirect and Tibco Jdbc URLs
  ([#6420](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6420))
- Set http.route in spring-autoconfigure webmvc instrumentation
  ([#6414](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6414))
- Grizzly: capture all matching request & response headers
  ([#6463](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6463))
- Capture messaging header value as span attribute
  ([#6454](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6454))
- Add JDBC-specific sanitizer property
  ([#6472](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6472))

### 🛠️ Bug fixes

- Fix duplicate spans for Quarkus gRPC server
  ([#6356](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6356))
- Update Kafka library instrumentation to support version 3.0.0 and later
  ([#6457](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6457))
- Mongodb: avoid duplicate tracing
  ([#6465](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6465))
- Fix netty instrumentation NoSuchElementException
  ([#6469](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6469))

## Version 1.16.0 (2022-07-19)

### Migration notes

- Config has been replaced by ConfigProperties in Javaagent extensions SPIs
- The deprecated TimeExtractor has been removed
- The `opentelemetry-instrumentation-api-annotation-support` artifact has been renamed to
  `opentelemetry-instrumentation-annotation-support`
- The `opentelemetry-annotations` instrumentation suppression key has been renamed to
  `opentelemetry-extension-annotations`
- The 'otel.javaagent.experimental.use-noop-api' flag has been removed, as this capability is now
  available via the `otel.experimental.sdk.enabled` flag

### 🌟 New javaagent instrumentation

- C3P0 connection pool metrics
  ([#6174](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6174))
- JVM buffer pool metrics
  ([#6177](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6177))
- Kafka client metrics
  ([#6138](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6138))
- dropwizard-metrics to OpenTelemetry metrics bridge
  ([#6259](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6259))

### 🌟 New library instrumentation

- C3P0 connection pool metrics
  ([#6174](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6174))
- JVM buffer pool metrics
  ([#6177](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6177))
- Kafka client metrics
  ([#6138](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6138))
- Add metrics & micrometer support to spring-boot-autoconfigure
  ([#6270](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6270))
- Spring Kafka library instrumentation
  ([#6283](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6283))

### 📈 Enhancements

- Update GraphQL instrumentation to match spec
  ([#6179](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6179))
- Make rpc.grpc.status_code required
  ([#6184](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6184))
- Always pass Context when recording HttpServerMetrics
  ([#6223](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6223))
- Capture enduser.id in servlet instrumentation
  ([#6225](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6225))
- Support metric view configuration file in the Javaagent
  ([#6228](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6228))
- Aws sdk2 sqs context propagation
  ([#6199](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6199))
- More Spring JMS support
  ([#6308](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6308))
- Hikaricp: Avoid registering duplicate metrics
  ([#6325](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6325))

### 🛠️ Bug fixes

- Fix liberty net.peer.port
  ([#6274](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6274))

## Version 1.15.0 (2022-06-16)

### Migration notes

- The `opentelemetry-jboss-logmanager-1.1` artifact has been renamed to
  `opentelemetry-jboss-logmanager-appender-1.1`
- The play instrumentation name has changed from `play` to `play-mvc`
  ([#6106](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6106))
- The vertx-http-client instrumentation name has changed from `vertx-client` to `vertx-http-client`
  ([#6106](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6106))
- The metric `process.runtime.java.memory.max` has been renamed
  to `process.runtime.java.memory.limit`
  ([#6161](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6161))

### 🌟 New javaagent instrumentation

- JVM classes metrics
  ([#6069](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6069))
- JVM threads metrics
  ([#6070](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6070))
- Vibur DBCP connection pool metrics
  ([#6092](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6092))
- tomcat-jdbc connection pool metrics
  ([#6102](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6102))
- JVM cpu metrics
  ([#6107](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6107))
- Oracle UCP connection pool metrics
  ([#6099](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6099))
- Apache DBCP2 datasource metrics
  ([#6175](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6175))
- Add instrumentation for JAX-RS 3.0
  ([#6136](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6136))

### 🌟 New library instrumentation

- JVM classes metrics
  ([#6069](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6069))
- JVM threads metrics
  ([#6070](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6070))
- Vibur DBCP connection pool metrics
  ([#6092](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6092))
- tomcat-jdbc connection pool metrics
  ([#6102](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6102))
- JVM cpu metrics
  ([#6107](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6107))
- Oracle UCP connection pool metrics
  ([#6099](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6099))
- Apache DBCP2 datasource metrics
  ([#6175](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6175))

### 📈 Enhancements

- Enable grizzly instrumentation by default
  ([#6049](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6049))
- Instrumentation for redisson 3.17.2+
  ([#6096](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6096))
- Instrumentation for jboss-logmanager getMdcCopy()
  ([#6112](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6112))
- Allow specifying a comma separated list of extensions
  ([#6137](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6137))

### 🛠️ Bug fixes

- Fix redisson ClassCastException
  ([#6054](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6054))
- Fix debug logging
  ([#6085](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6085))
- HttpURLConnection instrumentation can capture wrong http.method
  ([#6053](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6053))
- fix bug: get return type in a wrong way for method instrumentation
  ([#6118](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6118))
- Show correct runnable name in spring scheduling actuator
  ([#6140](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6140))
- Fix ClassCastException in JDBC instrumentation
  ([#6088](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6088))

### 🧰 Tooling

- Remove TimeExtractor and use internal API for setting start/end timestamps
  ([#6051](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6051))
- Change SpanStatusExtractor to use a builder that can set status description
  ([#6035](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6035))
- Make gRPC metadata available to AttributeExtractors
  ([#6125](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6125))

## Version 1.14.0 (2022-05-17)

### Migration notes

- The `opentelemetry-log4j-appender-2.16` artifact has been renamed to
  `opentelemetry-log4j-appender-2.17`
- The `opentelemetry-log4j-context-data-2.16-autoconfigure` artifact has been renamed to
  `opentelemetry-log4j-context-data-2.17-autoconfigure`
- Micrometer library instrumentation has been removed as it has been moved to the core repo and
  is now published under `io.opentelemetry:opentelemetry-micrometer1-shim`
- The rxjava javaagent instrumentation names for suppression have changed to `rxjava`
- `AgentListener#beforeAgent()` has been deprecated, as it is not expect to be needed by extensions
  authors
- `ConfigPropertySource` has been deprecated in favor of `ConfigCustomizer`
- Several changes in the Instrumentation API
  - `RequestMetrics` has been renamed to `OperationMetrics`
  - `RequestListener` has been renamed to `OperationListener`
  - `ErrorCauseExtractor#extractCause()` has been renamed to `extract()`
  - `ContextCustomizer` and `RequestListener` `start()`/`end()` methods have been renamed to
    `onStart()`/`onEnd()`
- The `opentelemetry-javaagent-instrumentation-api` artifact has been merged into the
  `opentelemetry-javaagent-extension-api` artifact

### 🌟 New javaagent instrumentation

- Add jboss-logmanager mdc support
  ([#5842](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5842))
- Spring-kafka single record instrumentation
  ([#5904](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5904))
- Add metrics instrumentation for grpc
  ([#5923](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5923))
- Add vertx-kafka-client instrumentation
  ([#5973](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5973),
  [#5982](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5982))
- Hide the GC runtime metrics behind an experimental config flag
  ([#5990](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5990))
- Add HikariCP connection pool metrics
  ([#6003](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6003))

### 🌟 New library instrumentation

- Add metrics instrumentation for grpc
  ([#5923](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5923))
- Add HikariCP library instrumentation
  ([#6023](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6023))

### 📈 Enhancements

- Enable span suppression by SpanKey by default
  ([#5779](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5779))
- record exception in dubbo high version
  ([#5892](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5892))
- Introduce LocalRootSpan (replacing ServerSpan)
  ([#5896](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5896))
- Add javaagent<->application context bridge for HttpRouteHolder
  ([#5838](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5838))
- Exclude spring temporary type matching class loader
  ([#5912](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5912))
- Load agent classes child first
  ([#5950](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5950))
- Avoid looking up annotation types during type matching
  ([#5906](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5906))
- Add an SPI for customizing Config just before it's set
  ([#6010](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6010))

### 🛠️ Bug fixes

- Fix duplicate class error on Android build
  ([#5882](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5882))
- Avoid npe in netty 4.1 instrumentation
  ([#5902](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5902))
- Fix logging exporter autoconfiguration issue
  ([#5928](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5928))
- fix NPE for commons-httpclient v3.1
  ([#5949](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5949))
- Exclude duplicate project classes from inst/
  ([#5957](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5957))
- Ignore known problematic jdbc wrappers
  ([#5967](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5967))
- Fix default enabled for runtime and oshi metrics
  ([#5989](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5989))
- Mitigate against another kafka leak
  ([#6021](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/6021))

## Version 1.13.1 (2022-04-22)

### 🛠️ Bug fixes

- Fix duplicate class error on Android build
  ([#5882](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5882))
- Fix spring-kafka single record instrumentation
  ([#5904](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5904))

## Version 1.13.0 (2022-04-19)

### Migration notes

- Micrometer instrumentation is now automatically applied to spring-boot-actuator apps
- Some configuration properties have been renamed:
  * `otel.instrumentation.common.experimental.suppress-controller-spans`
    → `otel.instrumentation.common.experimental.controller-telemetry.enabled`
    (important: note that the meaning is inverted)
  * `otel.instrumentation.common.experimental.suppress-view-spans`
    → `otel.instrumentation.common.experimental.view-telemetry.enabled`
    (important: note that the meaning is inverted)
  * `otel.instrumentation.netty.always-create-connect-span`
    → `otel.instrumentation.netty.connection-telemetry.enabled`
  * `otel.instrumentation.reactor-netty.always-create-connect-span`
    → `otel.instrumentation.reactor-netty.connection-telemetry.enabled`
- Runtime memory metric names were updated to reflect
  [semantic conventions](https://github.com/open-telemetry/opentelemetry-specification/blob/main/specification/metrics/semantic_conventions/runtime-environment-metrics.md#jvm-metrics)
- Micrometer library instrumentation has been deprecated as it has been moved to the core repo and
  is now published under `io.opentelemetry:opentelemetry-micrometer1-shim`
- Library instrumentation entry points have been renamed from `*Tracing` to `*Telemetry`

### 🌟 New javaagent instrumentation

- GraphQL
  ([#5583](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5583))
- JBoss Log Manager
  ([#5737](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5737))
- Apache HttpClient 5.x async client
  ([#5697](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5697))

### 🌟 New library instrumentation

- GraphQL
  ([#5583](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5583))
- Ktor 2
  ([#5797](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5797))

### 📈 Enhancements

- Elasticsearch rest client low cardinality span names
  ([#5584](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5584))
- Implement "Prometheus mode" for better micrometer->OTel->Prometheus support
  ([#5537](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5537))
- Apply micrometer instrumentation to spring-boot-actuator apps
  ([#5666](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5666))
- Sql sanitizer: handle double quoted table names
  ([#5699](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5699))
- Spring Boot Starter service-name is constant
  ([#5359](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5359))
- Update runtime memory metrics to reflect semantic conventions
  ([#5718](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5718))
- change rpc type in apache dubbo
  ([#5432](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5432))
- Rework context propagation to redisson async callback
  ([#5748](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5748))
- Resolve end strategy after WithSpan method instead of before.
  ([#5756](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5756))
- Allow scanning instrumented reactor publishers and only allow registe…
  ([#5755](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5755))
- Faster type matching
  ([#5724](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5724))
- Use UnsynchronizedAppenderBase as base class for our logback appender
  ([#5818](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5818))
- Do not set the http.route attribute in JSF instrumentations
  ([#5819](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5819))
- Use micrometer1-shim in micrometer javaagent instrumentation, deprecate library instrumentation
  ([#5820](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5820))
- Rename netty `always-create-connect-span` property to `connection-telemetry`
  ([#5834](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5834))
- Update the http.route attribute even for not sampled server spans
  ([#5844](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5844))

### 🛠️ Bug fixes

- Fix possible deadlock
  ([#5585](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5585))
- Prevent possible deadlock in downstream distro
  ([#5830](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5830))
- Limit problems from kafka iterator instrumentation thread context leak
  ([#5826](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5826))

### 🧰 Tooling

- Remove deprecated methods from instrumentation-api and library instrumentations
  ([#5575](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5575))
- Split out RpcAttributesGetter
  ([#5548](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5548))
- Run tests with jdk17
  ([#5598](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5598))
- Split out MessagingAttributesGetter
  ([#5626](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5626))
- Run Gradle and compile code with Java 17
  ([#5623](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5623))
- Rename library entrypoints to Telemetry
  ([#5624](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5624))
- Add InstrumenterBuilder.addRequestListener
  ([#5655](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5655))
- Simplify HttpUrlConnection instrumentation
  ([#5673](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5673))
- Convert all logging statements from slf4j to jul
  ([#5674](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5674))
- Allows passing an OpenTelemetry instance to registerObservers() methods.
  ([#5716](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5716))
- Make it possible to register multiple helper resources under the same…
  ([#5703](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5703))
- Split out instrumentation-api-semconv
  ([#5721](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5721))
- Move ClassNames & SpanNames to .util package
  ([#5746](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5746))
- Library instrumentation should read its version from a file
  ([#5692](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5692))
- Rename view and controller suppression config properties
  ([#5747](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5747))
- Deprecate AttributesExtractor#set() method
  ([#5749](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5749))
- Cleanup Config & ConfigBuilder API
  ([#5733](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5733))
- Instrumenter instrumentation version and schema url
  ([#5752](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5752))

## Version 1.12.1 (2022-03-17)

### 🛠️ Bug fixes

- Elasticsearch rest client low cardinality span name
  ([#5584](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5584))
- Fix possible deadlock
  ([#5585](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5585))

## Version 1.12.0 (2022-03-12)

### 🌟 New javaagent instrumentation

- Add Azure SDK instrumentation
  ([#5467](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5467))

### 📈 Enhancements

- Use repository interface name in spring data operation name
  ([#5352](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5352))
- Change the way Micrometer LongTaskTimer is bridged
  ([#5338](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5338))
- Updates to http.server_name
  ([#5369](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5369))
- Support forwarded proto field and x-forwarded-proto
  ([#5357](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5357))
- Remove server span peer name
  ([#5404](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5404))
- Add peer service support back to couchbase26
  ([#5451](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5451))
- Remove duplicative JAXRS HttpClient instrumentation
  ([#5430](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5430))
- Add experimental thread attributes for logs
  ([#5474](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5474))
- Add log4j 1.2 appender MDC capture
  ([#5475](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5475))
- Capture logback formatted message
  ([#5497](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5497))
- Add JBoss java.util.logging support
  ([#5498](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5498))
- Disable the messaging receive span telemetry by default
  ([#5500](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5500))
- Remove old experimental properties in CapturedHttpHeaders
  ([#5524](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5524))
- Avoid conflicts in Micrometer description mapping
  ([#5452](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5452))

### 🛠️ Bug fixes

- Fix another reverse lookup
  ([#5393](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5393))
- Regression in loading the prometheus exporter
  ([#5408](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5408))
- Fix muzzle failure on calls to primitive array clone
  ([#5405](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5405))
- Fix regression in spring-scheduling span name
  ([#5436](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5436))
- Fix android desugaring for HashMap.forEach
  ([#5468](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5468))
- Fix duplicate class definition of ContextDataProvider
  ([#5528](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5528))
- Do not propagate gRPC deadline when propagating OTel context via javaagent
  ([#5543](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5543))

### 🧰 Tooling

- Split out CodeAttributesGetter
  ([#5342](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5342))
- Add prometheus smoke test
  ([#5417](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5417))
- Set custom gRPC client/server span name extractor
  ([#5244](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5244))
- Split out DbClientAttributesGetter and SqlClientAttributesGetter
  ([#5354](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5354))
- Add builders for setting optional attributes on HTTP extractors
  ([#5347](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5347))
- Write http server tests in java
  ([#5501](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5501))
- Deprecate CapturedHttpHeaders and replace it with builder methods
  ([#5533](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5533))
- Update to Groovy 4
  ([#5532](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5532))

## Version 1.11.1 (2022-02-21)

### 🛠️ Bug fixes

- Regression in loading the prometheus exporter
  ([#5408](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5408))

## Version 1.11.0 (2022-02-11)

### Migration notes

- The previous release (1.10.0) deprecated the entire `io.opentelemetry.instrumentation.api.tracer`
  package in the `instrumentation-api` artifact, and the package was removed in this release.
- The javaagent `-slim` artifact has been dropped in this release, because the exporters are much
  smaller now and there is no longer a significant size difference between the `-slim` and default
  artifacts.
- The `opentelemetry-aws-lambda-1.0` has been split into two artifacts
  `opentelemetry-aws-lambda-core-1.0` and `opentelemetry-aws-lambda-events-2.2`.

### 🌟 New javaagent instrumentation

- Spring RMI
  instrumentation ([#5033](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5033))

### 🌟 New library instrumentation

- Ratpack
  httpclient ([#4787](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4787))

### 📈 Enhancements

- Add `http.route` to server spans where route was already being captured for span name
  ([#5086](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5086),
  [#5240](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5240),
  [#5242](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5242),
  [#5241](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5241),
  [#5239](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5239))
- Use RPC attributes from spec for AWS SDK
  ([#5166](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5166))
- SdkTracerProvider auto closed as separate Context Bean
  ([#5124](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5124)) (#5125)
- Support redisson 3.16.8+
  ([#5201](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5201))
- Support AWS SDK v1 request object subclasses.
  ([#5231](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5231))
- Remove slim artifact
  ([#5251](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5251))
- kotlinx-coroutines-reactor context propagation
  ([#5196](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5196))
- Log a warning whenever GlobalOpenTelemetry.set() is called
  ([#5264](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5264))
- Use `http.route` in `HttpServerMetrics`
  ([#5266](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5266))
- Use VirtualField for associating netty listener with wrapper
  ([#5282](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5282))
- Add code attributes to spring-scheduling spans
  ([#5306](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5306))
- Propagate context into redisson async callback
  ([#5313](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5313))
- Add max measurements to Micrometer Timer & DistributionSummary
  ([#5303](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5303))
- Make it possible to configure base time unit used by the Micrometer bridge
  ([#5304](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5304))
- Make HttpClientMetrics report low cardinality metrics
  ([#5319](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5319))
- Implement NamingConvention support in Micrometer bridge
  ([#5328](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5328))
- Add net.peer.name and net.peer.port attributes for grpc client span
  ([#5324](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5324))
- Split lambda instrumentation into core and events
  ([#5326](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5326))
- Add jaeger remote sampler to agent
  ([#5346](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5346))
- Weak cache optimization
  ([#5344](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5344))

### 🛠️ Bug fixes

- Several micrometer instrumentation fixes
  ([#5118](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5118))
- Fix serialisation exception on default lambda events
  ([#4724](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4724))
- NoSuchMethodError when using agent and modules (JPMS)
  ([#5169](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5169))
- Spring boot cloud gateway, context propagation broken
  ([#5188](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5188))
- Akka http server span names are always akka.request #3478
  ([#5150](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5150))
- Recover from duplicate class definition errors
  ([#5185](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5185))
- Fix serialization for quartz JobExecutionContext
  ([#5263](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5263))
- End jedis span when operation actually ends
  ([#5256](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5256))
- Enable oshi ProcessMetrics in javaagent
  ([#5281](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5281))
- Add missing return type matchers to the executor instrumentation
  ([#5294](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5294))
- Fix triggering of DNS lookup
  ([#5297](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5297))
- Avoid potential for reverse name lookup
  ([#5305](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5305))
- Fix WeakConcurrentMap memory leak
  ([#5316](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5316))
- AWS Lambda instrumentation requires jackson and lambda-events on the classpath
  ([#5326](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5326))

### 🧰 Tooling

- Convert InstrumentationTestRunner from interface to abstract class
  ([#5112](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5112))
- Parameterize VirtualField field type
  ([#5165](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5165))
- Remove old TraceUtils and use InstrumentationTestRunner#run*Span() (almost) everywhere
  ([#5160](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5160))
- Remove deprecated tracer API
  ([#5175](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5175))
- Remove HttpServerTest#extraAttributes() method
  ([#5176](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5176))
- Rename ServerSpanNaming to HttpRouteHolder
  ([#5211](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5211))
- Don't run testLatestDeps on alpha/beta/rc versions
  ([#5258](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5258))
- Refactor HTTP attributes extractors to use composition over inheritance
  ([#5030](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5030),
  [#5194](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5194)
  [#5267](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5267))
- Refactor AttributesExtractor so that it extracts route from Context
  ([#5288](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5288))
- Publish gradle-plugins to Maven Central
  ([#5333](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5333))

## Version 1.10.1 (2022-01-27)

### 🛠️ Bug fixes

- Regression in project reactor context propagation instrumentation
  ([#5188](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5188))
- Recover from duplicate class definition errors
  ([#5185](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5185))
- StringIndexOutOfBoundsException in AWS SDK v1 when using request object subclass
  ([#5231](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5231))
- Update to OTel SDK 1.10.1
  ([#5218](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5218))

## Version 1.10.0 (2022-01-15)

### Migration notes

- The `opentelemetry-log4j-2.13.2` artifact has been renamed
  to `opentelemetry-context-data-2.16-autoconfigure`
- The `opentelemetry-logback-1.0` artifact has been renamed to `opentelemetry-logback-mdc-1.0`
- The `opentelemetry-ratpack-1.4` artifact has been renamed to `opentelemetry-ratpack-1.7`
  and only supports Ratpack 1.7 and above now

### 🌟 New javaagent instrumentation

- Logback appender instrumentation to send logs through the OpenTelemetry logging pipeline
  ([#4939](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4939),
  [#4968](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4968))
- Log4j 2.x appender instrumentation to send logs through the OpenTelemetry logging pipeline
  ([#4944](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4944),
  [#4959](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4959),
  [#4966](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4966))
- Log4j 1.2 appender instrumentation to send logs through the OpenTelemetry logging pipeline
  ([#4943](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4943))
- java.util.logging instrumentation to send logs through the OpenTelemetry logging pipeline
  ([#4941](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4941))
- Micrometer instrumentation to send micrometer metrics through the OpenTelemetry metrics pipeline
  ([#4919](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4919),
  [#5001](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5001),
  [#5017](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5017))

### 🌟 New library instrumentation

- Logback appender to send logs through the OpenTelemetry logging pipeline
  ([#4984](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4984))
- Log4j 2.x appender to send logs through the OpenTelemetry logging pipeline
  ([#4375](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4375),
  [#4907](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4907))
- Ktor instrumentation
  ([#4983](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4983))
- Micrometer instrumentation to send micrometer metrics through the OpenTelemetry metrics pipeline
  ([#5063](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5063))

### 📈 Enhancements

- Renamed Apache Dubbo and Log4j MDC library artifacts
  ([#4779](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4779))
- Added http4 handler to camel instrumentation
  ([#4650](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4650))
- Capture servlet request parameters
  ([#4703](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4703))
- Propagate Context instead of SpanContext in Kafka instrumentation
  ([#4806](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4806))
- Instrument ContextPropagationOperator to bridge lib/agent calls
  ([#4786](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4786))
- Add shouldStart() call to Armeria server instrumentation
  ([#4843](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4843))
- Capture RPC metrics
  ([#4838](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4838))
- Update log4j library base version
  ([#4914](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4914))
- Rename log4j-thread-context modules to log4j-context-data
  ([#4957](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4957))
- Support latest oshi version
  ([#4993](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4993))
- Support latest RxJava version
  ([#4954](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4954))
- Create producer span from spring integration instrumentation
  ([#4932](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4932))
- Capture servlet request parameters at the end of the request
  ([#5019](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5019))
- Don't extract deprecated cassandra keyspace attribute
  ([#5041](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5041))
- Add OTLP logs exporters
  ([#5060](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5060),
  [#5088](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5088))
- End redisson span when the operation actually ends
  ([#5073](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5073))
- Don't capture high-cardinality http.target as metrics attribute
  ([#5081](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5081))

### 🛠️ Bug fixes

- Remove virtual field interfaces from reflection results
  ([#4722](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4722))
- Work around jvm crash on early 1.8
  ([#4345](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4345))
- Fix http.url handing in vert.x 3 http client
  ([#4739](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4739))
- Capture missing RMI spans
  ([#4764](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4764))
- Avoid crashing on early 1.8 openjdk vms
  ([#4789](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4789))
- Fix Quarkus correlation
  ([#4883](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4883))
- Fix RabbitMQ instrumentation consumption on empty headers
  ([#4903](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4903))
- Fix NPE in Apache HttpClient 4.0 instrumentation
  ([#4913](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4913))
- Fix NPE in RocketMQ instrumentation
  ([#4901](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4901))
- Fix time units in HTTP & RPC metrics
  ([#4963](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4963))
- Fix some gauge types
  ([#4962](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4962))
- Fix context propagation for undertow async dispatch
  ([#4950](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4950))
- Fix redefinition failure on openj9
  ([#5009](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5009))
- Fix NPE in rmi server instrumentation
  ([#5042](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/5042))

### 🧰 Tooling

- Merge start and end time extractors
  ([#4692](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4692))
- Move cache implementations to internal package
  ([#4746](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4746))
- Reorganize shared servlet code (intro
  to [#4317](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4317))
  ([#4785](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4785))
- Move `AppServerBridge` and `MappingResolver` to `servlet-common:bootstrap`
  ([#4817](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4817))
- Move `ServletContextPath` to `servlet-common:bootstrap`
  ([#4824](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4824))
- Expose AutoConfiguredOpenTelemetrySdk to AgentListener
  ([#4831](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4831))
- Deprecate the Tracer API
  ([#4868](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4868))
- Remove ConfigPropertiesAdapter as it's no longer needed
  ([#4888](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4888))
- Refactor `ServerSpanNaming` (in preparation for `http.route`)
  ([#4852](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4852))
- Move SpanKey to internal package
  ([#4869](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4869))

## Version 1.9.2 (2022-01-07)

### 🛠️ Bug fixes

- Fix reactor-netty memory/connection leak
  ([#4867](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4867))

## Version 1.9.1 (2021-12-01)

### 🛠️ Bug fixes

- Shade class references within AWS SDK service files
  ([#4752](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4752))

## Version 1.9.0 (2021-11-25)

### 📈 Enhancements

- Don't report 400 level as error for SERVER spans
  ([#4403](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4403))
- Netty instrumentation now captures `http.scheme`
  ([#4446](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4446),
  [#4576](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4576))
- Stabilize HTTP headers capturing configuration property names
  ([#4459](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4459))
- Add metrics to remaining http instrumentation
  ([#4541](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4541))
- Remove hibernate session spans
  ([#4538](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4538))
- Support Jedis 4
  ([#4555](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4555))
- Trace DNS resolution in Netty 4.1 and reactor-netty
  ([#4587](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4587),
  [#4627](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4627))
- Update garbage collector instruments to be async counters
  ([#4600](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4600))
- Update HTTP metrics view to match the specification
  ([#4556](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4556))
- Improve Spring Integration interceptor ordering
  ([#4602](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4602))
- Support Restlet 2.0
  ([#4535](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4535))
- Improved capture of couchbase queries
  ([#4615](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4615))
- Trace SSL handshakes in netty 4.0 and 4.1
  ([#4635](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4635),
  [#4604](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4604))
- Capture exception on finatra controller spans
  ([#4669](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4669))
- Capture exception on async servlet spans
  ([#4677](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4677))
- Automatic AWS library instrumentor
  ([#4607](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4607))
- Support spring boot 2.6.0
  ([#4687](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4687))

### 🛠️ Bug fixes

- Preserve caught netty exception in the context instead of calling end()
  ([#4413](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4413))
- Extract net attributes both on start and on end in netty HTTP client
  ([#4420](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4420))
- Capture metric dimensions from end attributes also
  ([#4430](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4430))
- Avoid logging servlet3 muzzle failure when running on servlet2
  ([#4474](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4474))
- Fix JettyHttpClient9TracingInterceptor NullPointerException
  ([#4527](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4527))
- Fix context propagation in tomcat thread pool
  ([#4521](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4521))
- Add missing java.util.logging.Logger methods to PatchLogger
  ([#4540](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4540))
- Fix ClassCircularityError when running with security manager
  ([#4557](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4557))
- Fix sun.misc.Unsafe generation on Java 17
  ([#4558](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4558))
- Fix IndexOutOfBounds in apache http clients
  ([#4575](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4575))
- Fix RMI instrumentation on Java 17
  ([#4577](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4577))
- Fix Spring Integration instrumentation name
  ([#4601](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4601))
- Capture instrumentation version provided by application tracer correctly when using agent
  ([#4630](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4630))
- Ensure that netty 4.0 instrumentation is not applied to 4.1
  ([#4626](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4626))
- Fix muzzle problems happening when netty without SSL is used
  ([#4631](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4631))
- Fix memory leak when using ktor-client-java
  ([#4637](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4637))
- Fix quartz instrumentation name
  ([#4657](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4657))
- Fix Spring Integration context leak
  ([#4673](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4673))
- Fix exemplars
  ([#4678](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4678))
- Fix and enforce Android support
  ([#4671](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4671),
  [#4667](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4667)
  [#4505](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4505))

### 🧰 Tooling

- Migrate to Spock 2
  ([#4458](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4458))
- Rename `newBuilder()` to `builder()`
  ([#4475](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4475))
- Sync gradle-plugins version with main project
  ([#4248](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4248))
- Muzzle match only once in each class loader
  ([#4543](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4543))
- Inject helper resources only once
  ([#4573](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4573))
- Improve muzzle check for constructors
  ([#4591](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4591))
- Add version to the InstrumenterBuilder and Instrumenter
  ([#4611](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4611))
- Add a ClassAndMethod class to Instrumentation API
  ([#4619](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4619))
- Implement a dedicated reactor-netty 1.0 instrumentation
  ([#4662](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4662))
- Remove gRPC dependency for export
  ([#4674](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4674))
- Start using Gradle Enterprise instance
  ([#4663](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4663))

## Version 1.8.0 - Bad Release

Due to an issue in the publishing infrastructure, a bad release was published as 1.8.0. Do not use
it.

## Version 1.7.0 (2021-10-19)

### 📈 Enhancements

- Change the default javaagent artifact to have exporters, introduce new `-slim` artifact,
  and deprecate the `-all` artifact
  ([#4106](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4106))
- Support jlinked images without jdk.unsupported module
  ([#4154](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4154))
  ([#4124](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4124))
- Added experimental option to suppress messaging receive spans
  ([#4187](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4187))
  ([#4204](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4204))
- Refine 404 handling in Restlet instrumentation
  ([#4206](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4206))
- Remove dynamo db.name attribute
  ([#4208](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4208))
- Remove capturing http.url in server instrumentation in favor of http.scheme, http.host
  and http.target
  ([#4209](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4209))
- Intern db info to reduce memory consumption
  ([#4263](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4263))
- Better JAX-RS async cancel handling
  ([#4279](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4279))
- Extract HTTP request/response headers as span attributes
  ([#4237](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4237),
  [#4309](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4309),
  [#4320](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4320),
  [#4321](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4321),
  [#4328](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4328),
  [#4395](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4395))
- Support kafka streams 3
  ([#4236](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4236))
- AWS lambda - improvements in custom type handling in wrappers, SQS event wrapper added
  ([#4254](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4254))
- Add code attributes to quartz spans
  ([#4332](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4332))
- Collect more attributes from servlet instrumenter
  ([#4356](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4356))
- Allow reactor instrumentation to pick up spans from reactor context
  ([#4159](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4159))
- Hide virtual field accessor interface methods from reflection
  ([#4390](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4390))

### 🛠️ Bug fixes

- Fix spring context reload issue
  ([#4051](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4051))
- Remove incorrect lettuce db.statement attribute
  ([#4160](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4160))
- Fix tomcat async spans
  ([#4339](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4339))

### 🧰 Tooling

- Add start/end time to RequestListener
  ([#4155](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4155))
- Add context customizer hook to Instrumenter API
  ([#4167](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4167))
- Transform lambda classes
  ([#4182](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4182))
- Separate HTTP client/server AttributesExtractors
  ([#4195](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4195))
- Introduce muzzle-specific interface to InstrumentationModule
  ([#4207](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4207))
- Make it possible to use InstrumentationContext (now VirtualField) from library instrumentation
  ([#4218](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4218))
- Add functionality to generate API changes
  ([#4285](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4285))
- Split NetAttributesExtractor into NetClientAttributesExtractor and NetServerAttributesExtractor
  ([#4287](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4287))
- Back VirtualField with a volatile field
  ([#4355](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4355))
- Convert AttributesExtractor to interface
  ([#4363](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4363))
- Rename some `*InstrumenterBuilder` classes to `*InstrumenterFactory`
  ([#4391](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4391))
- rename `newBuilder()` to `builder()`
  ([#4407](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4407))

## Version 1.6.2 (2021-09-30)

### 🛠️ Bug fixes

- The 1.6.1 patch release was not backwards compatible with javaagent extensions built against 1.6.0
  ([#4245](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4245))

## Version 1.6.1 (2021-09-29)

### 🛠️ Bug fixes

- Fix possible JDBC instrumentation deadlock
  ([#4191](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4191))

## Version 1.6.0 (2021-09-18)

### 🌟 New javaagent instrumentation

- Add instrumentation for Quartz 2.0
  ([#4017](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4017))
- Restlet instrumentation
  ([#3946](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3946))

### 🌟 New library instrumentation

- Add instrumentation for Quartz 2.0
  ([#4017](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4017))
- Restlet instrumentation
  ([#3946](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3946))

### 📈 Enhancements

- Extract Jedis 3 net attributes from InetSocketAddress
  ([#3912](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3912))
- Add option to suppress controller and view spans
  ([#3865](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3865))
- Capture http.user_agent for AsyncHttpClient
  ([#3930](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3930))
- Instrument spring-kafka batch message listeners
  ([#3922](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3922))
- Use unsafe to inject classes to the bootstrap class loader
  ([#4026](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4026))
- Some performance optimizations
  ([#4004](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4004),
  [#4006](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4006),
  [#4008](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4008),
  [#4013](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4013),
  [#4014](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4014))
- Do not fallback to net attributes for http.client_ip
  ([#4063](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4063))
- Start a CONSUMER span for Kafka poll()
  ([#4041](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4041))
- Support otlp http exporter
  ([#4068](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4068))
- Better grpc events
  ([#4098](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4098))

### 🛠️ Bug fixes

- Bridge span keys defined in instrumentation-api
  ([#3911](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3911))
- Hide generated fields and methods from reflection
  ([#3948](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3948))
- Remove invalid message header
  ([#3958](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3958))
- Fix memleak in the Netty ChannelPipeline instrumentation
  ([#4053](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4053))
- Fix grpc instrumentation of callbacks
  ([#4097](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4097))
- Bridge trace builder
  ([#4090](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4090))
- Remove original handler when removelast in netty
  ([#4123](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4123))

### 🧰 Tooling

- Deprecate old extensions
  ([#3825](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3825))
- Add request parameter to EndTimeExtractor
  ([#3947](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3947))
- Make Config behave exactly as SDK DefaultConfigProperties
  ([#4035](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4035))
- Fix extension shading
  ([#4064](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4064))
- Add error parameter to EndTimeExtractor and AttributesExtractor#onEnd()
  ([#3988](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3988))
- Allow adding multiple ContextStore fields to one key class
  ([#4067](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4067),
  [#4084](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4084),
  [#4110](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4110))

## Version 1.5.3 (2021-08-31)

### 🛠️ Bug fixes

- Fix parsing of unclean map values in Config
  ([#4032](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/4032))

## Version 1.5.2 (2021-08-27)

### 🛠️ Bug fixes

- Fix unbounded metrics cardinality, which in particular causes memory leak when not using any
  metrics exporter
  ([#3972](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3972))

## Version 1.5.1 (2021-08-25)

### 🛠️ Bug fixes

- Fix broken Android level 21-25 support in OkHttp 3 library instrumentation
  ([#3910](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3910))
- Fix maven central pom file for the opentelemetry-javaagent artifact
  ([#3929](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3929))
- Fix maven central pom file for the opentelemetry-agent-for-testing artifact
  ([#3935](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3935))

## Version 1.5.0 (2021-08-22)

### 🌟 New library instrumentation

- Library instrumentation for Apache HTTP Client 4.3
  ([#3623](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3623))
- Library instrumentation for Ratpack server
  ([#3749](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3749))

### 📈 Enhancements

- Support Couchbase 3.2.0
  ([#3645](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3645))
- Handle port and IPv6 in forwarded headers
  ([#3651](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3651))
- Set real Hibernate span name on method entry to help samplers
  ([#3603](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3603))
- Reduce overhead of unsampled requests
  ([#3681](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3681))
- Sanitize SQL in Apache Camel instrumentation
  ([#3683](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3683),
  [#3717](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3717))
- Add option to create span on new netty connection
  ([#3707](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3707))
- Propagate context into jdk http client callback
  ([#3719](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3719))
- Instrument Tomcat executor to support async servlets in new Tomcat 9.0.52 release
  ([#3789](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3789))
- Add otlp-logging exporter
  ([#3807](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3807))
- Add new option to support capturing nested client spans of different types
  ([#3691](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3691))
- Propagate context to lettuce callbacks
  ([#3839](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3839))
- Instrument ForkJoinTask.fork()
  ([#3849](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3849))
- Implement a Call.Factory for okhttp 3.x+ library instrumentation
  ([#3812](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3812))
- Record exception in Dubbo instrumentation
  ([#3851](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3851))
- Propagate context to elasticsearch callbacks
  ([#3858](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3858),
  [#3861](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3861))
- Added Vertx http client 4 instrumentation
  ([#3665](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3665))
- Make empty agent bridged context equal root context
  ([#3869](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3869))

### 🛠️ Bug fixes

- Fix OkHttp 3 correlation when using callback under concurrency
  ([#3669](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3669),
  [#3676](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3676))
- Fix Netty span not captured on read timeout
  ([#3613](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3613))
- Fix Netty connection failure handling when listener is lambda
  ([#3569](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3569))
- Fix NullPointerException in Apache HttpAsyncClient instrumentation
  ([#3692](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3692))
- Fix NullPointerException in Tomcat instrumentation
  ([#3705](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3705))
- Fix Apache HttpClient telemetry when host and absolute URI are used
  ([#3694](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3694))
- Fix JDK http client should propagate even when sampled out
  ([#3736](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3736))
- Limit netty exception capture to netty spans
  ([#3809](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3809))
- Fix jetty httpclient returning empty response when instrumented
  ([#3831](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3831),
  [#3833](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3833))
- Don't clobber user decorators in Armeria client instrumentation
  ([#3873](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3873))
- Use valid Java identifiers for message keys
  ([#3863](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3863))
- Fix ClassNotFoundException: HandlerMappingResourceNameFilter in some ear deployments
  ([#3718](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3718))

### 🧰 Tooling

- Improve extension sample documentation and add it to the README file
  ([#3656](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3656))
- Extract muzzle check plugin
  ([#3657](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3657))
- Move instrumentation specific classes out of javaagent-instrumentation-api
  ([#3604](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3604))
- Publish muzzle plugins to Gradle Plugin Portal
  ([#3720](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3720),
  [#3763](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3763))
- Fill `http.client_ip` in ServerInstrumenter
  ([#3756](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3756))
- Fix printMuzzleReferences gradle task
  ([#3808](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3808))
- Introduce stable property for external extensions
  ([#3823](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3823))
- Run tests on j9 JVM during CI
  ([#3764](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3764))
- Support looking up a ContextStore from outside of Advice
  ([#3827](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3827))
- Deprecate MetricExporterFactory
  ([#3862](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3862))
- Don't pass configuration to SDK autoconfigure through system props
  ([#3866](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3866))
- Rename Config get\*Property() methods to get\*()
  ([#3881](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3881))

## Version 1.4.0 (2021-07-20)

### ☢️ Behavioral changes

- Updated all instrumentation names to `io.opentelemetry.{libName}-{libVersion}`
  ([#3411](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3411))
- Updated RabbitMQ to follow semantic conventions
  ([#3425](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3425))

### 🌟 New javaagent instrumentation

- Jetty 9 HTTP client instrumentation
  ([#3079](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3079))

### 🌟 New library instrumentation

- Jetty 9 HTTP client instrumentation
  ([#3079](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3079))
- Jdbc instrumentation
  ([#3367](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3367))

### 📈 Enhancements

- Make @RabbitListener propagate context properly
  ([#3339](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3339))
- Add peer.service to grpc javaagent instrumentation
  ([#3357](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3357))
- Propagate context to cassandra4 callbacks
  ([#3371](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3371))
- Update Armeria instrumentation to support new Armeria 1.9.0 release
  ([#3407](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3407))
- Context propagation for ratpack Execution.fork()
  ([#3416](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3416))

### 🛠️ Bug fixes

- Fix Kafka stream instrumentation to support Kafka 2.6 and above
  ([#3438](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3438))
- Fix Dubbo trace/span cross-process propagation
  ([#3442](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3442))
- Fix `peer.service` configuration mapping
  ([#3378](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3378))

### 🧰 Tooling

- Hide Config#create() method and use builder everywhere
  ([#3338](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3338))
- Ignore task classes using IgnoredTypesConfigurer
  ([#3380](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3380))
- Exclude duplicate classes from final jars
  ([#3432](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3432),
  [#3430](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3430))
- Port AsyncSpanEndStrategy to Instrumenter API
  ([#3262](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3262))
- Rename `opentelemetry-javaagent-api` artifact to `opentelemetry-javaagent-instrumentation-api`
  ([#3513](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3513))

## Version 1.3.1 (2021-06-23)

### 🛠️ Bug fixes

- Fix incorrect dependency in published BOM
  ([#3376](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3376))
- Fix UnsupportedOperationException with reactor-rabbitmq
  ([#3381](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3381))
- Fix Spring JMS not being instrumented
  ([#3359](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3359))

## Version 1.3.0 (2021-06-17)

### ☢️ Behavioral changes

- Update agent logger prefix
  ([#3007](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3007))
- Remove khttp instrumentation
  ([#3087](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3087))
- Enable akka actor instrumentation by default
  ([#3173](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3173))

### 🌟 New javaagent instrumentation

- Spring Integration javaagent instrumentation
  ([#3295](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3295))

### 🌟 New library instrumentation

- Spring Integration library instrumentation
  ([#3120](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3120))

### 📈 Enhancements

- Support peer-service-mapping in OkHttp3 instrumentation
  ([#3063](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3063))
- Low cardinality span names for Hibernate spans
  ([#3106](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3106))
- Propagate context to armeria callbacks
  ([#3108](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3108))
- Add attributes to netty connection failure span
  ([#3115](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3115))
- Defer initialization of OpenTelemetry in spring-boot-autoconfigure
  ([#3171](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3171))
- Support couchbase 3.1.6
  ([#3194](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3194))
- New experimental support for agent extensions
  ([#2881](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2881),
  [#3071](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3071),
  [#3226](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3226),
  [#3237](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3237))
- Propagate context to akka http callbacks
  ([#3263](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3263))

### 🛠️ Bug fixes

- Remove Netty instrumented handler wrapper when original handler is removed
  ([#3026](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3026))
- Fix memory leak when Netty handler is a lambda
  ([#3059](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3059))
- Fix race condition on Undertow
  ([#2992](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2992))
- Remove db.connection_string from redis instrumentation
  ([#3094](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3094))
- Fix context propagation leak in Akka instrumentation
  ([#3099](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3099))
- Fix webflux handler span sporadically not ending
  ([#3150](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3150))
- End span on cancellation of subscription to reactive publishers
  ([#3153](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3153))
- End span on cancellation of Guava future
  ([#3175](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3175))
- Create Netty connection failure span only when first operation fails
  ([#3228](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3228))
- Internal instrumentation should always be enabled by default
  ([#3257](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3257))
- Fix context propagation leak in Akka HTTP instrumentation
  ([#3264](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3264))
- Only include exporters in the `-all` jar
  ([#3286](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3286))
- Fix ForkJoinPool sometimes not instrumented
  ([#3293](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3293))

### 🧰 Tooling

- Migrate MuzzlePlugin to Java
  ([#2996](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2996),
  [#3017](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3017))
- Refactor TypeInstrumentation#transformers() method
  ([#3019](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3019))
- Change a couple of Longs to Integers in Instrumenter API
  ([#3043](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3043))
- Add peer.service to Instrumenter API
  ([#3050](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3050))
- Add response type parameter to db attributes extractor
  ([#3093](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3093))
- Add optimized Attributes implementation for Instrumenter
  ([#3136](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3136))
- Rename ComponentInstaller to AgentListener and add #order() method
  ([#3182](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3182))
- Update ByteBuddy
  ([#3254](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3254))
- Introduce IgnoredTypesConfigurer SPI to enable defining per-module ignores
  ([#3219](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3219))
- Extract agent shadow configuration to conventions script
  ([#3256](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3256))
- Deprecate SpanExporterFactory in favor of ConfigurableSpanExporterProvider
  ([#3299](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3299))
- Refactor span names class
  ([#3281](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3281))
- Move http client/server testing dependencies to internal package
  ([#3305](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/3305))

## Version 1.2.0 (2021-05-14)

### ☢️ Behavioral changes

- AWS lambda flush timeout raised to 10 seconds
  ([#2855](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2855))
- `SERVER` span names improved for Spring MVC, Grails, Wicket, and Struts
  ([#2814](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2814))
- `SERVER` span names improved for Servlet filters
  ([#2887](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2887))
- `SERVER` span names improved for Resteasy
  ([#2900](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2900))
- `SERVER` span names improved for Jersey and CXF
  ([#2919](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2919))
- JAX-RS `@ApplicationPath` annotation captured as part of `SERVER` span name
  ([#2824](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2824))
- RequestDispatcher `forward()` and `include()` internal spans removed
  ([#2816](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2816))
- Raised gRPC min version supported to 1.6 in order to use new gRPC context bridge API
  ([#2948](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2948))

### 🌟 New javaagent instrumentation

- RxJava 3
  ([#2794](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2794))

### 🌟 New library instrumentation

- RxJava 3
  ([#2794](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2794))

### 📈 Enhancements

- Support sub-millisecond precision for start/end times on Java 9+
  ([#2600](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2600))
- `@WithSpan` async support added for methods returning async Reactor 3.x types
  ([#2714](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2714))
- `@WithSpan` async support added for methods returning Guava ListenableFuture
  ([#2811](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2811))
- Semantic attributes `code.namespace` and `code.function` captured on JAX-RS internal spans
  ([#2805](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2805))
- Context propagated to reactor-netty callbacks
  ([#2850](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2850))

### 🛠️ Bug fixes

- gRPC context bridging issues
  ([#2564](https://github.com/open-telemetry/opentelemetry-java-instrumentation/issues/2564),
  [#2959](https://github.com/open-telemetry/opentelemetry-java-instrumentation/issues/2959))
- URL credentials of the form `https://username:password@www.example.com/` no longer captured
  ([#2707](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2707))
- Spring MVC instrumentation can cause Spring MVC to misroute requests under some conditions
  ([#2815](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2815))
- RxJava2 NoSuchFieldError
  ([#2836](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2836))
- Duplicate http client tracing headers
  ([#2842](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2842))
- Netty 4.1 listeners could not be removed by application
  ([#2851](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2851))
- NPE caused in gRPC ProtoReflectionService
  ([#2876](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2876))
- Context leak when using Ratpack
  ([#2910](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2910))
- Context leak when using Jetty
  ([#2920](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2920))
- Servlet instrumentation overwrites setStatus that was set manually earlier
  ([#2929](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2929))
- Spans not captured on interface default methods annotated with JAX-RS annotations
  ([#2930](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2930))

### 🧰 Tooling

- Documented how to write InstrumentationModule line by line
  ([#2793](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2793))
- New instrumenter API used in JMS instrumentation
  ([#2803](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2803))
- Instrumenter API improvements
  ([#2860](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2860))
- Muzzle checks whether used fields are actually declared somewhere
  ([#2870](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2870))
- Extracted javaagent-extension-api from tooling & spi
  ([#2879](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2879))
  - You no longer have to depend on the `javaagent-tooling` module to implement custom
    instrumentations: a new `javaagent-extension-api` module was introduced, containing all the
    necessary instrumentation classes and interfaces;
  - `InstrumentationModule` and `TypeInstrumentation` were moved to
    the `io.opentelemetry.javaagent.extension.instrumentation` package;
  - `AgentElementMatchers`, `ClassLoaderMatcher` and `NameMatchers` were moved to
    the `io.opentelemetry.javaagent.extension.matcher` package;
  - A new SPI `AgentExtension` was introduced: it replaces `ByteBuddyAgentCustomizer`;
  - `InstrumentationModule#getOrder()` was renamed to `order()`;
  - `InstrumentationModule#additionalHelperClassNames()` has been removed;
    use `isHelperClass(String)` instead if you use the muzzle compile plugin. If you're not using
    muzzle, you can override `getMuzzleHelperClassNames()` directly instead;
  - `InstrumentationModule#getAllHelperClassNames()` has been removed; you can
    call `getMuzzleHelperClassNames()` to retrieve all helper class names instead.

## Version 1.1.0 (2021-04-14)

### ☢️ Behavioral changes

- Update servlet attribute names for log injection, from `traceId` and `spanId` to `trace_id` and
  `span_id`
  ([#2593](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2593))
- Renamed `runtime.jvm.gc.collection` metric to `runtime.jvm.gc.time`
  ([#2616](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2616))

### 🌟 New javaagent instrumentation

- Elasticsearch 7
  ([#2514](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2514),
  [#2528](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2528))
- Couchbase 3.1
  ([#2524](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2524))
- Grails
  ([#2512](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2512))
- RocketMQ
  ([#2263](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2263))
- Lettuce 6
  ([#2589](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2589))
- Servlet 5
  ([#2609](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2609))
- Vaadin web framework
  ([#2619](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2619))
- GWT
  ([#2652](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2652))
- Tapestry web framework
  ([#2690](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2690))
- `@WithSpan` support for methods returning CompletableFuture
  ([#2530](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2530))
- `@WithSpan` support for methods returning async RxJava 2 types
  ([#2530](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2530))

### 🌟 New library instrumentation

- Library instrumentation for AWS SDK v1
  ([#2525](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2525))
- Library instrumentation for Lettuce 5.1
  ([#2533](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2533))
- RocketMQ
  ([#2263](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2263))
- Lettuce 6
  ([#2589](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2589))
- Spring Boot Autoconfigure support for `@WithSpan` methods returning CompletableFuture
  ([#2618](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2618))
- Spring Boot Autoconfigure support for `@WithSpan` methods returning async RxJava 2 types
  ([#2530](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2530))

### 📈 Improvements

- Move attributes to span builder for use by samplers
  ([#2587](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2587))
- Apache Camel - SNS propagation
  ([#2562](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2562))
- Apache Camel - S3 to SQS propagation
  ([#2583](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2583))
- Added `runtime.jvm.gc.count` metric
  ([#2616](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2616))
- Support reactor netty `HttpClient.from` construction
  ([#2650](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2650))
- Improve akka instrumentation
  ([#2737](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2737))
- Record internal metric for SQL cache misses
  ([#2747](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2747))
- End Netty 4.1 client and server spans when the response has completed, instead of when the
  response has started
  ([#2641](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2641))

### 🛠️ Bug fixes

- Fix RestTemplateInterceptor so that it calls endExceptionally() on exception
  ([#2516](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2516))
- Fix app failure under Eclipse OSGi
  ([#2521](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2521))
- Fix undertow span ending too early
  ([#2560](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2560))
- Fix context leak in AWS SDK 2.2 and RocketMQ instrumentations
  ([#2637](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2637))
- Fix hang when a webflux http request is made inside of another webflux http request
  (e.g. auth filter)
  ([#2646](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2646))
- Fix `@WithSpan` instrumentation breaking Java 6 classes
  ([#2699](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2699))
- Fix context not propagated over JMS when explicit destination used
  ([#2702](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2702))
- Fix StackOverflowError if jdbc driver implementation of Connection getMetaData calls Statement
  execute
  ([#2756](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2756))

### 🧰 Tooling

- Make muzzle reference creation package(s) configurable
  ([#2615](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2615))
- Instrumentations now can skip defining context store manually
  ([#2775](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2775))
- New Instrumenter API
  ([#2596](https://github.com/open-telemetry/opentelemetry-java-instrumentation/pull/2596))
