---
title: Week 7
linkTitle: Week 7
weight: 7
---
## Overview

The plan for week 7 is to refactor the code, integrate JWT-based authentication and authorization, and deploy the application to AWS. Additionally, the plan is to work on a web application that allows knowledge exploration via a user interface.

## What have I done?
As planned, I worked on refactoring the code and integrating the token (or JWT)--based authentication and authorization.  The rest endpoints are now secured with JWT and access to any protected endpoints as indicated by the lock sign in Figure 1 requires both: _(i) a valid JWT token; and (ii) a valid permission (or scopes)_.  Anyone who wishes to use the service must register using the register endpoint, and the registered user can obtain the token via the token endpoint. 

<img src="jwt-integrate.png" alt="JWT Integrate" style="width:700px;"/>
Figure 1: Ingestion Service REST Endpoints after integration of Token-based Authentication & Authorization

{{% callout note %}}
- You will not be able to access the protected endpoints just by registering. The registration needs to be confirmed (or activated) by the administrator and have the appropriate permissions, which the administrator can assign.
- At the moment, we only support ingestion via the _raw/jsonld_ endpoint. As we progress, support for the rest will be enabled. 
{{% /callout %}}

Additionally, the other services, such as query service, were also refactored.

The other planned task that I worked on was deploying all the applications. Currently, six different services, including databases, different microservices (e.g., query service), and web applications (e.g., API token manager), are running and have been deployed in three different (two micro and one large) EC2 instances. The reason for using multiple instances is the separation of deployment based on service type and tolerance. For instance, consider a scenario where microservices are hosted on the same server as the database. If there's an issue (e.g., while debugging a microservice), it will only impact the services related to that microservice, without affecting the database. Another reason involves the system requirements for various services, such as graph databases, which generally demand higher configurations—like more RAM and storage.

The next planned task is visualizing the knowledge graphs (KGs). While I was also expecting this task to be completed by today, it seems it might need a day or two more; the AWS deployment of different services consumed more time than I had anticipated. I am focused on better understanding the LinkML Schema and KGs (Figure 2) and testing corresponding SPARQL queries. This understanding is important for identifying the knowledge embedded within the KGs, which will inform our decisions on what should be prioritized for visualization based on the interests and needs of the users and the broader community.

<img src="kg_viz.png" alt="Knowledge graph visualization" style="width:700px;"/>
Figure 2: Sample Instance of a Knowledge Graph



## What is the result?

The following are the major outcomes of this week.

- The first is the integration of token-based authentication & authorization to other services, e.g., ingestion services.
- The second is deploying ([Deployed Ingest REST Endpoints](http://3.143.252.80:8006/docs)) the different (micro-)services to the AWS.
- The third is the end-to-end integration of the different microservices.

The other updates include addressing the code review comments and analyzing KGs, generating SPARQL queries needed to implement

**Codes:**

- [Fast API Skeleton](https://github.com/sensein/fastapi-skeleton) 
 	- _Currently status: pull request is in review._


- [Ingestion Service](https://github.com/sensein/brainypedia/)
	 - _Currently, the ingestion-API-skeleton branch is under the ingestion_service directory. The code has been refactored to include security features, i.e., JWT-based authentication and authorization._


<!-- ### References -->

 
