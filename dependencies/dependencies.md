# Dependencies
UML chart of the overall workflow can be found [further down this document](#workflow-image).

Dependencies for various data processing and analysis repositories can initially be collected here. If this file becomes too large, we can split it up by script. 
A dependency entry consists of:
* Script name
* input csv-file names and paths in [csv-data](https://github.com/COMHIS/estc-data-private)
* required input fields from that csv
* output csv-file names in [csv-data](https://github.com/COMHIS/estc-data-private)

Further documentation, such as field names and descriptions of the output data should go in the [data repository](https://github.com/COMHIS/estc-data-private).

## Data processing scripts

### Publishers data processing script
[Publishers -repository](https://github.com/COMHIS/estc-publishers)
* _input csv:_ this_is_not_the_real_path/estc_processed.csv
* _field names:_ Field1, Field2, Field3, ...
* _output csv:_ [TBD/estc_processed.csv](https://github.com/COMHIS/estc-data-private/publishers)

## Data analysis scripts

### This is just a placehold for an analysis script name
What should be here?

## <a name="workflow-image"></a> Overall workflow

![ESTC master workflow](./dependencies.png)
