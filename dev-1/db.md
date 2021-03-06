# DB

### CAP theorem

Consistency  
Availability  
Partition tolerance  


In distributed database system only two of the following can be guaranteed:

![CAP diagram](../.gitbook/assets/image.png)

### ACID

Atomicty  
Consistency  
Isolation  
Durability  


### RDBMS - relational database management system



## Cassandra

```text
CREATE TABLE IF NOT EXISTS learning_scores.exercise(
  student_id bigint, 
  solution_time timestamp,
  exercise_id bigint,
  score float,
  activity_type text,
  activity_id bigint,
  primary key (student_id, exercise_id,solution_time)
  ) WITH CLUSTERING ORDER BY (exercise_id DESC ,solution_time DESC);  
```

* The **Partition Key** is responsible for data distribution across your nodes \(student\_id\)
* The **Clustering Key** is responsible for data sorting within the partition \(exercise\_id, solution\_time\)

Replication factor - on how many nodes data should be replicated  
Consistency level - how many replies should Cassandra have to respond OK   
ALL - all replicas should be written, QUORUN - majority \(RF=5 &gt; CL =3, etc\) , ONE - sends OK when only one write to happen \(lower is faster IO and high available\)  


#### Write

![write process](../.gitbook/assets/image%20%2814%29.png)

for each flush SSTable is created, later async merge process \(compaction\)

#### Tombstone

after data has been deleted instead of erasing, the tombstone \(nagrobek\) is set that data is deactivated

#### Logs

 There are three types of Log files in /var/log/

1. cassandra.out
2. system.log
3. gc-&lt;number&gt;.log

tracing on;

### Get started with cassandra on docker

`$ winpty docker exec -it cassandra-db bash  
cqlsh   
desc keyspaces;  
use <keyspace>;  
desc tables;`  


## Other:

denormalize - put data from some tables into another one to prevent joins and increase performance, but this approach introduces data redundancy 

sharding - different data on different masters, DBs, different places



