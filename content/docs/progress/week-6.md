---
title: Week 6
linkTitle: Week 6
weight: 6
---
## Overview

The plan for week 6 is to continue the work I did in week 5, namely, the web application (see Figure 1) and the ingest service (Figure 2). Additionally, the plan is also to work on the implementation of the semantic entity resolution algorithm. 

<img src="webapp.png" alt="Web Application" style="width:700px;"/>
Figure 1: BrainyPedia Web Application

<img src="ingest.png" alt="ingest" style="width:600px;"/>
Figure 2: Ingest Service Architecture

 

## What have I done?
As planned, I worked on the ingestion service (Figure 3), implementing the architecture (Figure 2) presented in the overview section. The ingestion service currently has endpoints (not all functionalities have been implemented) that allow users to upload different file types, such as Excel, Text, JSON and CSV, to create knowledge graphs. Additionally, it provides an endpoint to ingest JSON-LD, raw text and JSON inputs. The worker listens to the messaging queue and relays the request as necessary for further processing, e.g., validations. 

<img src="ingest_api.png" alt="Ingestion Service" style="width:700px;"/>
Figure 3: Ingestion Service

However, the current implementation lacked authorization and authentication, meaning, anyone could make a request to our service-something not desirable. Therefore, in addition to working on ingestion service, I also worked on upgrading the initial Fast API skeleton to include token (or JWT token) based authentication and authorization. Additionally, to easily manage the JWT users and the scopes (or permissions), I have created a web application, _JWT User & Scope Manager_. Figures 4, 5 and 6 show the snapshots of the application.

{{% callout note %}}
The [Fast API Skeleton](https://github.com/sensein/fastapi-skeleton) is now dependent on _[JWT User & Scope Manager](https://github.com/sensein/brainypedia/)_ web application
{{% /callout %}}
 

<img src="overview.png" alt="JWT User & Scope Manager Overview" style="width:600px;"/>
Figure 4: JWT User & Scope Manager Admin Overview

<img src="scopes.png" alt="Scopes Overview" style="width:600px;"/>
Figure 5: Overview of different Scopes, i.e., permissions

<img src="users.png" alt="Users Overview" style="width:600px;"/>
Figure 6: Overview of JWT user(s)

In addition to the work on ingestion service, upgrading the FAST API skeleton and JWT User & Scope Manager, I have also worked on implementation of the query service, which at the moment implements the functions to query data from graph database and establish connection.

{{% callout note %}}
The _[JWT User & Scope Manager](https://github.com/sensein/brainypedia/)_ web application uses PostgreSQL database that will be used to store information about JWT users and scopes. The docker compose file is available in APItokenmanager->docker-postgresql directory.
{{% /callout %}}

## What is the result?

This week's major achievement was the upgrade of the Fast API skeleton and JWT user manager. The upgraded version can now be used in any other FAST API-based projects, saving time that would otherwise be spent implementing features such as user management, security, roles (or scopes), and their management. As shown in the code segment below, it is as easy as defining the API endpoints to protect the REST API endpoints with a JWT-bearer token and scopes (permissions).

```python 
@router.get("/endpoint-name", dependencies=[Depends(require_scopes(["read"]))]) #1 check if the authenticated user has read permission
async def your_endpoint_name(user: Annotated[LoginUserIn, Depends(get_current_user)]): #2 check if the user (or bearer token) is a valid one 
    #your logic 

```
The other updates include the implementation of the query service and ingestion service.

**Codes:**

- [Fast API Skeleton](https://github.com/sensein/fastapi-skeleton) 
 	- _Currently, in authtoken branch, need to merge with master._

- [JWT User & Scope Manager](https://github.com/sensein/brainypedia/)
	 - _Currently, in the ingestion-fapi-skeleton branch under the APItokenmanager directory, it needs to be merged with the master._

- [Query Service](https://github.com/sensein/brainypedia/)
	 - _Currently, in the ingestion-fapi-skeleton branch under the query_service directory, it needs further work before merging with the master._
- [Ingestion Service](https://github.com/sensein/brainypedia/)
	 - _Currently, in the ingestion-fapi-skeleton branch under the ingestion_service directory, it needs to be refactored to include security features, i.e., JWT-based authentication and authorization._


<!-- ### References -->

 
