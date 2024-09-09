# Notes on the Preface

## Why Did We Write This Book?

This book is an updated edition of our *Optimizing Java* title, which was released in 2018. The world has changed markedly since then—​in many ways. For Java programmers, the cloud has become ever-more important, and it is now probably more likely than not that Java applications are deployed in the cloud.

Cloud native deployment fundamentally changes a number of aspects of *performance engineering*, so it seemed appropriate to produce a new edition of the book that reorientates the material toward this new reality.

## Why Should You Read This Book?

Java developers have, in many cases, not necessarily had a lot to do with the deployment and management of their applications in production. With the increasing tide of cloud adoption, this has led to a possible knowledge gap, which this book aims to fix.

Alternatively, DevOps professionals may not have had much exposure to Java/JVM technologies, but are now finding themselves needing to manage Java applications, or pieces of infrastructure that are implemented in it (e.g., Cassandra, Infinispan, Kafka, etc.). Java processes are fundamentally different from those implemented in Go, Python, Node.js, etc. To get the best out of them, you need some level of understanding of those differences and how to work with them.

Whichever tradition you have come from, the end goal is the same—​to enable you to have confidence in managing your cloud-based production applications and be able to diagnose issues with them as they arise.

## Who This Book Is For

Java performance optimization is of interest to several different groups of professionals, not just developers. As such, it is important that we provide on-ramps for people who may be coming from different backgrounds and approaching the subject with a different grounding.

The sorts of jobs that our readers might do include:

* Developers
* Application support and operations staff
* DevOps engineers
* Architects

Each of these groups is likely to have a different focus and take on the material, but they all share a common interest in looking after production business applications in the cloud. They will need to understand the performance behavior of both a single-JVM application and a cloud-deployed, distributed system. In this book we will consider cloud deployments to be public cloud, private cloud, and also a mixture of the two.

An awareness of performance methodology and the relevant aspects of statistics is also important, so that observability and other performance data can be accurately analyzed once it has been collected.

It is also to be expected that the majority of people who read this book will have a need, or at least an interest, in some of the internals of the systems they support. This understanding is often very important when diagnosing certain types of performance problems, as well as being attractive to the intellectually curious engineer.

## What You Will Learn

The material in this book covers a wide variety of topics. This is because this field extends beyond the boundaries of software development and overlaps into a variety of other fields.

## What This Book Is Not

You will not find virtually any discussion of the vendor-specific technologies present on the cloud hyperscalers (AWS, Azure, GCP, OpenShift, and so on) in this book.

This is for two main reasons:

* It would expand the scope of the book and make it unmanageably long.
* It is impossible to stay current with such a large topic area.

The progress made by teams working on those products would make any detailed information about them out of date by the time the book is published. So, instead, in the cloud chapters, we focus on fundamentals and patterns, which remain effective regardless of which cloud your applications are deployed upon.

# Notes on the Table of Contents

The book "Cloud Native Java, 2nd Edition" begins with a Foreword and Preface, setting the stage by explaining the motivation behind the book, its intended audience, and what readers can expect to learn. The first chapter delves into the fundamentals of optimization and performance, defining key concepts such as throughput, latency, and scalability, and emphasizing the importance of performance as an experimental science. The second chapter outlines a comprehensive performance testing methodology, detailing various types of performance tests and best practices, while also addressing common performance antipatterns and cognitive biases.

The third chapter provides an overview of the Java Virtual Machine (JVM), covering its architecture, memory management, threading, and monitoring tools. The fourth and fifth chapters focus on garbage collection, explaining basic concepts and advanced techniques, including various garbage collectors like G1, Shenandoah, and ZGC. Chapter six explores code execution on the JVM, discussing bytecode interpretation, JIT compilation, and evolving execution methods like AOT and GraalVM.

Chapter seven examines hardware and operating systems, highlighting modern processor features, memory management, and the interaction between the JVM and the OS. The eighth chapter introduces the components of the cloud stack, including Java standards, Kubernetes, Prometheus, and virtualization techniques. Chapter nine covers deploying Java in the cloud, discussing container orchestration, deployment techniques, and Java-specific concerns.

Chapter ten introduces observability, explaining its importance and the three pillars: metrics, logs, and traces. The eleventh chapter focuses on implementing observability in Java, introducing tools like Micrometer, Prometheus, and OpenTelemetry. Chapter twelve delves into profiling, covering various tools and techniques for performance analysis. Chapter thirteen discusses concurrent performance techniques, including parallelism, concurrency libraries, and virtual threads.

Chapter fourteen addresses distributed systems techniques and patterns, covering basic data structures, consensus protocols, and distributed systems examples like Cassandra and Kafka. The final chapter, fifteen, looks at modern performance and future trends, discussing new concurrency patterns, Project Panama, Leyden, and Valhalla. The book concludes with appendices on microbenchmarking and a catalogue of performance antipatterns.

# Key Takeaways from the Table of Contents

- **Optimization and Performance Fundamentals**: Understanding key performance metrics such as throughput, latency, and scalability is crucial for optimizing Java applications, especially in cloud environments.
- **Performance Testing Methodology**: A structured approach to performance testing, including various test types and best practices, helps identify and mitigate performance issues effectively.
- **Java Virtual Machine (JVM) Insights**: A deep dive into the JVM's architecture, memory management, and threading provides the foundational knowledge needed to optimize Java applications.
- **Garbage Collection Techniques**: Both basic and advanced garbage collection methods are essential for managing memory efficiently and ensuring application performance.
- **Code Execution and Compilation**: Understanding bytecode interpretation, JIT compilation, and evolving execution methods like AOT and GraalVM can significantly impact application performance.
- **Cloud Deployment and Observability**: Effective deployment strategies and robust observability practices, including metrics, logs, and traces, are vital for maintaining and troubleshooting cloud-native Java applications.
- **Concurrent and Distributed Systems**: Mastering concurrency techniques and distributed systems patterns is key to building scalable and resilient Java applications in a cloud-native environment.