---
title: System Design Introduction
categories: ["System Design"]
tags: [Design, microservices, Devops]
math: true
---

# System Design

A structured process of defining the architecture, components, modules, interfaces, and data for a system.
- helps create scalable, efficient and maintainable systems

# High level Design vs Low level Design

- High level Design: It gives an abstract overview of major components, data flow and how they interact with each other
- Low level Design: It gives a much Detailed view of with system like classes, database schema, Interfaces etc


# key questions to remember while designing a system
- **scalability** : What is the expected user count and can the system handle growth ?
- **Availability** : what is the uptime of the system ?
- **Reliability** : Is the design reliable or are there any single point of failures ?
- **Maintainability** : Is it easy to maintain, modify or extend without redesigning ?
- **Performance** : can it work well under load ?
- **Security** : is the system secure ?
- **Cost** : is the system cost efficient?


# Fundamental components

## Load balancers
- These are servers that distribute the incoming traffic across various nodes, they also server as a reverse proxy
- They generally tend to be the single point of failures in systems


## Databases
- Various types of data is stored in various kinds of databases, based on ho w the database is qured databases can be devied into sql and nosql databases
- Based on what kind of data is stored, The databases can be devided as
  - Relational Database ( Mysql )
  - Full text search ( Elastic Search )
  - Graph ( neo4j )
  - Document ( mongoDB )
  - cache ( Redis )

## caching
It is one of the most important and widely used method to reduce load on the upstream servers by caching the result in the memory, if a particular data is found in cache it's called cache hit, if it's not found it is called cache miss, in case of cache miss the cache server fetches the data from the upstream

Types of cache include
- browser cache: The web browser caches static content for faster rendering 
- Application cache: stores responses from API's or computationally expensive calculations
- Database cache: stores frequently accessed DB queries
- CDN ( content delivery network ): distributed network of cache servers located around the world that serve users with their nearest node.
## Message Queues
- A message queue is a communication system used in distributed systems to enable asynchronous message passing between services or components.
- Instead of sending a request and waiting for a response (synchronous), a producer sends a message to a queue, and the consumer processes it later, decoupling the sender and receiver.
