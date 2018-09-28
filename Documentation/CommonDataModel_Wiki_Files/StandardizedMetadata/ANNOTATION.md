The ANNOTATION table for capturing subjective assertions about record(s) in the METADATA table from subject matter experts.				

Field					|Required	|Type	|Description
:------------------------------|:--------|:------------|:-----------------------------------------
annotation_id|      Yes     |integer      |A system generated primary key to identify the annotation record.
metadata_id     |Yes      |integer      |A foreign key that refers to a metadata record in the Metadata table.
annotation_concept_id     |Yes      |integer      |A standard concept identifying the annotation's assertion.
annotation_type_concept_id      |Yes      |integer      |A standard concept identifying the type of the annotation's assertion, which provides more granularity about the scope of the annotation.
security_concept_id     |Yes      |integer      |A standard concept identifying the security access around this annotation record.


### Conventions

  * The Annotation table works in concert with the METADATA table. That is, an annotation cannot exist without a related metadata record.
  * Use the security_concept_id to tag a sensitivity level about this particular annotation.
