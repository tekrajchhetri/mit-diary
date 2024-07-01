---
title: Week 13
linkTitle: Week 13
weight: 13
---
## Overview

This week, the plan is to continue working on crawling, update the ecosystem diagram, transcribe the BICAN video text, and work on the knowledge graphs (KGs) validator.

{{% callout note %}}
Most of the links here are to the [Sensein](https://sensein.group/) Google Drive (or private repository) and, therefore, are inaccessible to the external world. Whenever feasible, the information is disclosed to the public.
{{% /callout %}}
<br/>

{{% callout warning %}}
The finalized name for our application is **BrainKB**, no BrainyPedia.
{{% /callout %}}

## What have I done?

This week, as planned, I worked on crawler. In particular, I have updated to code to download the metadata information, such as copyright information about the publication. In addition to updating the code, I also created a pull request and resolved the review comments. Further to working on the crawler, I also worked on improving the ecosystem diagram.

In addition, I worked on transcribing the video from BICAN workshops using OpenAI Whisper mode. The transcribed texts are available in [Sensein Google Drive](https://drive.google.com/drive/folders/1zLIPi50dmROANIZsmI5nQcGXr_XIDCUA?usp=drive_link). Apart from transcribing text and improving the crawling code, I also worked on KG validation, generating the necessary skeleton and unit tests.

Moreover, I organized a meeting with Ontotext to discuss GraphDB. I also held an internal meeting with the Sensein team to review the architecture, during which we decided to use NextJS for the UI.


## What is the result?

The major results of this week are as follows:

- Updated the ecosystem diagram to improve the readibility.
- Updated the code to crawl the Biorxiv publications to dowload the metadata information.
- Crawled and downloaded 41K publications from Biorxiv relating to neuroscience and their corresponding metadata information.
- Addressed the reviewed comments and merged the created pull request. 
- Transcribed BICAN workshop videos.
- Implemented basic functionalities required for KG validator and generated the corresponding unit tests.

**Codes/Other Resources:**

- [Updated Biorxiv Crawler Code](https://github.com/sensein/crawler_publications) 
- [KG Validator](https://github.com/sensein/graph_validator/tree/validator)
- [Updated Ecosystem Diagram](https://drive.google.com/file/d/1WjFh6fWgotVYBEQkayrZzJvSaxVpDZiZ/view?usp=drive_link)
- [Transcription of BICAN video using Whisper](https://drive.google.com/drive/folders/1zLIPi50dmROANIZsmI5nQcGXr_XIDCUA?usp=drive_link)


<!-- ### References -->

 
