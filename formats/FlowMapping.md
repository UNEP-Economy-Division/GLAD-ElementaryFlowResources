# Flow Mapping format

Flow mapping data is in the form of a csv file with the unique source list acronymn, 'to' and the unique target list acronymn as the file name, e.g. 'IDEAv2.2toFEDEFLv1.0.3.csv'.
See the [FlowList template](FlowList.csv).

Field | Type | Required? | Note |
----- | ---- | --------  | ----------- |
SourceListName | string | Y | Name and version of the source flowlist, e.g. `openLCA1.7` or `TRACI2.1` |
SourceFlowName | string | Y | Name of the source flow |
SourceFlowUUID | string | N | If no UUID present, UUID generated based on olca algorithm|
SourceFlowContext | string | Y | Compartments separated by `/`, like `emission/air`|
SourceUnit | string | Y | A unit abbreviation, like `kg`|
MatchCondition | string | N |Single character. `=`, `>`,`<`,`~`. Meaning 'equal to','a superset of', 'a subset of', 'a proxy for'. Assumes `=` if not present |
ConversionFactor | float | N | Value for multiplying with source flow to equal target flow. Assumes `1` if not present |
TargetListName | string | Y | Name and version of the target flowlist, e.g. openLCA1.7 or TRACI2.1
TargetFlowName | string | Y | Name of the Fed Commons flowable |
TargetFlowUUID | string| Y| UUID for Fed Commons flow |
TargetFlowContext | string | Y | Fed commons context, in form like `emission/air` |
TargetUnit | string | Y | A unit abbreviation, like `kg`|
Mapper | string | N | Person creating the mapping |
Verifier | string | N | Person verifying the mapping |
LastUpdated | datetime | N | Date mapping last updated |
MemoMapper | string | N	| Memo by Mapper
MemoVerifier |	string | N | Memo by Verifier
MemoSource | string	| N |	Memo by Source EF system admin
MemoTarget | string	| N	| Memo by Target EF system admin

