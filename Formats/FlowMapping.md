# Flow Mapping format

Flow mapping data is in the form of a csv file with the unique source list acronymn, 'to' and the unique target list acronymn as the file name, e.g. 'IDEAv2.2toFEDEFLv1.0.3.csv'.
See the [FlowMapping template](FlowMapping.csv).

Field | Type | Required? | Note |
----- | ---- | --------  | ----------- |
SourceListName | string | Y | Name and version of the source flowlist, e.g. `openLCA1.7` or `TRACI2.1` |
SourceFlowName | string | Y | Name of the source flow |
SourceFlowUUID | string | N | If no UUID present, UUID generated based on olca algorithm|
SourceFlowContext | string | Y | Compartments separated by `/`, like `emission/air`|
SourceUnit | string | Y | A unit abbreviation, like `kg`|
MatchCondition | string | N |Single character. `=`, `>`,`<`,`~`. Meaning 'equal to','a superset of', 'a subset of', 'a proxy for'. Assumes `=` if not present |
ConversionFactor | float | N | Value for multiplying with source flow to equal target flow. Assumes `1` if not   present |
MapType | string | N | MapType token output from Auto mapper tool |
TargetListName | string | Y | Name and version of the target flowlist, e.g. openLCA1.7 or TRACI2.1
TargetFlowName | string | Y | Name of the flowable |
TargetFlowUUID | string| Y| UUID for target flow |
TargetFlowContext | string | Y | Target context, in form like `emission/air` |
TargetUnit | string | Y | A unit abbreviation, like `kg`|
Mapper | string | N | Person creating the mapping |
Verifier | string | N | Person verifying the mapping |
LastUpdated | datetime | N | Date mapping last updated |
Flow Condition (S) | string | N	| FlowName mapping condition Source |
Flow Condition (T) | string | N	| FlowName mapping condition Target |
Flow Conf (S) | string | N	| FlowName mapping confidence rating Source |
Flow Conf (T) | string | N	| FlowName mapping confidence rating Target |
Context Condition (S) | string | N	| Context mapping condition Source |
Context Condition (T) | string | N	| Context mapping condition Target |
Context Conf (S) | string | N	| Context mapping confidence rating Source |
Context Conf (T) | string | N	| Context mapping confidence rating Target |
Conversion Conf (S) | datetime | N | ConversionFactor confidence rating Source |
Conversion Conf (T) | datetime | N | ConversionFactor confidence rating Target |
