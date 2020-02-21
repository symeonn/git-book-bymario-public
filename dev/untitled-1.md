# DB

### CAP theorem

Consistency  
Availability  
Partition tolerance

In distributed database system only two of the following can be guaranteed:

![](../.gitbook/assets/image%20%285%29.png)

### ACID

Atomicty  
Consistency  
Isolation  
Durability

### RDBMS - relational database management system

### Relational vs. noSQL

relational DB are optimized for fast writes \(entities are granulated\) and when we query for complex objects we need to join tables together

noSQL are opposite of above - every table is already the query result, so you need to know all queries upfront

## MongoDB

### Export query result to JSON

query file content example:

```text
var collection = db.getCollection('curriculum_group_tree').aggregate([
    // {$limit: 1},
    {$addFields: {"publishedLearningFactors.childFactors.childFactors.currName": "$name"}},

    {$project: {chlf: "$publishedLearningFactors.childFactors.childFactors"}},

    {$unwind: "$chlf"},
    {$unwind: "$chlf"},
    {$unwind: "$chlf"},
    {
        $addFields: {
            "chlf.subIds": {
                "$reduce": {
                    "input": "$chlf.linkedSourceList.subcategoryIdList",
                    "initialValue": [],
                    in: {$concatArrays: ["$$value", "$$this"]}
                }
            }
        }
    },

    {
        $project: {
            "chlf._id": 1, "chlf.currName": 1, "chlf.name": 1, "chlf.subIds": 1
        }
    },

    {$replaceRoot: {newRoot: "$chlf"}},
]);

while (collection.hasNext()) {
    var element = collection.next();

    if (element.subIds && element.subIds.length > 0) {
        for (var item of element.subIds) {
            print(element._id.hex() + "," + JSON.stringify(element.name) + "," + element.currName + "," + item);
        }
    } else {
        print(element._id.hex() + "," + JSON.stringify(element.name) + "," + element.currName + ",");
    }

}

```

CLI:

mongo -u &lt;username&gt; -p &lt;password&gt; --quiet &lt;dbName&gt; &lt;queryFilePath&gt;.js &gt; &lt;resultFileName&gt;.json

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

![](../.gitbook/assets/image-14.png)

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

