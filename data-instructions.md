# Data Repository structure and practices

The data is spread over multiple repositories, depending on it's state:

1) The original data in unmodified XML format as received from the British Library (and converted to `.csv` with no data loss). ([COMHIS/estc-data-originals](https://github.com/COMHIS/estc-data-originals))
2) Above data with erroneous and duplicated entries filtered out, but with no other modifications. This should be the starting point of all the cleanup and unification scripts. ([COMHIS/estc-data-verified](https://github.com/COMHIS/estc-data-verified))
3) The "finished" object model resulting from the cleanup scripts. This is the starting point of all analysis scripts. No code here please, only data! ([COMHIS/estc-data-unified](https://github.com/COMHIS/estc-data-unified))
4) Results of analysis scripts, be they simple summaries and statistical overviews or whatnot should be in their respective repositories.

## Data Repositories

Various data repositories in more detail, with links pointing to them.

### Originals

[COMHIS/estc-data-originals](https://github.com/COMHIS/estc-data-originals)

Original data as received from the British Library. In XML format, and also as csv with no data loss from the XML. 

### Legacy

[COMHIS/estc-data-legacy](https://github.com/COMHIS/estc-data-legacy)

Versions of data that should not be modified further. Kept for legacy compatibility.

### Verified

[COMHIS/estc-data-verified](https://github.com/COMHIS/estc-data-verified)

Original ESTC data with erroneous and duplicated entries separated out. Starting point of clenup and unification scripts.

### Unified

[COMHIS/estc-data-unified](https://github.com/COMHIS/estc-data-unified)

Unified and cleaned ESTC data. Starting point of analysis scripts.

## Structure

* There is a README.md in the root of each repository, and it should be kept up to date with the dataset details.
  * If you add a new dataset to a repository, make sure that the README.md has a link pointing to that dataset and brief description under it.
* Each dataset should be in it’s own subdirectory within the repository.
  * Publisher data, for example, is in https://github.com/COMHIS/estc-data-unfied/tree/master/estc-publishers 
* The data itself should be in .csv format. If the data exceeds Github size limits, use Git LFS.
  * The data fields should only include ones that are unique to that dataset, and a field linking the dataset to the rest of the ESTC data (that reference field would typically be the ESTCid).
  * All datasets and their fields should be documented in directory -specific README.md -files. Look at existing datasets to get a template for this.

## Practices

* Only data in a “finished” state should be committed to the data repository, not intermediate work-in-progress -versions, but rather versions that are ready to be used for analysis and/or further refinement.
  * Each time data is added to the repository or and existing dataset is updated, a new release for the data repository should be created with release notes specifying the data updated.
* References to datasets used in further refining of other datasets, or analysis **should always be to release versions**, not to the master branch. Eg. publisher data in the v0.1.1 release can be found here: https://github.com/COMHIS/estc-data-private/tree/v0.1.1/estc-publishers 
* On each commit, do use useful and informative commit messages.
* Data documentation should be kept up to date, with a dataset specific README.md -file in each data directory.

## Very (/somewhat) large files

* GitHub only accepts individual files of 100MB or less.
* Data that exceeds Github's size limit is stored with Git LFS. To be able to clone that data LFS needs to be installed locally. Refer to [Git LFS tutorial](https://github.com/git-lfs/git-lfs/wiki/Tutorial) for further instructions.
