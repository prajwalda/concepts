# Investigating NoSQL Databases for Improved Performance and Scalability 🚀

NoSQL databases are purpose-built for specific data models and store data in flexible schemas that scale easily for modern applications. [NoSQL databases](https://aws.amazon.com/nosql/) are widely recognized for their ease of development, functionality, and performance at scale. This page includes resources to help you better understand `NoSQL databases` and to get started.

## Scenario
In our current project, we are experiencing performance and scaling issues. After conducting an initial analysis, our team lead has suggested that we explore the use of NoSQL databases to address these challenges. This `technical paper` investigates five popular [NoSQL databases](https://aws.amazon.com/nosql/), highlighting their features and use cases to determine their suitability for our project.

![Alt Text](https://miro.medium.com/v2/resize:fit:710/1*aft5e_gFeDW4DQ8tayEsrA.png)

## NoSQL Databases

1. **[MongoDB](https://www.techtarget.com/searchdatamanagement/definition/MongoDB) ![MongoDB](https://img.icons8.com/color/48/000000/mongodb.png)**
   - **Type**: Document Store 
   - **Key Features**:
     - Schema flexibility with `JSON-like` documents.
     - High performance with efficient indexing.
     - Horizontal scaling through sharding.
   - **Use Cases**: Content management systems, real-time analytics, IoT applications, and mobile apps.

2. **[Cassandra](https://cassandra.apache.org/_/index.html)  🟥**
   - **Type**: Wide Column Store
   - **Key Features**:
     - High availability with no single point of failure.
     - Linear `scalability` and `fault tolerance`.
     - Optimized for high write throughput.
   - **Use Cases**: Time series data, sensor data, recommendation systems, and product catalogs.

3. **[Redis](https://www.ibm.com/topics/redis) 🟥**
   - **Type**: Key-Value Store
   - **Key Features**:
     - Extremely `low latency` and high throughput with in-memory data storage.
     - Supports various data structures such as strings, hashes, lists, sets, and sorted sets.
   - **Use Cases**: `Caching`, real-time analytics, session storage, leaderboards, and message brokering.

4. **[Couchbase](https://docs.couchbase.com/home/index.html) 🟦**
   - **Type**: Document Store
   - **Key Features**:
         - Memory-first architecture for high performance.
         - Easy and efficient scaling for `large data volumes`.
   - **Use Cases**: Mobile and web applications, real-time analytics, and customer 360 applications.

5. **[Neo4j](https://neo4j.com/docs/getting-started/get-started-with-neo4j/graph-database/) 🟩**
   - **Type**: Graph Database
   - **Key Features**:
     - Excels in handling `complex and connected data` with fast traversal of relationships.
     - Flexible schema supporting various types of relationships and properties.
   - **Use Cases**: Social networks, `recommendation engines`, fraud detection, and network/IT operations.

![Image shows how the database schema looks like](https://redis.io/wp-content/uploads/2022/05/nosql-database-1.svg?&auto=webp&quality=85,75&width=1600)

## Types of NoSQL Databases

1. **[Document-oriented databases](https://www.mongodb.com/resources/basics/databases/nosql-explained) 📄**
   - A document-oriented database stores data in documents similar to `JSON objects`. Each document contains pairs of fields and values. The values can typically be a variety of types, including things like strings, numbers, booleans, arrays, or even other objects. A document database offers a flexible data model, much suited for semi-structured and typically unstructured data sets. They also support nested structures, making it easy to represent complex relationships or `hierarchical data`.

2. **[Key-value databases](https://www.mongodb.com/resources/basics/databases/nosql-explained) 🔑**
   - A key-value store is a simpler type of database where each item contains `keys and values`. Each key is unique and associated with a single value. They are used for caching and session management and provide `high performance` in reads and writes because they tend to store things in memory. Examples are `Amazon DynamoDB` and Redis.

3. **[Wide-column stores](https://www.mongodb.com/resources/basics/databases/nosql-explained) 📊**
   - Wide-column stores store data in tables, rows, and `dynamic columns`. The data is stored in tables. However, unlike traditional SQL databases, wide-column stores are flexible, where different rows can have different sets of columns. These databases can employ column compression techniques to `reduce the storage space` and enhance performance. The wide rows and columns enable efficient retrieval of sparse and wide data. Some examples of wide-column stores are Apache Cassandra and HBase.

4. **[Graph databases](https://www.mongodb.com/resources/basics/databases/nosql-explained) 🔗**
   - A graph database stores data in the form of nodes and edges. `Nodes` typically store information about people, places, and things (like nouns), while edges store information about the relationships between the nodes. They work well for highly connected data, where the relationships or patterns may not be very obvious initially. Examples of graph databases are `Neo4J and Amazon Neptune`.

## Differences between RDBMS and NoSQL databases


| Feature             | NoSQL                                                                                                         | RDBMS                                                                                              |
|---------------------|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Data modeling       | Data models vary based on the type of NoSQL database used — for example, key-value, document, graph, and wide-column. | Uses a tabular data structure with data represented as a set of rows and columns.                  |
| Schema              | Provides a flexible schema where each set of documents/row-column/key-value pairs can contain different types of data. | Has a fixed schema where every row should contain the same predefined column types.                |
| Query language      | Varies based on the type of NoSQL database used. MongoDB has MQL, Neo4J uses Cypher, etc.                      | Uses structured query language (SQL).                                                              |
| Scalability         | Designed for vertical and horizontal scaling.                                                                 | Designed primarily for vertical scaling, with limited capabilities for horizontal scaling.         |
| Data relationships | Relationships can be nested, explicit, or implicit.                                                            | Defined through foreign keys and accessed using joins.                                             |
| Transaction type    | Transactions are either ACID- or BASE-compliant.                                                               | Transactions are ACID-compliant.                                                                   |
| Performance         | Suitable for real-time processing, big data analytics, and distributed environments.                           | Suitable for read-heavy and transaction workloads.                                                 |
| Data consistency    | Offers high data consistency.                                                                                  | Offers eventual consistency, in most cases.                                                        |
| Distributed computing | Supports distributed data storage, vertical and horizontal scaling through sharding, replication, and clustering. | Supports distributed computing through clustering and replication, but less scalable and flexible. |
| Fault tolerance     | Built-in fault tolerance and high availability due to data replication.                                         | Uses replication, backup, and recovery mechanisms, may require additional disaster recovery measures. |
| Data partitioning   | Done through sharding and replication.                                                                         | Supports table-based partitioning and partition pruning.                                           |
| Data to object mapping | Stores data in a variety of ways (JSON documents, wide-column stores, key-value pairs). Provides ODM frameworks. | Relies on data-to-object mapping for integration between database columns and object-oriented code. |


## Conclusion
Each [NoSQL databases](https://aws.amazon.com/nosql/) offers unique strengths and is suited to different types of applications and `workloads`. Based on our project’s specific requirements—such as `data type`, volume, read/write patterns, and need for scalability and high availability—we can select the most appropriate NoSQL database to improve our system’s `performance` and `scalability`.

## References 📚
🔗 [Official NoSQL Documentation](https://aws.amazon.com/nosql/)  
🔗 [MongoDB Explained](https://www.mongodb.com/nosql-explained)  
🔗 [Types of NoSQL databases](https://www.mongodb.com/resources/basics/databases/nosql-explained)  
🔗 [MongoDB](https://www.techtarget.com/searchdatamanagement/definition/MongoDB)  
🔗 [Cassandra](https://cassandra.apache.org/_/index.html)  
🔗 [Redis](https://www.ibm.com/topics/redis)  
🔗 [Couchbase](https://docs.couchbase.com/home/index.html)  
🔗 [Neo4j](https://neo4j.com/docs/getting-started/get-started-with-neo4j/graph-database/)  
🔗 [YouTube Reference 1](https://youtu.be/0buKQHokLK8?si=C1WUIe2vbAH2ONeV)  
🔗 [YouTube Reference 2](https://youtu.be/VfcRxtBKI54?si=kjXGdp28yvRLdPO1)  
