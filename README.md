# Graphql #

![](https://res.cloudinary.com/codersociety/image/fetch/f_webp,ar_16:9,c_fill,w_1140/https://cdn.codersociety.com/uploads/graphql-reasons.png)

## Abstracts:
---
- This paper is about GraphQL API which is used for mobile and web applications and i have explained what is a GraphQL ,why is it powerful as well as popular.Also,what is the process inside the GraphQL server.Moreover i have included the basic fundamentals in the GraphQL Architecture.Finally concluding which API is best among those other API'S.

---
## Table of Contents :
---

  1. [Introduction](#introduction)

  1. [The Schema Definition Language](#the-schema-definition-language)

  1. [GraphQL Architectures](#graphql-architectures)
      1. [Use cases:](#use-cases)
          - [GraphQL server with a connected database](#1graphql-server-with-a-connected-database)

          - [GraphQL layer that integrates existing systems](#2graphql-layer-that-integrates-existing-systems)

          - [Hybrid approach with connected and integration of existing system](#3hybrid-approach-with-connected-and-integration-of-existing-system)

      1. [Resolver Functions](#resolver-functions)

  1. [Conclusions](#conclusion) 

---
  ## Introduction 
 ---

 - GraphQL is an open source server-side technology which was developed by Facebook to optimize RESTful API calls.
 
 - GraphQL is a query language for API's and runtime for fulfilling these queries with your existing data.
     
- It provides a complete understandable description of the data in your API and gives clients the power to ask for exactly what they need and nothing more.

 ---
 ## The Schema Definition Language       
 ---

 - GraphQL has its own type system that's used to define the schema of an API. The syntax for writing schemas is called Schema Definition Language (SDL).

- Here is an example of how we can use the SDL:

``` Js
type Person {
  name: String!
  age: Int!
  posts: [Post!]!
} 
       The ! type means that this field is required.
```
---
## GraphQL  Architectures
---

- GraphQL is a specification that describes the behavior of a GraphQL server.

- The request made by a client to the GraphQL server is called a Query.

- It is also neutral to databases, so you can use it with relational or NoSQL databases.
---
### Use Cases 
---
- In this section, we’ll walk you through 3 different kinds of architectures that include a GraphQL server:

- GraphQL server with a connected database

- GraphQL server that is a thin layer in front of a number of third party or legacy systems and integrates them through a single GraphQL API

- A hybrid approach of a connected database and third party or legacy systems that can all be accessed through the same GraphQL API

      All three architectures represent major use cases of GraphQL and demonstrate the flexibility in terms of the context where it can be used.
---
### 1.GraphQL server with a connected database
---

- This architecture will be the most common for greenfield projects. 

- In the setup, you have a single (web) server that implements the GraphQL specification.

- When a query arrives at the GraphQL server, the server reads the query's payload and fetches the required information from the database. This is called  "Resolving the query".

- GraphQL also doesn't care about the database or the format that is used to store the data. You could use a SQL database like AWS Aurora or a NoSQL database like MongoDB.


 ![Server with connected database](https://i.imgur.com/cRE6oeb.png)

---
 ### 2.GraphQL layer that integrates existing systems
---
- In this diagram, a GraphQL API acts as an interface between the client and the existing systems. 

- Client applications communicate with the GraphQL server which in turn resolves the query.

- One major problem with these legacy systems is that they make it practically impossible to build innovative products that need access to multiple systems.

- The GraphQL server is then responsible for fetching the data from the existing systems and package it up in the GraphQL response format.


![Graphql Layer](https://i.imgur.com/zQggcSX.png)

---
### 3.Hybrid approach with connected and integration of existing system
---

- Finally, we can combine the above two approaches and build a GraphQL server.

- In this architecture, the GraphQL server will resolve any request that is received.

- It will either retrieve data from connected database or from the integrated API's. 

![Hybrid Approach](https://i.imgur.com/73dByTz.png)

---
## Resolver Functions

---
- In the GraphQL server implementation, each of these fields actually corresponds to exactly one function that's called a resolver. 

- The sole purpose of a resolver function is to fetch the data for its field.

- When the server receives a query, it will call all the functions for the fields that are specified in the query's payload.

- It resolves the query and it is able to retrieve the correct data for each field.

![Resolver Functions](https://i.imgur.com/e1gBEP5.png)

---
## Conclusion 
---

- RESTful APIs is a clear and well-structured resource-oriented approach.when the data gets more complex, the routes get longer. Sometimes it is not possible to fetch data with a single request. This is where GraphQL gives us the strength and its powerful query syntax for traversing, retrieving, and modifying data still stands alone. 
 

## References :

1. [Tutorialspoint](https://www.tutorialspoint.com/graphql/index.htm) 

1. [Javatpoint](javatpoint.com/graphql-architecture)