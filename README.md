# estc-workflow
Documentation for linkages and dependencies in different parts of ESTC processing [workflow](#workflow).

Quick and dirty summary for adding your work to the ESTC workflow can be found below under the header *[Guidelines](#guidelines)*.

## Overview
Starting point of the ESTC refining and analyzing workflow is the raw XML dump provided by the British Library. This is parsed into "raw" csv format, that is easier to access, and break into multiple fields, such as title, author, edition or publisher information. Those data subsets are then refined in different scripts and their outputs, as well as the raw input data is collected in the [data repository](https://github.com/COMHIS/estc-data-private).

Any analysis scripts take as their starting points one or more of these derived datasets in the data repository, and combines them as needed. There is no single massive refined ESTC .csv -outputfile, but rather a set of tables linked by unique identifying fields (typically the Cu-Rives number).

## Guidelines
For more detailed instructions, see further down this document. The below buillet points are a summary.

**How do you commit your field processing script(s) and data to the ESTC repositories?**
1. Create a private git repository for your code under https://github.com/COMHIS
2. Make sure your code is in sane state and can be run from start to finish without modifications.
3. Create a README.md -file (Markdown) in the root directory of your code. Have a look at the one in https://github.com/COMHIS/estc-publishers and use that as a template.
4. Commit your code, and if the commit is a finished version create a release also.
5. Also commit the final output data to the https://github.com/COMHIS/estc-data-private -repository and make sure it is documented there as well. https://github.com/COMHIS/estc-data-private/tree/master/estc-publishers can act as an example.
6. Have someone read the readme and see if it is understandable.

## Data repository

Refer [here](./data-instructions.md) for more detailed guidelines on using (both adding data and accessing and referring to it) the [data repository](https://github.com/COMHIS/estc-data-private).

## Data processing scripts

There are multiple and occasionally interdependant scripts that produce the processed field data. These scripts and their repositories are listed [here](data-processing-scripts.md).

Each data processing repository should have a readme laying out the logic of the script(s) and specifying the scripts and datasets that that script depends on.

Outputs from these scripts should be collected in the **data repository** referred to above.

## Data analysis scripts

The various data analysis scripts should be collected [here](./data-analysis-scripts.md) for easy reference.

When creating data analysis scripts, **make sure to take as a starting point a release version of the data** from the data repository.

## Script and data interdependency

The interdependencies of the various parts of the workflow are documentend in [/dependencies](./dependencies).

## TODO
Major parts of the workflow that need updating:
* MARC XML parser rewrite
* Separate data processing and analysis -scripts in the original csv processing script.
