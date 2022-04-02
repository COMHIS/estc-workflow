# estc-workflow
Documentation for linkages and dependencies in different parts of ESTC processing workflow.

Quick and dirty summary for adding your work to the ESTC workflow can be found below under the header *[Guidelines for data cleaning workflow](#guidelines-for-data-cleaning-workflow)*.

## Overview
Starting point of the ESTC refining and analyzing workflow is the raw XML dump provided by the British Library. This is parsed into "raw" csv format, that is filtered for erroneous entries. [This verified original raw data](https://github.com/COMHIS/estc-data-verified) is then refined in different scripts, and the output of these cleaning and unification scripts make up the "ESTC object model".

Any analysis scripts take as it's starting points one or more of these derived datasets in the [unified ESTC data](https://github.com/COMHIS/estc-data-unified) repository, and combines them as needed. There is no single massive refined ESTC .csv -outputfile, but rather a set of tables linked by unique identifying fields (typically the Cu-RivES number).

## Guidelines for data cleaning workflow
For more detailed instructions, see further down this document. The below buillet points are a summary.

**How do you commit your field processing script(s) and data to the ESTC repositories?**
1. Create a private git repository for your code under https://github.com/COMHIS
2. Make sure your code is in sane state and can be run from start to finish without modifications.
3. Create a README.md -file (Markdown) in the root directory of your code. Have a look at the one in https://github.com/COMHIS/estc-publishers and use that as a template.
4. Commit your code, and if the commit is a finished version create a release also.
5. Also commit the final output data to the https://github.com/COMHIS/estc-data-unified -repository and make sure it is documented there as well. https://github.com/COMHIS/estc-data-unified/tree/master/estc-publishers can act as an example. **No code in the data repository!** Also avoid duplicated and compressed data. See [below](#data-repository) for further instructions.
6. Have someone read the readme and see if it is understandable.

## Data repository

Refer **[here](./data-instructions.md)** for more detailed guidelines on using (both adding data and accessing and referring to it) the data repositories.

## Data processing scripts

There are multiple and occasionally interdependant scripts that produce the processed field data. These scripts and their repositories are listed **[here](data-processing-scripts.md)**. 

Each data processing repository should have a README laying out the logic of the script(s) and specifying the scripts and datasets that that script depends on.

Outputs from these scripts should be collected in the **data repositories** referred to [above](#data-repository).

## Data analysis scripts

The various data analysis scripts should be collected [here](./data-analysis-scripts.md) for easy reference.

When creating data analysis scripts, **make sure to take as a starting point a release version of the data** from the data repository. Each analysis script too should have a README documenting the datasets that are used by that analysis script.

Datasets (summaries, network data, etc.) produced by the data analysis scripts should stay in the same repositories as the scripts themselves. There is no unified repository for the analysis data.

## Script and data interdependency

The interdependencies of the various parts of the workflow are documentend in [/dependencies](./dependencies).
