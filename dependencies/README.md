# Dependencies
UML chart of the overall workflow can be found [further down this document](#overall-workflow).

Dependencies for various data processing and analysis repositories can initially be collected here. If this file becomes too large, we can split it up by script. 
A dependency entry consists of:
* Script name
* input csv-file names and paths in [csv-data](https://github.com/COMHIS/estc-data-private)
* required input fields from that csv
* output csv-file names in [csv-data](https://github.com/COMHIS/estc-data-private)

Further documentation, such as field names and descriptions of the output data should go in the [data repository](https://github.com/COMHIS/estc-data-private).

## Data processing scripts

### Publishers data processing script
* _repository:_ [COMHIS/estc-publishers](https://github.com/COMHIS/estc-publishers)
* _input csv:_ this_is_not_the_real_path/estc_processed.csv
* _field names:_ Field1, Field2, Field3, ...
* _output csv:_ [COMHIS/estc-data-private/estc-publishers](https://github.com/COMHIS/estc-data-private/tree/master/estc-publishers)

### Authors (and other actors) data processing script
* _repository:_ [COMHIS/estc-viaf](https://github.com/COMHIS/estc-viaf)
* _input xml:_ this_is_not_the_real_path/estc.xml (https://github.com/COMHIS/estc-data-private/tree/master/XXXXXXXX)
* _input xml:_ viaf-XXXXX-clusters.xml (http://viaf.org/viaf/data/)
* _output csv:_ [COMHIS/estc-data-private/XXXXX](https://github.com/COMHIS/estc-data-private/tree/master/estc-viaf)

## Data analysis scripts

### This is just a placehold for an analysis script name
What should be here?

## Overall workflow
The UML chart is produced from PlantUML -standard file [dependencies.uml](./dependencies.uml). See [PlantUML](http://plantuml.com/) for details of the file format. The image is built automatically via PlantUML.com server (updates can take up to 10 minutes).<sup>[1](#note1)</sup>

![PlantUML chart](http://www.plantuml.com/plantuml/svg/LSqn3i8m34RXdLF00OXtfaeiC206JX0SGoiIfx9_AzUdZ4nFt_GcHpP4gxl3eboZI5ZTpy3g9oBB8xqNpF4C5-Ek44NYtkXylrsk3n877qUtpwlsGIqxnAZ8Abf4UH7_G_fzferRlm00?max-age=600)
```
A - analysis
D - data
P - data processing
```


### Notes
<a name="note1">1</a>: See ["How to integrate UML diagrams into GitLab or GitHub"](https://stackoverflow.com/questions/32203610/how-to-integrate-uml-diagrams-into-gitlab-or-github) on Stackoverflow for instructions on how to replicate this. 
