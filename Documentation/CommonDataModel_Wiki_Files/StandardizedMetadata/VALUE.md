The VALUE table captures values associated with metadata/annotation/reference record(s). Values can be represented in various formats and can be ordered using the value_ordinal field				

Field					|Required	|Type	|Description
:------------------------------|:--------|:------------|:-----------------------------------------
value_id     |Yes     |integer      |A system generated primary key for the value record.
value_ordinal     |No     |integer      |The ordinal value of the record.
metadata_id     |No     |integer      |A foreign key that refers to a metadata record in the Metadata table.
annotation_id     |No     |integer      |A foreign key that refers to an annotation record in the Annotation table.
value_concept_id      |Yes      |integer      |A standard concept that represents the value of the associated metadata/annotation record.
value_type_concept_id     |Yes      |integer      |A standard concept that represents the type of value.
value_as_string     |No     |varchar(1000)      |A string representation of the associated metadata/annotation record, useful for text descriptions.
value_as_number     |No     |float      |A numeric representation of the associated metadata/annotation record, useful for counts or proportions

### Conventions

  * Depending on the value(s) being stored here, use the most type-appropriate representation as possible.
  * Use the value_ordinal field to assign an order to a set of value records.
