# Biodiversity data formating and Quality Control workflows. 

## Summary
This repo contains the standardized workflows to Quality Control (QC) and format biodiversity data into DarwinCore Occurrence Core or Event Core, as implemented by the biodiversity.aq team. The workflows start from any raw data tables and are meant to re-structure (adding fields, standardizing the content of fields), re-format (into a core with extensions) and map to DarwinCore. 
The data validator script check wether the data (as CSV file) conforms to the DarwinCore [standard for text](https://dwc.tdwg.org/text/), and checks the correct use of DarwinCore terms, including specific requirements and formats of fields. It assumes the data has been pre-processed, formatted and mapped to DarwinCore. It differs from the [GBIF Darwin Core archive validator](https://www.gbif.org/tools/data-validator/about), as validation of the content of the data is more thorough, including a search for typos and pseudoreplicates. This higher resolution in validating the content of the data is achieved by tayloring the validator to a limited range of input data (occurrence Core).


## How to use the workflow
The main aims of this workflow is to 1) standardize the format of the data in compliance with DarwinCore, 2) enrich the data with information that make it better computer readable or future-compatible (e.g. link taxonomic names to a taxonomic backbone) and 3) perform serval general quality checks along the way to identify errors or typos in the data (e.g. checking the dates, geographic coordinatesm,...). This workflow consists of 3 main chapters, each divided into several subsections. The first chapter deals with formatting and checks that are relevant for all datasets, and should always be run. The second chapter describes how to QC data with an occurrence core, and the third chapter deals with data formatted as an event core.
There is an enormous variety in the data that is submitted to biodiversity.aq, for example differing in research environment (e.g. terrestrial, marine, etc.), experimental set-up (e.g. environmental transect, GPS deployments, repeated measurements, etc.) or type of measurements taken (species occurrences, movement tracks, community composition of a fixed sample, abundances, etc.). To accomodate these differences into a single workflow, users can choose a data Core type (occurrence or event), and then select and runs specific sections of code in that chapter depending on the needs of the dataset. Each sub-section is specific for a certain QC or data formatting step, but not all code should be run each time. For our standard workflow, we use R as a programing language, which can be run through the R Studio (http://www.rstudio.com) develloping environment.

## How to use the validator
The data validator scripts are written in R markdown, and need to be rendered with the knitr package after updating the source directory and file name of the data that needs to be validated. The output of this script is a PDF quality report with a number of potential issues flagged.

## More information
For more information, please contact the biodiversity.aq team:  https://www.biodiversity.aq/about/contacts/

