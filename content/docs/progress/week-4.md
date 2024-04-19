---
title: Week 4
linkTitle: Week 4
weight: 4
---
## Overview

Week 4 started after a long holiday—a weekend followed by Patriots Day! This week, the plan is to work on the BrainyPedia implementation. Alongside the implementation, the plan is to work on the architecture, as the plan is to move away from the centralized architecture (see Figure 1) because of its limitations. The centralized controlling authority has been viewed as a key limitation of the centralized architecture/system, thus giving rise to decentralization (or decentralized systems). 


<img src="centralized.png" alt="Centralized System" style="width:400px;"/>
Figure 1: Centralized architecture
 
{{% callout note %}}
A decentralized system is one in which there is no single point of control or authority. Bitcoin is a good example of such a system.
{{% /callout %}}

Therefore, decentralized systems are more preferred, and interest in them is growing. However, that being said, they have limitations and may not always be suitable. One of the prime limitations is scalability, which has been highlighted by numerous studies, such as the one by Yang et al. [1]. Moreover, the nature of the tasks BrainyPedia will perform makes use of the current blockchain-based decentralized approach unsuitable. So, the question is, _can we design the BrainyPedia in a decentralized (Figure 2) manner such that there is no single controlling authority?_

<img src="brainypedia-decentralized.png" alt="Decentralized System" style="width:400px;"/>
Figure 2: Decentralized BrainyPedia

In a nutshell, my major objectives for this week are to seek an answer to my question, as mentioned earlier, regarding the decentralization of BrainyPedia and start the implementation of BrainyPedia.

## What have I done?
While BrainyPedia's architecture has not yet been finalized, a complete implementation would not be possible. Therefore, to bootstrap the development later, I decided to implement the generic application skeleton based on FastAPI that can be used in this project and by others. The logging features have been implemented, and I need to resolve a few review comments before merging it into the main branch. The code is available in Sensein GitHub at [https://github.com/sensein/fastapi-skeleton](https://github.com/sensein/fastapi-skeleton).

The second is decentralization. For this first, I looked into existing works, particularly, the [Linked Data Fragments](https://linkeddatafragments.org/software/), which allows web-scale querying of Linked Data. The other thing I have done is test the [distributed hash table](https://en.wikipedia.org/wiki/Distributed_hash_table), a distributed system that provides a lookup service and is used in decentralized systems for node discovery. In particular, I have experimented with [Kademlia]((https://kademlia.readthedocs.io/en/latest/index.html)) [2] setting up 2 AWS instances and my own Mac. Other than that, I have also tested an approach based on a message-passing mechanism using [RabbitMQ](https://www.rabbitmq.com/) and graph databases [GraphDB](https://www.ontotext.com/products/graphdb/?ref=menu) and [Blazegraph](https://blazegraph.com/).


## What is the result?

While the Linked Data Fragments is interesting, the question of whether it can be used or not, I have come to the following conclusions based on my analysis so far:

- If we use the centralized architecture, I see the possibility for Linked Data Fragments and its benefits. This will also allow us to utilize heterogeneous graph storage.
- Technically, Linked Data Fragments should be possible to implement even in decentralized systems. However, I do not see the (increased) benefits, at least from my preliminary analysis for BrainyPedia, but rather the increased complexity. 

Regarding the question of decentralizing BrainyPedia, I see the possibility and the architecture will soon follow.

### References
[1] Yang, D., Long, C., Xu, H. and Peng, S., 2020, March. A review on scalability of blockchain. In Proceedings of the 2020 the 2nd International Conference on Blockchain Technology (pp. 1-6).<br/>
[2] Maymounkov, P. and Mazieres, D., 2002, March. Kademlia: A peer-to-peer information system based on the xor metric. In International Workshop on Peer-to-Peer Systems (pp. 53-65). Berlin, Heidelberg: Springer Berlin Heidelberg.