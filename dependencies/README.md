# Dependencies
<<<<<<< HEAD
An abtracted UML chart of the overall ESTC cleaning and analysis workflow.
=======
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

### Document dimension data processing script
* _repository:_ [COMHIS/estc-physical-dimension](https://github.com/COMHIS/estc-physical-dimension)
* _input xml:_ Aalto/estc/originals/MARC/estc.xml (estc.xml)
* _output csv:_ [COMHIS/estc-data-private/estc-physicaldimension](https://github.com/COMHIS/estc-data-private/tree/master/estc-physicaldimension)


## Data analysis scripts

### This is just a placehold for an analysis script name

TBA
>>>>>>> 1dc9d16e0040326bcc7f2ab0111728dc667279bb

## Overall workflow
The UML chart is produced from PlantUML -standard file [dependencies.uml](./dependencies.uml). See [PlantUML](http://plantuml.com/) for details of the file format. The image is built automatically via PlantUML.com proxy server.<sup>[1](#note1)</sup>

![PlantUML chart](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/COMHIS/estc-workflow/master/dependencies/dependencies.uml&fmt=svg)
```
A - analysis
D - data
P - data processing
```

### Notes
<a name="note1">1</a> See ["How to integrate UML diagrams into GitLab or GitHub"](https://stackoverflow.com/questions/32203610/how-to-integrate-uml-diagrams-into-gitlab-or-github) on Stackoverflow for instructions on how to replicate this. Also see [this post](http://forum.plantuml.net/7163/githubs-aggressive-caching-prevent-diagrams-updated-markdown) on PlantUML forums on how to fix the caching issue.
