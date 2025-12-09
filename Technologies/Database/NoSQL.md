NoSQL (**Non-relational SQL**) databases are a diverse group of database systems that provide a mechanism for storage and retrieval of data that is **modeled in ways other than the tabular relations** used in traditional relational databases

#### Characteristics
- Data structure can be highly fluid. You can add fields to records without affecting other records in the database
- Databases are typically designed to scale out horizontally by distributing the data load across multiple low-cost servers, rather than scaling up vertically by requiring more expensive, powerful single servers

#### The Four main types of NoSQL Databases
NoSQL is not a single technology but an umbrella term covering several distinct architectures, each optimized for different data models and workloads:

##### 1. Key-Value Stores
- **Concept:** The simplest form of NoSQL. Data is store as a collection of unique keys and corresponding values
- **Analogy:** A massive dictionary where the key is the word, and the values is the definition
- **Use Cases:** Caching, session management, user profiles
- **Examples:** Redis, Memcached, DynamoDB

##### 2. Document Databases
- **Concept:** Stores data in flexible, semi-structured documents (often JSON, BSON or XML format). A document can contain arrays, nested data and varying fields
- **Analogy:** A filling cabinet where each folder holds all the information related to a single entity (e.g., a customer)
- **Use Cases:** Content management systems, catalogs, user management and e-commerce product databases
- **Examples:** MongoDB, Couchbase

##### 3. Wide-Column Stores
- **Concept:** Similar to a relational table, but columns are grouped into "column familities". Designed for massive scale and high availability, optimizing for retrieving data in large, predictable slices
- **Analogy:** A two-dimensional map where the rows are keys, and the columns are highly distributed
- **Use Cases:** Time-series data, operational logging, large-scale analytics and high-volume data ingestion
- **Examples:** Cassandra, HBase, Google Bigtable

##### 4. Graph Databases
- **Concept:** Stores data as nodes and edges. Highly optimized for modeling and traversing complex relationships
- **Analogy:** A social network map where people are nodes and friendships are edges
- **Use Cases:** Social networks, recommendation engines, fraud detection, identity and access management
- **Examples:** Neo4j, Amazon Neptune