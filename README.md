# Course detailes

[Udemy link](https://sisense.udemy.com/course/software-architecture-design-of-modern-large-scale-systems/learn/lecture/27280376#overview)

# Section 1: Introduction

Course workbook: [PDF](Software+Architecture+and+Design+of+Large+Scale+Systems+-+Workbook.pdf)

# Section 2: System Requirements & Architectural Drivers

## 4. Feature Requirements - Step by Step Process

- UML (unified modeling language) 
- Sequence Diagram

## 5. System Quality Attributes Requirements

Consideration of quality attributes:
- Teasting and Measurability
- Trade offs (a balance achieved between two desirable but incompatible features; a compromise)
- Feasibility (the state or degree of being easily or conveniently done)

## 6. System Constraints in Software Architecture

- Technical Constraints
- Business Constraints
- Regulatory/Legal Constrains

# Section 3: Most Important Quality Attributes in Large Scale Systems

## 7. Performance

- Response time (Processing time + Waiting time) - time between sending req and receiving res
- Throughput - amount of work/data processed by our system per unit of time

Important Consideration:
- Proper measuring of response time
- Response time percentile distribution
- Performance degradation

## 8. Scalability

Load/Traffic Patterns

Vertical scalability - adding resources or upgrading existing in SINGLE machine
Horisontal scalability - adding resources or upgrading existing in DIFFERENT machines

Team/Organization scalabillity

## 9. Availability - Introduction & Measurement

Uptime - service is available to the user
Downtime - service is unavailable to the user
MTBF - Mean time between failures
MTTR - Mean time to recovery

Availability = MTBF / (MTBF + MTTR)

99,9% - is standart in the industry (3 'nines'), if 99,99% - 4 'nines'

## 10. Fault Tolerance & High Availability

Falures:
1. Human Errors
2. Software Errors
3. Hardware Falures

Fault Tolerence:
- Failure Prevemtion
- Failure Detection and Isolation
- Recovery

## 11. SLA, SLO, SLI

## 12. Real World SLA Examples from the Industry

Cloud Vendor SLA Examples
AWS Service Level Agreements (SLAs)
Google Cloud Platform Service Level Agreements
Microsoft Azure Service Level Agreement
GitHub Enterprise Service Level Agreement
Atlassian Products Service Level Agreement

# Section 4: API Design

## 13. Introduction to API Design for Software Architects

 API - contract between engeers and applliacation clients

 API:
 - Public APIs
 - Private/Internal APIs
 - Partner APIs

## 14. RPC

RPC - Remote Procedure Call

## 15. Popular RPC Frameworks and Technologies

gRPC
gRPC is a modern open source high performance Remote Procedure Call (RPC) framework. It was originally developed by Google in 2015 as the next generation of its own internal RPC infrastructure.

It uses HTTP/2 as its transport protocol and Protocol Buffers as its Interface Description Language.
gRPC currently supports the following languages:

C#
C++
Dart
Go
Java
Kotlin
Node
Objective-C
PHP
Python
Ruby

Apache Thrift
Thrift is a lightweight, language-independent software stack for point-to-point RPC.

Thrift makes it easy for programs written in different programming languages to share data and call remote procedures since it supports more than 28 languages, including C++, Java, Python, Go, Scala, Swift, PHP, Ruby, Perl, C#, JavaScript, Node.js, and other languages.

Thrift was created at Facebook for "scalable cross-language services development". It uses its own Interface Description Language called Thrift interface description language.

A full tutorial for all the supported languages can be found here.

Java Remote Method Invocation (RMI)
RPC framework that allows one Java virtual machine to invoke methods on an object running in another Java virtual machine.

RMI uses Java as the Interface Description Language.

You can find the full tutorial here.

## 16. REST API

Representational State Transfer (REST): https://ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm
HTTP request methods: https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods

# Section 5: Large Scale Systems Architectural Building Blocks

## 17. DNS, Load Balancing & GSLB

Quality attrubutes of LB:
1. Scalability - Auto-scaling
2. High Availability
3. Performance
4. Maintainability

Loadbalancer types:
1. DNS
2. Hardware load balancing
3. Software load balancing
4. Global Server Load Balancing (GSLB) - provide also DNS with health monitoring.

https://sisense.udemy.com/course/software-architecture-design-of-modern-large-scale-systems/learn/lecture/29603416#overview

Load Balancing Solutions & Cloud Technologies
Open Source Software Load Balancing Solutions
HAProxy
HAProxy is a free and open-source, reliable, high performance TCP/HTTP load balancer.
It is particularly suited for very high traffic web sites, and powers a significant portion of the world's most visited ones. It is considered the de-facto standard open-source load balancer, and is  shipped with most mainstream Linux distributions.
HAProxy supports most Unix style operating systems.

NGINX
NGINX is a free, open-source, high-performance HTTP server and reverse proxy (load balancer). It is known for its high performance, stability, rich feature set and simple configuration.
For a full tutorial on how to install, configure and use NGINX follow this link.

Cloud Based Load Balancing Solutions
AWS - Elastic Load Balancing (ELB)
Amazon ELB is a highly scalable load balancing solution.

It is an ideal solution for running on AWS, and integrates seamlessly with all of AWS services.

It can operate on 4 different modes:

Application (Layer 7) Load Balancer - Ideal for advanced load balancing of HTTP and HTTPS traffic

Network (Layer 4) Load Balancer - Ideal for load balancing of both TCP and UDP traffic

Gateway Load Balancer - Ideal for deploying, scaling, and managing your third-party virtual appliances.

Classic Load Balancer (Layer 4 and 7) - Ideal for routing traffic to EC2 instances.

For the full documentation on Amazon ELB and its autoscaling policies follow this link

GCP - Cloud Load Balancing
Google Cloud Platform Load Balancer is Google's highly scalable and robust load-balancing solution.

"Cloud Load Balancing allows you to put your resources behind a single IP address that is externally accessible or internal to your Virtual Private Cloud (VPC) network".

Some of the load balancer types available as part of the GCP Cloud Load Balancing are:

External HTTP(S) Load Balancer - Externally facing HTTP(s) (Layer 7) load balancer which enables you to run and scale your services behind an internal IP address.

Internal HTTP(S) Load Balancer - Internal Layer 7 load balancer that enables you to run and scale your services behind an internal IP address.

External TCP/UDP Network Load Balancer - Externally facing TCP/UDP (Layer 4) load balancer

Internal TCP/UDP Load Balancer - Internally facing TCP/UDP (Layer 4) load balancer.

Microsoft Azure Load Balancer
Microsoft Azure load balancing solution provides 3 different types of load balancers:

Standard Load Balancer - Public and internal Layer 4 load balancer

Gateway Load Balancer - High performance and high availability load balancer for third-party Network Virtual Appliances.

Basic Load Balancer - Ideal for small-scale application

GSLB Solutions
Amazon Route 53 - Amazon Route 53 is a highly available and scalable cloud Domain Name System (DNS) web service.

AWS Global Accelerator -  A networking service that helps you improve the availability, performance, and security of your public applications.

Google Cloud Platform Load Balancer & Cloud DNS - Reliable, resilient, low-latency DNS serving from Google's worldwide network with everything you need to register, manage, and serve your domains.

Azure Traffic Manager - DNS-based load balancing

## 19. Message Brokers

Benefits:
- Asynchronous architecture
- Buffering

Quality attributes:
- Hight availability
- scalability

## 20. Message Brokers Solutions & Cloud Technologies

Open Source Message Brokers
Apache Kafka - The most popular open-source message broker nowadays. Apache Kafka is a distributed event streaming platform used by thousands of companies for high-performance data pipelines, streaming analytics, data integration, and mission-critical applications.

RabbitMQ - A widely deployed open-source message broker. It is used worldwide at small startups and large enterprises.

Cloud Based Message Brokers
Amazon Simple Queue Service (SQS) - Fully managed message queuing service that enables you to decouple and scale micro-services, distributed systems, and serverless applications.

GCP Pub/Sub and Cloud Tasks - Publisher/Subscriber and message queue solutions offered by Google Cloud Platform. See this article for comparison between the two offerings.

Microsoft Azure:

Service Bus - Fully managed enterprise message broker with message queues and publish-subscribe topics.

Event Hubs - Fully managed real-time data ingestion service. Allows streaming millions of events per second from any source. Integrates seamlessly with Apache Kafka clients without any code changes. A perfect solution for Big Data.

Event Grid - Reliable, serverless event delivery system at a massive scale. It uses the publish-subscribe model. It is Dynamically scalable, Low cost with a pay-as-you-go model, and guarantees "At least once delivery of an event"

## 21. API Gateway

Benefits quality attributes:
- It also calls API composition
- Creates an abstraction between client and the system
- Consoledate Authentification only in one place
- Implement Request routing
- Caching Static content and response cahing
- Monitoring and alerting
- Protocol Translation

Consideration:
 1. API Gateway shouldn't contain any business logic
 2. It may become a Single Point of Failure
 3. Avoid bupassingg API Gateway from external resources

Open Source API Gateways
Netflix Zuul
Zuul is a free and open-source application gateway written in Java that provides capabilities for dynamic routing, monitoring, resiliency, security, and more.

Cloud-Based API Gateways
Amazon API Gateway
Amazon API Gateway is a fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale. Supports RESTful APIs and WebSocket APIs (bi-directional communication between client and server).

Google Cloud Platform API Gateway
Google Cloud Platform API Gateway enables you to provide secure access to your services through a well-defined REST API that is consistent across all of your services, regardless of service implementation. It is designed for serverless workloads on GCP. For full documentation, follow this link.

Apigee is Google Cloud’s API management product that enables organizations to build, manage, and secure APIs — for any use case, environment (on-premises, in Google Cloud, or a hybrid environment), or scale. For full documentation, follow this link.

Microsoft Azure API Management
API Management helps organizations publish APIs to external, partner, and internal developers to unlock the potential of their data and services.

## 23. Content Delivery Network - CDN

- Provide service by caching our website content on their edge servers which are relocated at different Points of Presence (PoP).
- Those edge servers are physically closer to the user and more strategically located in terms network infrastructure

Strategies:
- Pull
- Push

## 24. CDN Solutions & Cloud Technologies

Cloudflare
Cloudflare offers ultra-fast static and dynamic content delivery over our global edge network. It helps reduce bandwidth costs and takes advantage of built-in unmetered DDoS protection.

Fastly
Fastly's Deliver@Edge is a modern, efficient, and highly configurable CDN that gives you the freedom to control how your content is cached so you can deliver the content your users want quickly.

Akamai
Akamai has a large variety of offerings for API Acceleration, Global Traffic Management, Image & Video Management, Media Delivery, and much more.

Amazon CloudFront
Amazon CloudFront is a content delivery network (CDN) service built for high performance, security, and developer convenience. Some of its use-cases include delivering fast secure websites, accelerating dynamic content delivery and APIs, live streaming, video-on-demand, and others.

Google Cloud Platform CDN
GCP CDN offers fast, reliable web and video content delivery with a global scale and reach.

Microsoft Azure Content Delivery Network
Microsoft's CDN solution offers global coverage, full integration with Azure services, and a simple setup.

# Section 6: Data Storage at Global Scale

## 25. Relational Databases & ACID Transactions

When to choose:
    - Perform complex and flexible queries to analyze our data
    - Guarantee ACID transactions between different entities in our database

When not to choose:
    - There isn't any inherent relationship between different records that justifies storing our data in tables
    - Read performance is the most important quality that we need for providing good user expiriance

## 26. Non-Relational Databases

When to choose:
    - Superior when it comes to query speed
    - Perfect choice for caching
    - Handling real-time big data
    - Data is not structured
    - Different records can contain different attributes

Where to use: User Profiles, Content Management

Non-Relational Databases - Solutions

Key/Value Stores Examples
- Redis
- Aerospike
- Amazon DynamoDB

Document Store Examples
- Cassandra
- MongoDB

Graph Databases Examples
- Amazon Neptune
- NEO4J

## 28. Techniques to Improve Performance, Availability & Scalability Of Databases

- Database Indexing
- Database Replication
- Database Partitioning/Sharding

## 29. Brewer’s (CAP) Theorem

Network partition - when one DB Replica cannot reach other Replicas to synch

CAP Theorem - "In the presence of a Network Partion, a distributed database cannot guarantee both Consistancy and Availability and has to choose only one of them."
It's valid for only when there is network patition!!!

C = Consistency
A = Availability
P = Partition Tolerance

We have to drop one of three:

- CA - no Partition Tolerance
- CP - no Availability
- AP - no Consistency

## 30. Scalable Unstructured Data Storage
 - DFS - Distributed File System
 - Object Store (Cloud - Amazon S3, GCP Storage, Azure Blob, Alibaba OSS)

+ Cloud-Based Object Store Solutions
Amazon S3 (Simple Storage Service) - Amazon's highly scalable cloud storage service that stores object data within buckets. Designed to store and protect any amount of data for various use cases, such as websites, cloud-native applications, backups, archiving machine learning, and analytics.
GCP Cloud Storage - Google Cloud's managed service for storing unstructured data for companies of all sizes
Azure Blob Storage -  Microsoft's massively scalable and secure object storage for cloud-native workloads, archives, data lakes, high-performance computing, and machine learning
Alibaba Cloud OSS (Object Storage Service) - Fully managed enterprise-ready Object Storage Service to store and access any amount of data from anywhere.

+ Open Source and Third-Party Object Store Solutions
OpenIO - A software-defined open-source object storage solution ideal for Big Data, HPC, and AI. It is S3 compatible and can be deployed on-premises or cloud-hosted on any hardware that you choose.
MinIO - High-performance, S3-compatible object storage. It is native to Kubernetes and 100% open source under GNU AGPL v3.
Ceph - Open-source, reliable and scalable storage. Ceph provides a unified storage service with object, block, and file interfaces from a single cluster built from commodity hardware components.