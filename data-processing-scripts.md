# Data processing scripts

## Summaries

Standard summary document and tables should be generated automatically for each processed field, available in the respective processing folders.

## List script repositories

### Raw MARC XML to CSV parser
The process starts with parsing selected fields from the raw MARC XML to csv format.
* _repository:_ [MARC XML data parsing](https://github.com/COMHIS/MARCdata). 
* _output data:_ [COMHIS/estc-data-private/estc-csv-raw](https://github.com/COMHIS/estc-data-private/tree/master/estc-csv-raw)

### ESTC initial cleanup
* _repository:_ [COMHIS/ESTC](https://github.com/COMHIS/estc)
* _output data:_ [COMHIS/estc-data-private/estc-cleaned-initial](https://github.com/COMHIS/estc-data-private/tree/master/estc-cleaned-initial)

### Publishers data processing script
* _repository:_ [COMHIS/estc-publishers](https://github.com/COMHIS/estc-publishers)
* _output data:_ [COMHIS/estc-data-private/estc-publishers](https://github.com/COMHIS/estc-data-private/tree/master/estc-publishers)

### Authors (and other actors) data processing script
* _repository:_ [COMHIS/estc-viaf](https://github.com/COMHIS/estc-viaf)
* _output data:_ [COMHIS/estc-data-private/estc-viaf](https://github.com/COMHIS/estc-data-private/tree/master/estc-viaf)
