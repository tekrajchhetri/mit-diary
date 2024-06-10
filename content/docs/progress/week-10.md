---
title: Week 10
linkTitle: Week 10
weight: 10
---
## Overview

The plan for week 10 is to improve the web application further and work on survey paper and workshop preparations (e.g., presentation).   

{{% callout note %}}
Most of the links here are to the [Sensein](https://sensein.group/) Google Drive (or private repository) and, therefore, are inaccessible to the external world. Whenever feasible, the information is disclosed to the public.
{{% /callout %}}
<br/>

{{% callout warning %}}
The finalized name for our application is **BrainKB**, no BrainyPedia.
{{% /callout %}}

## What have I done?
As planned, I worked on improving the web application. In particular, the following major improvements were made: (i) optimized the SPARQL query, thereby improving the load time; and (ii) updated the entity card design and the view on how information is presented. Additionally, the other pages, such as About, were also updated to include more information. Figures 1, 2, 3 and 4 show the updated view. 

I also worked on deploying the updated application on AWS, setting up an SSL certificate to enable HTTPS, configuring AWS Route 53 to set up the new subdomain, and mapping the BrainKB web application to it.

<img src="landing.png" alt="Updated index page" style="width:700px;"/>
Figure 1: Updated home page 
 
<img src="kb-page.png" alt="KB page" style="width:700px;"/>
Figure 2: Updated knowledge base page

<img src="entity-card.png" alt="Entity card" style="width:700px;"/>
Figure 3: Entity card

<img src="about.png" alt="About" style="width:700px;"/>
Figure 4: About us page

In addition to improving the web application, I worked on BICAN workshop preparations, such as entity-card exercise and addressing the design document review comments. Moreover, I also had a weekly meeting with one of the interns working with me on BrainKB and guided him on the next steps.

## What is the result?
The following are the major results of this week.
- Optimized SPARQL query, thereby improving the performance.
- Deployed updated application on AWS and setup [beta.brainkb.org](https://beta.brainkb.org).
- Configured SSL certificate to enable HTTPS.
- Improved the entity card design by updating the implementation. 


**Codes:**
- [BrainKB source code](https://github.com/sensein/BrainKB/tree/ingestion-fapi-skeleton)
- [SPARQL queries](https://github.com/sensein/brainypedia/tree/ingestion-fapi-skeleton/sparql_queries) 
 	 


<!-- ### References -->

 
