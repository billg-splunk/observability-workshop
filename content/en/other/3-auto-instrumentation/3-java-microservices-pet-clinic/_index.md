---
title: Workshop using the Java microservices Pet Clinic demo (Kubernetes based).
linkTitle: Java Microservices Workshop
weight: 99
description: Learn how to enable Open Telemetry (Auto) Instrumentation for your Java-based application running in Kubernetes. Experience real-time monitoring and troubleshooting to help you maximize application behavior with end-to-end visibility.
hidden: true
---

The goal of this workshop is to introduce the features of Splunk's Opentelemetry Java Auto instrumentation. 
First we walk through the basic steps to enable auto-instrumentation for an existing Java application running in Kubernetes so it will start sending Opentelemetry signals to **Splunk Observability Cloud** platform and enable the following components:

* Splunk Infrastructure Monitoring (IM)
* Splunk Auto Instrumentation for Java (APM)
  * Database Query Performance
  * AlwaysOn Profiling
* Splunk Real User Monitoring (RUM)
* RUM to APM Correlation
* Splunk Log Observer (LO)

We will show the steps about how to clone (download) a sample microservices Java application (Spring PetClinic), as well as how to compile, package and deploy/run the application.

Once the application is up and running, and auto instrumentation is enabled we will instantly start seeing metrics and traces via the **Auto Instrumentation** for Java that will be used by the **Splunk APM** product.

We also will examine Alwayson Profiling and Database Query performance.

After that, we will instrument PetClinic's end user interface (HTML pages rendered by the application) with the **Splunk OpenTelemetry Javascript Libraries (RUM)** that will generate RUM traces around all the individual clicks and page loads executed by an end user.

Lastly, we will configure the Spring PetClinic application to write application logs to the filesystem and also configure the Splunk OpenTelemetry Collector to read (tail) the logs and send them to **Splunk Cloud**.

{{% notice title="Prerequisites" style="primary" icon="info" %}}

* Outbound SSH access to port `2222`.
* Outbound HTTP access to port `81`.
* Familiarity with the `bash` shell and `vi/vim/nano` editor.

{{% /notice %}}
![Splunk Otel Architecture](images/auto-instrumentation-java-diagram.png)

---
Based on the [example](https://github.com/signalfx/splunk-otel-collector-chart/blob/main/examples/enable-operator-and-auto-instrumentation/spring-petclinic-java.md) **Josh Voravong** has created.