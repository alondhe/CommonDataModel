The REFERENCE table captures expected thresholds for a specific element of a CDM dataset, which can help provide external benchmarks against datasets similar to it.

Field					|Required	|Type	|Description
:------------------------------|:--------|:------------|:-----------------------------------------
reference_id      |Yes      |integer      |A system generated primary key for the value record.
reference_concept_id      |Yes      |integer      |A standard concept representing the reference being established.
reference_type_concept_id     |Yes      |integer      |A standard concept identifying the reference's type, which provides more granularity about the scope of the reference.
reference_as_string     |No     |varchar(1000)      |A string describing the name of the reference if no concept available.
threshold_concept_id      |Yes      |integer      |A standard concept representing the threshold being used.
threshold_as_string     |No     |varchar(1000)      |A string representing the threshold for this reference record, if no standard concept available.
threshold_minimum_value     |No     |float      |The minimum threshold for the reference.
threshold_maximum_value     |No     |float      |The maximum threshold for the reference.

### Conventions

  * Use the metadata Vocabulary domain to obtain the appropriate reference_concept_id and reference_type_concept_id that represents the external benchmark. 
