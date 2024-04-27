---
title: Week 5
linkTitle: Week 5
weight: 5
---
## Overview

We defined our objective to concentrate on the development of a decentralized architecture during our discussions in week four. Nevertheless, before commencing the architectural design phase, it was essential to analyze the decentralization features that we are interested in or applicable to our particular use case. In our use case, we prefer the following features.

- Allow anyone to join, i.e., plug and play like a plugin.
- No central authority.
- Scalable and performant.
- Trustworthiness of knowledge graphs (KGs) triples.

The following features are currently not relevant to our use case.

- Immutability.
- Peer-to-Peer Transactions.
- Smart Contracts.

The following are why the features above are not interesting to us.

- The first reason is the blockchain's scalability and performance issues. For example, blockchain has low transactional efficiency (Bitcoin can only conduct **7 TPS (transactions per second) and Ethereum 30 TPS**) and high confirmation delay (Bitcoin takes **at least 10 minutes to confirm** as the Bitcoin block generation speed is 10 minutes) [1].
- The second reason is the **interoperability and integration** issues, especially with traditional systems and cloud infrastructures for tasks such as machine learning (ML) model training [2], which is essential in our use case and will play a key role in the BrainyPedia.

In addition to the work on the architecture, this week, the plan is to work on the design document, address the (code) review comments, and work on the web application.

 

## What have I done?
Following our initial plan of decentralization, the idea is to use the messaging service in a manner similar to the [distributed hash table (DHT)](https://en.wikipedia.org/wiki/Distributed_hash_table). DHT stores the information, i.e., key-value pair, about the peer nodes and provides the lookup service. Figure 1 shows the idea of the high-level architecture using a messaging service, which will further be mediated through a custom relay in the case of multiple messaging services. The reason for using messaging service is because of its scalability, and we are not interested in typical decentralized systems like the one based on blockchain. 

<img src="decentralized.png" alt="Decentralized Architecture" style="width:400px;"/>
Figure 1: Initial Decentralized Architecture

Figure 2 illustrates the microservices architecture, aka distributed systems (see Figure 3), which we will implement first. This is because we can later couple with our decentralized idea easily. If we decide not to have the decentralized approach, we would still have the full-fledged and scalable system performing all the BrainyPedia tasks.

<img src="high-level-arch.png" alt="High-level Architecture" style="width:600px;"/>
Figure 2: Initial High-level Architecture of BrainyPedia

<img src="distributed.png" alt="Distributed Systems" style="width:400px;"/>
Figure 3: Distributed Systems

Additionally, in terms of architecture, I worked on the ingest service architecture (see Figure 4), a pivotal component.

<img src="ingest.png" alt="ingest" style="width:600px;"/>
Figure 4: Ingest Service Architecture

Other than the architecture design, I worked on the design document and implementation of the web application that will enable interaction with BrainyPedia knowledge base to users, implementation of ingestion service, and finalizing review comments of FastAPI skeleton.

## What is the result?
The initial architecture design has been completed.

While still in progress, the design document has been updated to include new information like target audience, the motivation behind BrainyPedia and also addressing some of the review comments. 

- [Design document](https://github.com/sensein/brainypedia-design-document/tree/design-doc)

The pull request has been merged after addressing all the review comments.

- [FastAPI Skeleton](https://github.com/sensein/fastapi-skeleton)

The work on web application and ingestion service is also in progress.

- [Web Application](https://github.com/sensein/brainypedia/tree/WebApp)

- [Ingestion Service](https://github.com/sensein/brainypedia/tree/ingestion-fapi-skeleton)


### References

[1] Yang, D., Long, C., Xu, H. and Peng, S., 2020, March. A review on scalability of blockchain. In Proceedings of the 2020 the 2nd International Conference on Blockchain Technology (pp. 1-6).<br/>
[2] Alsagheer, D., Xu, L. and Shi, W., 2023. Decentralized machine learning governance: Overview, opportunities, and challenges. IEEE Access.

