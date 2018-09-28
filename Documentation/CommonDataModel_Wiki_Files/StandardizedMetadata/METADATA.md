The METADATA table contains objective facts about the CDM database or its usage that can be observed through query or obtained from data collectors				

Field					|Required	|Type	|Description
:------------------------------|:--------|:------------|:-----------------------------------------
metadata_id      |Yes      |integer      |A system generated primary key to identify a metadata record.
metadata_concept_id      |Yes      |integer      |A standard concept representing the fact being rendered.
metadata_type_concept_id      |Yes      |integer      |A standard concept identifying the metadata fact's type, which provides more granularity about the scope of the metadata.
metadata_as_string      |No     |varchar(1000)     |A string describing the fact being rendered if no standard concept available.
target_concept_id      |Yes      |integer        |A standard concept identifying the target this metadata will be about.
target_as_string      |No     |varchar(250)     |A string representing the targeted content this metadata will be about, if no concept available.
target_identifier      |No     |integer      |A foreign key to a specific identifier within the CDM.
reference_id     |No     |integer      |A foreign key to the reference table.
security_concept_id      |Yes      |integer      |A standard concept identifying the security access around this metadata record.


### Conventions

  * The metadata_concept_id / metadata_type_concept_id / metadata_as_string fields should represent the actual fact being captured.
  * The target_concept_id / target_as_string / target_identifier fields should represent the specific element of the CDM dataset that the fact is actually about.
    * The target_identifier field can be used to specify a particular ID from the CDM, e.g. a person_id, a cohort_definition_id, a visit_occurrence_id.
  * Use the security_concept_id to tag a sensitivity level about this piece of metadata.
