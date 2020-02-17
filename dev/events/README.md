# Events

## AMQP

### Producer

sends the message with the routing key

### Exchange

it is node that sends the msgs to appropriate queue by binding key, compares routing key with the binding key

Types

* fanout - sends to all
* direct - sends to specific queue
* topic - uses part of routing key \(eg. "foo.\*"\)
* header - uses msg header to connect to queue

### Queue

### Consumer

registers to queue\(s\) and when the msg arrives consumer get notified about it or receive msg right away

