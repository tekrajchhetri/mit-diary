---
title: Week 8
linkTitle: Week 8
weight: 8
---
## Overview

The plan for week 8 is to complete the web application, which will give the **first basic view** of the knowledge graphs (KGs) visualization, and discuss it with the team to get feedback. Additionally, the plan is to start work on the survey paper.

{{% callout note %}}
Most of the links here are to the [Sensein](https://sensein.group/) Google Drive (or private repository) and, therefore, are inaccessible to the external world. Whenever feasible, the information is disclosed to the public.
{{% /callout %}}

## What have I done?

As planned this week, I have worked on completing the basic configurable version of the web application that allows users to interact with our knowledge graphs. The web application design is inspired by WordPress, i.e., configurable, and allows one to configure (see Figure 1) what to display to the users (e.g., menu and knowledge graph contents). The primary reason for following this approach is to make our work reusable with minimal effort upon open source, as often _it's very difficult or time-consuming or requires a lot of work to use most of the existing open-source implementations_. 

<img src="configured-menu-queries.png" alt="Configurable view" style="width:700px;"/>
Figure 1: Configuration of the menu options as well as the KG content to display

Similarly, Figures 2, 3 and 4 show the basic visualization on the user side.

<img src="kb-view-default.png" alt="Configurable view" style="width:700px;"/>
Figure 2: The default view when the page loads

<img src="kb-view-navigation.png" alt="Configurable view" style="width:700px;"/>
Figure 3: Current view displayed after selecting an option by clicking on the ID

<img src="kb-view-navigation-I.png" alt="Configurable view" style="width:700px;"/>
Figure 4: The view displayed after selecting an option from the provenance (was derived from), accessed by clicking the ID

The next thing I worked on was preparing the presentations to discuss in our weekly lab meeting how we want to display the KG contents and what we would like to have in Evidence and Assertions. It's essential to have these things discussed as BrainyPedia integrates heterogeneous knowledge, e.g., genome annotations and donors. The slides can be accessed at [Presentation Slides](https://shorturl.at/J8EUK) (no public access). Following our meeting, I collected more data from different models, such as [ANSWRS](https://github.com/brain-bican/ansrs-schema) and [analyzed](https://shorturl.at/bqZX8) it to find the links to the [BICAN model](https://github.com/brain-bican/models/blob/cb70a5ee9d430f119eda52034d45f9b3525bc272/linkml-schema/bican_biolink.yaml). After analyzing, I worked on the SPARQL queries that I can use later for the implementation. The different SPARQL queries are available in our [BrainyPedia repository](https://github.com/sensein/brainypedia/tree/ingestion-fapi-skeleton/sparql_queries).

 
The next planned task that I worked on was the survey paper. The collected papers for review, as well as the annotated papers are available in [Google Drive](https://shorturl.at/mYMzG), and the survey paper is on Overleaf.


## What is the result?

The following are the major outcomes of this week.

- The (basic) visualization is completed, and it will be improved further based on the feedback received and the data end-to-end integration with other microservices components like the query service.
- Analyzing and understanding the collected KGs from different models to find the common links.
- Generating the necessary SPARQL queries so that they can be used later for implementation, a task (implementation completion + deployment) planned for next week.
- Collecting papers, reviewing them and writing manuscripts.


**Codes:**

- [SPARQL queries](https://github.com/sensein/brainypedia/tree/ingestion-fapi-skeleton/sparql_queries)
- [Collected papers for review](https://shorturl.at/mYMzG) 
- [Presentation slides from lab meeting](https://shorturl.at/J8EUK)
 	 


<!-- ### References -->

 
