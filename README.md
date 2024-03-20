# System-Design-Champion
Since you are here you have already taken a step to learn and grow. Welcome to this course and I hope thins helps you 
in whatever you are up to learning new thing, preparing for interview .
In case you finds any wrong or misleading content please feel free to drop me an email on nitishlvashisth@gmail.com and 
I will be more than happy to correct it.

[What is System Design ?](#what-is-system-design-)

- **Networking Concepts**
  
  - [IP](#url)
  - [OSI Model](#url)
  - [TCP and UDP](#url)
  - [Domain Name System (DNS)](#url)
  - [DNS](#dns)
  - [HTTP vs HTTPS](#http-vs-https)
 
- **Operating System Concepts**
  
   - [CPU and Memory](#cpu-and-memory)
   - Race Condition
   - [Cahche](#cahcing)
  
- **Software System Performance Metrics**
  
  - Latency and Network Bandwidth
  - Availablity
  - Reliability
  - Consistency
  - Scalability
  - Fault Tolerant

- ** Database Concepts **
- [Horizontal and vertical scaling](#horizontal-and-vertical-scaling)

- [CAP Theorem](#cap-theorem)

- ** Software Architecture Pattern **
  - Layered Pattern
  - Event Driven
  - Client Server
  - Microkernel
  - Microservices
  - Monolithic
 
- ** Advance Concepts **
  - [Hard Drive / Network Bandwidth](#hard-drive--network-bandwidth)
  - [Load Balancer](#load-balancer)
  - [Asyncronous Processing Queue](#asyncronous-processing-queue)
  - [Cloud](#cloud)
  - [Deployment](#deployment)
  - [CDN and Edges](#cdn-and-edges)
  - [Cahcing](#cahcing)
  - [Misc Topics](#misc-topics)
  - [Consistent Hashing](#consistent-hashing)
  - [Database](#database)
  - [Node Replication Startegy](#node-replication-startegy)
  - [Search](#search)
    
# What is System Design ?
System design is the process of defining the architecture, interfaces, and data for a system that satisfies specific requirements. System design meets the needs of your business or organization through coherent and efficient systems. Once your business or organization determines its requirements, you can begin to build them into a physical system design that addresses the needs of your customers. The way you design your system will depend on whether you want to go for custom development, commercial solutions, or a combination of the two.

System design requires a systematic approach to building and engineering systems. A good system design requires you to think about everything in an infrastructure, from the hardware and software, all the way down to the data and how it’s stored.

# CPU and Memory
Cental Processing Unit

# Horizontal and vertical scaling
Adding more resource in same node is vertical scaling
Adding new node is horizontal scaling

# Hard Drive / Network Bandwidth

# CAP Theorem

The CAP theorem is a belief from theoretical computer science about distributed data stores that claims, in the event of a network failure on a distributed database, it is possible to provide either consistency or availability—but not both. Either AP or CP

Consistency means that data is the same across the cluster, so you can read or write from/to any node and get the same data.

Availability means the ability to access the cluster even if a node in the cluster goes down.

Partition tolerance means that the cluster continues to function even if there is a "partition" (communication break) between two nodes (both nodes are up but can't communicate).

To get both availability and partition tolerance, you have to give up consistency. Consider if you have two nodes, X and Y, in a master-master setup. Now, there is a break between network communication between X and Y, so they can't sync updates. At this point you can either:
A) Allow the nodes to get out of sync (giving up consistency), or
B) Consider the cluster to be "down" (giving up availability)

All the combinations available are:

**CA** - data is consistent between all nodes - as long as all nodes are online - and you can read/write from any node and be sure that the data is the same, but if you ever develop a partition between nodes, the data will be out of sync (and won't re-sync once the partition is resolved).

**CP** - data is consistent between all nodes and maintains partition tolerance (preventing data desync) by becoming unavailable when a node goes down.
partition is resolved, but you aren't guaranteed that all nodes will have the same data (either during or after the partition)

You should note that CA systems don't practically exist (even if some systems claim to be so). So, either CP or AP

**AP** - nodes remain online even if they can't communicate with each other and will resync data once the 

Checkout this video on youtube from ByteByteGo : [CAP Theorem Simplified](https://www.youtube.com/watch?v=BHqjEjzAicA)

# Load Balancer
* Consistent Hashing
* Round Robin
* Weighted Round Robin
* Least Connection

#  Asyncronous Processing Queue
   * Rabbit MQ
   * Kafka
   * Service Bus
   * Pub / Sub
     
# Cloud
   * AWS
   * Azure
   * GCP
   * Blue Ocean

# Deployment
   * Docker
   * Kubentees
   * Virtula Machine / Container

# DNS 

# HTTP vs HTTPS

To provide encryption, HTTPS uses an encryption protocol known as Transport Layer Security, and officially, it is referred to as a Secure Sockets Layer (SSL)
This protocol uses a mechanism known as asymmetric public key infrastructure, and it uses two different keys which are given below:
(1) **Private key**: This key is available on the web server, which is managed by the owner of a website. It decrypts the information which is encrypted by the public key.
(2) **Public key**: This key is available to everyone. It converts the data into an encrypted form.


# CDN and Edges

# Cahcing
[Cache Fundamentals](https://nitishvashisth.hashnode.dev/caching-fundamentals)

# Consistent Hashing

# Database
* SLQ vs NoSql
* ACID vs BASE
* Data Denormalization
* Database partitioning (Shrading)
  * Vertical
  * Key Based
  * Directory Based
* DB indexing
  * Primary
  * Secondry
  * CLustering
* Types of NoSql
    * Key Value
    * Document Based
    * Wide column
    * Graph Based
      
# Node Replication Startegy
* Master - Master
* Master Slave
* Read Heavy vs Write Heavy

# Search
* Solr
* Elastic Search
  
# Misc Topics
### Zoo Keeper
### Hadoop / Spark / HDFS
### Stream vs Batch Processing
### Authentication vs Authorization
### A/B Testing
    



    
    
