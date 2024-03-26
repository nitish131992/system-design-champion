# System-Design-Champion
Since you are here you have already taken a step to learn and grow. Welcome to this course and I hope thins helps you 
in whatever you are up to learning new thing, preparing for interview .
In case you finds any wrong or misleading content please feel free to drop me an email on nitishlvashisth@gmail.com and 
I will be more than happy to correct it.

[What is System Design ?](#what-is-system-design-)

- **Operating System Concepts**
  
   - [CPU and Memory](#cpu-and-memory)
   - Race Condition
   - [Cahche](#cahcing)

- **Networking Concepts**
  
  - [IP](#url)
  - [OSI Model](#url)
  - [TCP and UDP](#url)
  - [Domain Name System (DNS)](#url)
  - [DNS](#dns)
  - [HTTP vs HTTPS](#http-vs-https)
 
- **Software Architecture Pattern**
  - Microservices
  - Monolithic
  - Event Driven
  - Client Server
  - Layered Pattern
  - Microkernel
      
- **Software System Performance Metrics**
  
  - Latency and Network Bandwidth
  - Availablity
  - Reliability
  - Consistency
  - Scalability
      - [Horizontal and Vertical Scaling](#horizontal-and-vertical-scaling)
  - Fault Tolerance

- **Database Concepts**
  - Database
  - DBMS
  - DB Design
  - Typical Data Storage
  - SQL
  - NoSQL
  - ACID vs BASE
  - [CAP Theorem](#cap-theorem)
  - PACELC Theorem
  - SQL vs NoSQL
     
- **Advance Concepts**
  - [Hard Drive / Network Bandwidth](#hard-drive--network-bandwidth)
  - Proxy
  - [Load Balancer](#load-balancer)
  - API Gateway
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

- **System Design Questions**
  - Design BookMyShow
  - Design TinyUrl
  - Design MakeMyTrip
  - Design System like Uber
  - Ecommerce System (Amazon)
  - Messanger App like Whatsapp / Facebook
  - Notification System Design
    
    
# What is System Design ?
System design is the process of defining the architecture, interfaces, and data for a system that satisfies specific requirements. System design meets the needs of your business or organization through coherent and efficient systems. Once your business or organization determines its requirements, you can begin to build them into a physical system design that addresses the needs of your customers. The way you design your system will depend on whether you want to go for custom development, commercial solutions, or a combination of the two.

System design requires a systematic approach to building and engineering systems. A good system design requires you to think about everything in an infrastructure, from the hardware and software, all the way down to the data and how it’s stored.

## Operating System Concepts

  #### CPU and Memory
  
  #### Race Condition
  
  #### Cache

## Networking Concepts

  #### IP
  #### OSI
  #### OSI Model
  #### TCP and UDP
  #### Doma Name System
  #### HTTP vs HTTPS

## Software Architecture Pattern

  #### Microservices
  #### Monolithic
  #### Event Driven
  #### Client Server
  #### Layered Pattern
  #### Microkernel

## Software System Performance Metrics
  
  #### Latency and Network Bandwidth
  #### Availablity
  #### Reliability
  #### Consistency
  #### Scalability
    * Horizontal and Vertical Scaling
  #### Fault Tolerance

## Database Concepts
  #### Database
  #### DBMS
  #### DB Design
    •	Type of Data – Structure vs Unstructured
    •	Query Pattern
    •	Scale

  #### Typical Data storage
    * Cache
    * File Storage 
      ex - Amazon S3
    * CDN 
    * For Search
      Apache Solr , Elastic Search
      Fuzzy Search
      Here data could be lost, no guarantee. So, primary source should be DB
    * Time Series 
      Prometheus
    * Analytics
      Datawarehouse -> offline reporting , ex Hadoop

  #### SQL
  #### NoSQL
  #### Distributed database
  #### ACID vs BASE
  #### CAP Theorem
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
  #### PACELC Theorem
  #### SQL vs NoSQL
  #### 
  

# Horizontal and vertical scaling
Adding more resource in same node is vertical scaling
Adding new node is horizontal scaling

# Hard Drive / Network Bandwidth

# Proxy


# Load Balancer
* Consistent Hashing
* Round Robin
* Weighted Round Robin
* Least Connection

# API Gateway

# Reverse proxy vs API gateway vs Load balancer

Reverse proxy vs. API gateway vs. load balancer

As modern websites and applications are like busy beehives, we use a variety of tools to manage the buzz. Here we'll explore three superheroes: Reverse Proxy, API Gateway, and Load Balancer.

🔹Reverse Proxy: change identity
- Fetching data secretly, keeping servers hidden.
- Perfect for shielding sensitive websites from cyber-attacks and prying eyes.

🔹API Gateway: postman
- Delivers requests to the right services.
- Ideal for bustling applications with numerous intercommunicating services.

🔹Load Balancer: traffic cop
- Directs traffic evenly across servers, preventing bottlenecks
- Essential for popular websites with heavy traffic and high demand.

In a nutshell, choose a Reverse Proxy for stealth, an API Gateway for organized communications, and a Load Balancer for traffic control. Sometimes, it's wise to have all three - they make a super team that keeps your digital kingdom safe and efficient.

![Proxy-LB-AG](https://github.com/nitish131992/System-Design-Champion/assets/19357644/795f6e97-b1e4-450e-bc93-5a8bc2b7f5f9)


# Encoding vs Encryption vs Tokenization. 

Encoding, encryption, and tokenization are three distinct processes that handle data in different ways for various purposes, including data transmission, security, and compliance. 
In system designs, we need to select the right approach for handling sensitive information. 
 
🔹 Encoding 
Encoding converts data into a different format using a scheme that can be easily reversed. Examples include Base64 encoding, which encodes binary data into ASCII characters, making it easier to transmit data over media that are designed to deal with textual data. 
 
Encoding is not meant for securing data. The encoded data can be easily decoded using the same scheme without the need for a key. 
 
🔹 Encryption 
Encryption involves complex algorithms that use keys for transforming data. Encryption can be symmetric (using the same key for encryption and decryption) or asymmetric (using a public key for encryption and a private key for decryption). 
 
Encryption is designed to protect data confidentiality by transforming readable data (plaintext) into an unreadable format (ciphertext) using an algorithm and a secret key. Only those with the correct key can decrypt and access the original data. 
 
🔹 Tokenization 
Tokenization is the process of substituting sensitive data with non-sensitive placeholders called tokens. The mapping between the original data and the token is stored securely in a token vault. These tokens can be used in various systems and processes without exposing the original data, reducing the risk of data breaches. 
Tokenization is often used for protecting credit card information, personal identification numbers, and other sensitive data. Tokenization is highly secure, as the tokens do not contain any part of the original data and thus cannot be reverse-engineered to reveal the original data. It is particularly useful for compliance with regulations like PCI DSS. 

![Eco-Encr-Tokenization](https://github.com/nitish131992/System-Design-Champion/assets/19357644/9d29059e-601c-402d-aebf-6bc861a01fc8)


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

# Security

When you login to a website, your identity needs to be managed. Here is how different solutions work: 

* Authentication vs Autherization
* Session : The server stores your identity and gives the browser a session ID cookie. This allows the server to track login state. But cookies don't work well across devices. 
* Token - Your identity is encoded into a token sent to the browser. The browser sends this token on future requests for authentication. No server session storage is required. But tokens need encryption/decryption. 
* JWT - JSON Web Tokens standardize identity tokens using digital signatures for trust. The signature is contained in the token so no server session is needed. 
* SSO - Single Sign On uses a central authentication service. This allows a single login to work across multiple sites. 
* OAuth2 - Allows limited access to your data on one site by another site, without giving away passwords. 
* QR Code - Encodes a random token into a QR code for mobile login. Scanning the code logs you in without typing a password.

  ![Secutiy_01](https://github.com/nitish131992/System-Design-Champion/assets/19357644/d5cb1892-1eca-46a0-9436-5d8eea6ae914)

  
# Misc Topics
### Zoo Keeper
### Hadoop / Spark / HDFS
### Stream vs Batch Processing
### Authentication vs Authorization
### Firewalls
### Rate Limiters
### A/B Testing
    
# System Design Questions
  ### Design BookMyShow
  ### Design TinyUrl
  ### Design MakeMyTrip
  ### Design System like Uber
  ### Ecommerce System (Amazon)
  ### Messanger App like Whatsapp / Facebook
  ### Notification System Design

# References
- [EduccativeIo](https://www.educative.io/courses/grokking-modern-system-design-interview-for-engineers-managers?utm_campaign=system_design&utm_source=google&utm_medium=ppc&utm_content=search&utm_term=course&eid=5082902844932096&utm_term=system%20design%20interview&utm_campaign=%5BNew%5D+System+Design-Search-+Exc+US+CN+IND&utm_source=adwords&utm_medium=ppc&hsa_acc=5451446008&hsa_cam=18181328148&hsa_grp=142026927753&hsa_ad=618844618310&hsa_src=g&hsa_tgt=aud-470210443676:kwd-297953488694&hsa_kw=system%20design%20interview&hsa_mt=b&hsa_net=adwords&hsa_ver=3&gad_source=1&gclid=Cj0KCQjwwYSwBhDcARIsAOyL0fh2OUmfHQ6GKAm2VIvMxcALMW7JehhwR-1esbyFd97HMC6SH3eJXcYaAuFnEALw_wcB)
    
    
