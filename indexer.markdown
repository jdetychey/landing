---
layout: default
---

<a href="/">Back</a>

# Indexer

## What it is

All applications that integrate blockchain data in their user journey need to query it at some point. Natively that data is formatted and stored to fit blockchain specifications that are based on different paradigms than what advanced real-life use cases require. After trying out the different approaches available on the market, we realized that we need a more flexible approach that can fit closer to the needs of different usages.

The Alambic blockchain extractor is the heart of the indexing process. It is able to feed any kind of service with a live stream of the latest logs emitted by the blockchain. The receiver of those logs can then use our indexing SDK to convert those logs into ready-to-use data. This system allows you to build easily whatever schema you might need out of this data, whether it is a relational database, a search engine, or a more specific structure.

With blockchain data prepared to fit your needs, your application developers or data analysts will be able to leverage whatever tool is necessary to bring the best value and experience to your users.  


## How it is done

We based our indexer approach on using a dedicated service to register blockchain data sources and properly query an RPC node for the logs we need. Those logs are then pushed into Kafka event streams. This approach allows to easily duplicate extractor instances and Kafka brokers, it combines simplicity and scalability. 

Any business service can connect to the event streams and use our SDK to receive the logs and start processing them. The rest of the data processing can be implemented however it might be needed for different use cases.

The indexer provides an easy-to-use Source API to dynamically add new contracts or topics to listen to. Details about reorgs are also communicated on the event streams to facilitate the data updates they might imply.


[Blockchain indexer architecture]