# Dependencies

An abtracted UML chart of the overall ESTC cleaning and analysis workflow.

UML chart of the overall workflow can be found [further down this document](#overall-workflow).

Dependencies for various data processing and analysis repositories can initially be collected here. If this file becomes too large, we can split it up by script. 
A dependency entry consists of:
* Script name
* input files and their repository paths.
* required input fields from that csv
* output files and their repository paths.

## Overall workflow
The UML chart is produced from PlantUML -standard file [dependencies.uml](./dependencies.uml). See [PlantUML](http://plantuml.com/) for details of the file format. The image is built automatically via PlantUML.com proxy server.<sup>[1](#note1)</sup>

![PlantUML chart](http://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/COMHIS/estc-workflow/master/dependencies/dependencies.uml&fmt=svg)
?cache=no
```
A - analysis
D - data
P - data processing
```

### Notes
<a name="note1">1</a> See ["How to integrate UML diagrams into GitLab or GitHub"](https://stackoverflow.com/questions/32203610/how-to-integrate-uml-diagrams-into-gitlab-or-github) on Stackoverflow for instructions on how to replicate this. Also see [this post](http://forum.plantuml.net/7163/githubs-aggressive-caching-prevent-diagrams-updated-markdown) on PlantUML forums on how to fix the caching issue.
