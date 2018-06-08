Linkfire DevDataOps assesment
================

What to do?
===========

First of all, clone this repository:

```
git clone git@github.com:getlinkfire/devDataOps-assesment.git
```

Now, given [this Docker Compose file](./docker-compose.yml), stand up a [Druid](http://druid.io) cluster.

The compose file is going to launch :

- 1 zookeeper node
- 1 MySQL database
- 1 Kafka message broker

and the following druid services :

- 1 broker
- 1 middlemanager
- 1 historical
- 1 coordinator/overlord

This will take a couple of minutes, but once it is up, you will have:  
- The Druid cluster dashboard on: (http://localhost:3001/#/)
- The Druid indexing console on: (http://localhost:3001/console.html)

Now that you have a running cluster, [ingest](wikiticker-index.json) the data found in (data/wikiticker-2015-09-12-sampled.json.gz).  
Once your ingestion job has succesfully executed, perform [a simple query](wikiticker-top-pages.json) on the freshly created *datasource*.

The dataset is kindly borrowed from the [Druid quickstart tutorial](http://druid.io/docs/0.12.1/tutorials/quickstart.html), you may find some inspiration there.  
Read little about the [Druid indexing service](http://druid.io/docs/0.12.1/design/indexing-service.html) if you like ;)
