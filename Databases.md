## Important Features of a Database

1. SQL or No-SQL

2. ACID properties

3. Consistent

4. Eventual consistency

5. Architectural Pattern - Master Slave ??

6. CAP theorem  Tradeoffs ?? Consistency -> Need to show latest commit, Availability --> Always need to show data whether correct or stale, Partition Tolerance --> when nodes come out of sink how well do they recover from the failure 

7. Transactions




#### Postgres

- SQL (RDBMS)
- Yes
- Not Guaranteed at Cluster Levels, Synchronized commits will leads to slow performance
- Asynchronous - No, Synchronous - Yes but total commits on the DB will be halted
- Applicable, Can configure Master-Slave, Master-Master
- CA
- Possible

#### Redis

- No-SQL(Key-Value)
- Not applicable
- Sub-milli second Latency & Consistent
- Strong Consistent
- Master-Slave, Pub-Sub, Queue
- CP
- Possible using Multi operations

#### Cassandra

- No-SQL(Key-column), CQLSH (Cassandra query language)
- No
- Not Strongly consistency
- Eventual Consistency - Yes
- No Master slave architecture, Every node plays the same role. High availability
- AP
- Supports atomicity and isolation at the row-level, but **trades transactional isolation** and atomicity for high availability and fast write performance

#### MongoDB

- No-SQL (Document Database)
- Yes , Document level
- Partial
- Eventually Consistent
- Single-master system (collections & documents) -- Writes Primary node & Reads from Secondary node.
- CP
- Not Applicable

