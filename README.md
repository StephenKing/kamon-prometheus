# Prometheus Integration <img align="right" src="https://rawgit.com/kamon-io/Kamon/master/kamon-logo.svg" height="150px" style="padding-left: 20px"/>
[![Build Status](https://travis-ci.org/kamon-io/kamon-prometheus.svg?branch=master)](https://travis-ci.org/kamon-io/kamon-prometheus)
[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/kamon-io/Kamon?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/io.kamon/kamon-prometheus_2.11/badge.svg)](https://maven-badges.herokuapp.com/maven-central/io.kamon/kamon-prometheus_2.11)

### Getting Started

Kamon Prometheus is currently available for Scala 2.10, 2.11 and 2.12.

Supported releases and dependencies are shown below.

| kamon      | status | jdk  | scala
|:----------:|:------:|:----:|------------------
|  1.0.0 |  stable   | 1.8+ | 2.10, 2.11, 2.12


#### Adding the Reporter to your project

First, add the dependency to your build. For SBT that would look like this:

```scala
libraryDependencies += "io.kamon" %% "kamon-prometheus" % "1.0.0"
```

and for Maven:

```xml
<dependency>
    <groupId>io.kamon</groupId>
    <artifactId>kamon-prometheus_2.12</artifactId>
    <version>1.0.0/version>
</dependency>
```

Then, start the reporter when your application starts:

```scala
import kamon.prometheus.PrometheusReporter
Kamon.addReporter(new PrometheusReporter())

```

That's it! You can now go to [http://localhost:9095] and see the metrics. Check the [reference.conf][1] file for more
details on what settings can be configured for the module.



[1]: https://github.com/kamon-io/kamon-prometheus/blob/master/src/main/resources/reference.conf
