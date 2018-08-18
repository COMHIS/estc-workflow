# estc-workflow
Documentation for linkages and dependencies in different parts of ESTC processing [workflow](#workflow).

## Overview

### Raw MARC data parsing 
There are multiple interdependant repositories that together form the ESTC processing pipeline. The process starts with [MARC XML data parsing](https://github.com/COMHIS/MARCdata). The XML data is parsed into a master-csv file, that is then further processed in the data processing repositories, that are interdependent to a varying degree.

### Field preparation and harmonization
The data unification code in those repositories both input from and output to the private [aggregate csv data repository](https://github.com/COMHIS/estc-data-private). This explained in more detail in the [/dependencies](./dependencies) -section.

### Summaries
Standard summary document and tables are generated automatically for each processed field, available in the respective processing folders.

### Analysis
General analysis of that processed data is done in [ESTC-analysis-general](https://github.com/COMHIS/estc-analysis-general) -repository, and links to further dataset specific analysis scripts are collected in [/dependencies](./dependencies) -folder.

## Workflow
The interdependencies of the various parts of the workflow are documentend in [/dependencies](./dependencies) -folder. To run any isolated processing script, you need to:
* Consult the [dependency chart](./dependencies#overall-workflow) and find out what inputdata the code depends on,
* check if that data has changed and pull it from [csv-data](https://github.com/COMHIS/estc-data-private),
* and update the [csv-data](https://github.com/COMHIS/estc-data-private) repository with new output.
* Additionally, keep the [/dependencies](./dependencies) documentation for the relevant script up to date.

## Data
Data structure is documented in the [data repository](https://github.com/COMHIS/estc-data-private). 

## TODO
Major parts of the workflow that need updating:
* MARC XML parser rewrite
* Separate data processing and analysis -scripts
