# Flow List format

A Flow List is in the form of a csv file with the unique list acronymns as the file name, e.g. 'IDEAv1.csv'.
See the [FlowList template](FlowList.csv).

 Field | Type | Required |  Note |
----------- |  ---- | ---------| -----  |
 FlowName | string | Y | The flow name |
 CASNo | string | N | CAS number |
 Formula | string | N | Chemical formula|
 Synonyms | string | N | Flow synonyms
 Unit | string | Y  | The reference unit. uses [olca-ipc.py](https://github.com/GreenDelta/olca-ipc.py) units |
 Class | string | Y | The flow class, e.g. `Energy` or `Chemical` |
 ExternalReference | string | N | E.g. a web link |
 Preferred | int |  N |   `1` for preferred*, `0` for non-preferred
 Context | string | Y | A path-like set of context compartments e.g. `emission/air`|  
 FlowUUID | string | Y | Unique hexadecimal ID for the flow |
 AltUnit | string | N | Alternate unit for the flow |
 AltUnitConversionFactor | float | N | Conversion factor in the form of alternate units/reference unit |
 SecondCAS | string | N | Secondary CAS numbers if any. If multiple CAS numbers they should be delimited by ";" |
