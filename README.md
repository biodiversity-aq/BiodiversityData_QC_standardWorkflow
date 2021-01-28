# Biodiversity data formating and Quality Control protocols and workflows. 

## Summary
This repo contains the standardized workflows or protocols to format biodiversity data into DarwinCore Occurrence Core or Event Core, and Quality Control (QC) the content implemented by the biodiversity.aq team. The workflows are meant to change the data, that is re-structure (adding fields, standardizing the content of fields), re-format (into a core with extensions) and map to DarwinCore. Protocols assume the data has been pre-processed formatted and mapped to DarwinCore, only perform a Quality control, and do not alter any data.

## How to use the workflows
The main aims of this workflow is to 1) standardize the format of the data in compliance with DarwinCore, 2) enrich the data with information that make it better computer readable or future-compatible (e.g. link taxonomic names to a taxonomic backbone) and 3) perform serval general quality checks along the way to identify errors or typos in the data (e.g. checking the dates, geographic coordinatesm,...). This workflow consists of 3 main chapters, each divided into several subsections. The first chapter deals with formatting and checks that are relevant for all datasets, and should always be run. The second chapter describes how to QC data with an occurrence core, and the third chapter deals with data formatted as an event core.
There is an enormous variety in the data that is submitted to biodiversity.aq, for example differing in research environment (e.g. terrestrial, marine, etc.), experimental set-up (e.g. environmental transect, GPS deployments, repeated measurements, etc.) or type of measurements taken (species occurrences, movement tracks, community composition of a fixed sample, abundances, etc.). To accomodate these differences into a single workflow, users can choose a data Core type (occurrence or event), and then select and runs specific sections of code in that chapter depending on the needs of the dataset. Each sub-section is specific for a certain QC or data formatting step, but not all code should be run each time. For our standard workflow, we use R as a programing language, which can be run through the R Studio (http://www.rstudio.com) develloping environment.


## More information
For more information, please contact the biodiversity.aq team:  https://www.biodiversity.aq/about/contacts/

