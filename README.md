# API Testing Overview Guide

**Definition/Overview:** An Application Programming Interface (API) enables communications between multiple apps/networks by utilizing a stack of integrated technologies over sessions or connections. The role of the API can be visualized as being similar to a connector: it 'plugs' a network as a data source/provider to another network that requests data on another 'side' (as a client).

#### Table of Contents:

1. [Who Uses Dedicated API Systems (and Why)](#dedicated-api)
2. [API Testing](#api-testing)
3. [REST and SOAP API](#rest-and-soap)
4. [Hypertext Transfer Protocol (HTTP)](#http)
5. [HTTP Methods](#methods)
6. [API vs. SDK](#apisdk)
7. [Supplemental Resources](#supplemental)
  
<hr />

## 1. <a name="dedicated-api">Who Uses Dedicated API Systems (and Why)</a>
  
**Who needs API?:** Web and streaming (e.g., videos, music) services are heavily dependent upon API systems to serve their consumers. In many cases, a consumer on the 'front end' (the part of a system that the user directly sees and interacts with) utilizes an interface (such as a web page) to request data from the 'back end' (the data part of the system that the user does not directly interact with, such as SQL and NoSQL databases) and its services. The API performs like a messenger that listens to the user's requests (such as desiring for a movie to appear on their television screen), informs the server network's technology of what it needs to do to satisfy the request, and then serves back the data response that the client requested (in this example, the movie).

**API Performance Assurance:** There are several common ways to improve API performance (increasing app efficiency/scalability and promoting optimal user experience).
  
* **Applying Throttling and Rate Limiting**
  + Throttling helps assure scalability when traffic increases.
  + Rate limiting manages the quantity of client requests that can be handled within a specified time window.
    - This prevents hacking attempts and promotes fair API usage.
* **Caching Efficaciously**
  + Common/popular requests can be resolved without impacting the database directly.
    - This can significantly improve request response times and API workload, as well.
  + Cache expiration and invalidation prevent unnecessary data persistance, keeping cache data appropriately limited and organized.
  + *Caching Examples:* [Memcached](https://memcached.org/), [Redis](https://redis.io/)
* **Keeping Sizes of Payloads Minimal**
  + *Example Solutions:* JSON compression, large data pagination, efficient data format choices (e.g., MessagePack, Protocol Buffers), eliminating unneeded fields from API responses.
* **Move Resource-Extensive Processes to the Background**
  + Promotes quick API responsiveness and asynchronous processing, while handling the more burdensome operations individually.
    - Can be done via message queues, such as Apache Kafka and RabbitMQ.
* **Optimizing API Endpoints**
  + *Example Solutions:* Follow RESTful standards, avoid establishing multiple enpoints by combining related operations and/or utilizing query parameters for filtered results.
* **Optimizing Database Queries to Reduce Bottlenecks**
  + *Example Solutions:* Indexing, JOIN operations/statements, not using 'SELECT *', database normalization/denormalization (based on need), query profiling/identifying.
* **Utilizing Load Balancers**
  + This distributes ingress API requests (and traffic spikes) across servers in a manner that prevents bottlenecking, provides fault tolerance, and mitigates or eliminates redundancy.
  
<hr />
  
## 2. <a name="api-testing">API Testing</a>
  
**Why concern ourselves with API Testing?:**
* API validation needs to be performed *before* modifications are committed to production environments.
  + Errors and bottlenecks should be identified and eliminated prior to client usage.
* The web, and the Internet at large, relies upon *millions* of APIs.
  + The average Web user utilizes API systems every single day, whether knowingly or unknowingly.
  + Users expect systems to work.
    - This is true whether a system is being used for entertainment purposes, such as music streaming, or by essential services like hospitals.

**What might API testing cover?:**
* **Key validation**, such as minimum and maximum length ranges (this can help prevent session crashes and buffer overflows).
* **Validation of data formats** such as JSON schema and XML.
* **Verification** of keys, key mechanisms, and proper protocol usage.
* Assurance that API error codes are appropriately recognized and **errors are handled properly and efficiently**.
    
**(TODO: Provide example of API Testing using Postman.)**

<hr />
  
## 3. <a name="rest-and-soap">REST and SOAP API</a>
  
**REST API Overview:** Representational State Transfer (REST) API are common in web environments, including social media sites such as LinkedIn and X. API that are assembled from REST have six essential features: statelessness, cachability, client-server data transfer, consistent interfacing, code provided on demand, and system layering.
  
* **Statelessness** assures that server and client networks don't need to concern themselves with the states of requests and responses.
* **Caches** allow frequent responses to be stored for quick retrieval, making routine requests quicker to process (for optimal time efficiency).
* The division of networks into **client and server constructs** allows for issues to be focused on and resolved by the appropriate organization/people.
* **Consistency in interfacing** involves both the client and server agreeing to protocols and data formats that are readily 'understood' and transferred by both systems.
  + *Self-documenting messages* are utilized during data transfer.
* **On-demand code/logic availability** for the server assists with data transfer (for optimal time and cost/storage efficiency).
* **System layering** allows for intermediary systems to exist between clients and servers while reducing/eliminating service bottlenecks.
  
**SOAP API Overview:** Simple Object Access Protocol (SOAP) API utilize messaging and allow for Operating System compatability and integrations with the web's Hypertext Transfer Protocol (HTTP) and Extensible Markup Language (XML). SOAP is a popular technology for e-mail systems but it does not compare with REST's diverse feature set and, in comparison and on average, ease of use and reliability for both clients and servers.
  
<hr />
  
## 4. <a name="http">Hypertext Transfer Protocol (HTTP)</a>
  
**The Data Servicing Role of HTTP:** HTTP functions within the appication layer of the 7-layer OSI model that maps the sending and receiving of data over networks. More specifically, HTTP is directly applicable to the 'IP' protocols contained within the suite of 'TCP/IP' protocols that govern Internet connections. HTTP satisfies requests that are sent from client computers, or hosts, which receive responses back from the relevant servers that handle the requests. Common examples of HTTP-handled data include HTML web pages and files that are downloaded from the Internet. Since HTTP is a stateless protocol, current requests are 'unaware' of previous requests.
  
<hr />

## 5. <a name="methods">HTTP Methods</a>

(TODO)

<hr />

## 6. <a name="apisdk">API vs. SDK</a>
  
While APIs and Software Developer Kits (SDKs) are both valuable tools for software developers, it is important that the terms not be used interchangeably.

| &nbsp; | API | SDK |
| :-----: | :-----: | :-----: |
| **Primary Purpose** | Defines/Enables Software Communications for Data Exchange | Provides Tools for Building Software from Scratch |
| **Paradigm** | Sends/Receives Data through Request/Response Calls | Complete and Installed Package/Suite for Writing/Testing/Running Apps |
| **Accessibility** | Provides Users Access to Specified Functionalities | Can Integrate with APIs for Data Access Purposes |
| **Focus** | User Interaction/Data Communications | Creating/Developing Apps |
| **Portability** | Compatible Across Platforms | Often Platform-Dependent |
  
<hr />

## 7. <a name="supplemental">Supplemental Resources</a>
  
* *[Amazon API Gateway](https://aws.amazon.com/api-gateway/)*
* *[Azure API Gateway](https://azure.microsoft.com/en-us/products/api-management)*  
* *[Google Cloud API Gateway](https://cloud.google.com/api-gateway/docs)*
