# Data Repository structure and practices

The main data repository is located at [github/COMHIS/estc-data-private](https://github.com/COMHIS/estc-data-private).

## Structure

* There is a README.md in the root of the repository, and it should be kept up to date with the dataset details.
  * If you add a new dataset to the repository, make sure that the README.md has a link pointing to that dataset and brief description under it.
* Each dataset should be in it’s own subdirectory within the repository.
  * Publisher data, for example, is in https://github.com/COMHIS/estc-data-private/tree/master/estc-publishers 
* The data itself should be in .csv format, compressed  if necessary (and ideally with bog-standard zip to make access easy).
  * The data fields should only include ones that are unique to that dataset, and a field linking the dataset to the rest of the ESTC data (that reference field would typically be the ESTCid).
  * All datasets and their fields should be documented in directory -specific README.md -files. Look at existing datasets to get a template for this.

## Practices

* Only data in a “finished” state should be committed to the data repository, not intermediate work-in-progress -versions, but rather versions that are ready to be used for analysis and/or further refinement.
  * Each time data is added to the repository or and existing dataset is updated, a new release for the data repository should be created with release notes specifying the data updated.
* References to datasets used in further refining of other datasets, or analysis **should always be to release versions**, not to the master branch. Eg. publisher data in the v0.1.1 release can be found here: https://github.com/COMHIS/estc-data-private/tree/v0.1.1/estc-publishers 
* On each commit, do use useful and informative commit messages.
* Data documentation should be kept up to date, with a dataset specific README.md -file in each data directory.
