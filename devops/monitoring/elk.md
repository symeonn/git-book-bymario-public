# ELK

![](../../.gitbook/assets/image-3.png)

have to user same version of elasticsearch and kibana

{% embed url="https://www.elastic.co/guide/en/elastic-stack-get-started/current/get-started-elastic-stack.html\#install-elasticsearch" caption="" %}

## ElasticSearch

configuration  
\[elasticsearch\_path\]/conf/elasticsearch.yml  
\[elasticsearch\_path\]/conf/jvm.options

#### Import/Export dumps: 

[https://github.com/taskrabbit/elasticsearch-dump](https://github.com/taskrabbit/elasticsearch-dump)

`$ elasticdump --limit 10000 --input "/c/Users/mario/Desktop/ELK/original/events-index_data-2019.12.11-01.50.json" --output=h`[`ttp://localhost:9200/events`](http://localhost:9200/events)

## Kibana

{% embed url="https://www.elastic.co/downloads/kibana" caption="" %}

configuration  
\[kibana\_path\]/conf/kibana.yml  
uncomment or add  
`elasticsearch.hosts: ["http://localhost:9200"]`

{% file src="../../.gitbook/assets/elk.postman\_collection.json" %}

### POSTMAN

