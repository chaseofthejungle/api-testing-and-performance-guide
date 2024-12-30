# API Testing Overview Guide

**Definition/Overview:** An Application Programming Interface (API) enables communications between multiple apps/networks by utilizing a stack of integrated technologies over sessions or connections. The role of the API can be visualized as being similar to a connector: it 'plugs' a network as a data source/provider to another network that requests data on another 'side' (as a client).

**Who needs API?:** Web and streaming (e.g., videos, music) services are heavily dependent upon API systems to serve their consumers. In many cases, a consumer on the 'front end' (the part of a system that the user directly sees and interacts with) utilizes an interface (such as a web page) to request data from the 'back end' (the data part of the system that the user does not directly interact with, such as SQL and NoSQL databases) and its services. The API performs like a messenger that listens to the user's requests (such as desiring for a movie to appear on their television screen), informs the server network's technology of what it needs to do to satisfy the request, and then serves back the data response that the client requested (in this example, the movie).

**API Performance Assurance:** Several common ways to improve API performance (increasing app efficiency and scalability, and promoting optimal user experience) include…

* Caching Efficaciously
* Implementing Throttling and Rate Limiting
* Keeping Sizes of Payloads Minimal
* Optimizing API Endpoints  
* Optimizing Database Queries
* Processing Asynchronously

* Utilizing Load Balancing
  
**Why concern ourselves with API Testing?:**
* API validation needs to be performed before modifications are committed to production environments.
  + Errors and bottlenecks should be identified and eliminated prior to client usage.
* The web, and the Internet at large, relies upon millions of APIs.
  + The average Web user utilizes API systems every single day, whether knowingly or unknowingly.
  + Users expect systems to work. This is true whether a system is being used for entertainment purposes, such as music streaming, or by essential services like hospitals.

**What might API testing cover?:**
* Key validation, such as minimum and maximum length ranges (this can help prevent session crashes and buffer overflows).
* Validation of data formats such as JSON schema and XML.
* Verification of keys, key mechanisms, and proper protocol usage.
* Assurance that API error codes are appropriately recognized and errors are handled properly and efficiently.
  
**REST API Overview:** Representational State Transfer (REST) API are common in web environments, including social media sites such as LinkedIn and X. API that are assembled from REST have six essential features: statelessness, cachability, client-server data transfer, consistent interfacing, code provided on demand, and system layering.

* Statelessness assures that both the server and client networks don't need to concern themselves with the states of requests and responses.
* Caches allow frequent responses to be stored for quick retrieval, making routine requests quicker to process (optimal time efficiency).
* The division of networks into client and server constructs allows for issues to be focused on and resolved by the appropriate organization/people.
* Consistency in interfacing involves both the client and server agreeing to protocols and data formatting that can be readily 'understood' and transferred by both systems, using self-documenting messages in the process of data transfer.
* Code/logic being available to the server on an on-demand basis assists with the ability to transfer data with time and cost (storage) efficiency.
* System layering allows for intermediary systems to exist between the client and server without there necessarily being a bottleneck in service.

**SOAP API Overview:** Simple Object Access Protocol (SOAP) API utilize messaging and allow for Operating System compatability and integrations with the web's Hypertext Transfer Protocol (HTTP) and Extensible Markup Language (XML). SOAP is a popular technology for e-mail systems but it does not compare with REST's diverse feature set and, in comparison and on average, ease of use and reliability for both clients and servers.

**The Role of HTTP:** HTTP functions within the appication layer of the 7-layer OSI model that maps the sending and receiving of data over networks. More specifically, HTTP is directly applicable to the 'IP' protocols contained within the suite of 'TCP/IP' protocols that govern Internet connections. HTTP satisfies requests that are sent from client computers, or hosts, which receive responses back from the relevant servers that handle the requests. Common examples of HTTP-handled data include HTML web pages and files that are downloaded from the Internet. Since HTTP is a stateless protocol, current requests are 'unaware' of previous requests.

TODO: Add information on how testing works (using Postman software as a tool) and HTTP methods.
