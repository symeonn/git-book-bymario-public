---
description: >-
  https://www.oracle.com/webfolder/technetwork/tutorials/obe/java/gc01/index.html
---

# GC

## HotSpot achitecture

![](../../.gitbook/assets/image%20%283%29.png)

## Automatic Garbage Collection

Steps

1. Marking
2. Normal Deletion
3. Deletion with Compacting

## JVM Generations

![](../../.gitbook/assets/image%20%2810%29.png)

##  **Island of isolation**

When object A reference object B, and object B references object A, but non of these objects is referenced by any other object in whole application.  
If objects A or B are not references by any GC root object \(threads, static variables, local variables etc\), A and B will be collected.

