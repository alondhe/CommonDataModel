The VALID_PERIOD table defines the time period(s) in which the metadata/annotations are valid, which allows for multiple periods of validity (e.g. seasonality)						

Field					|Required	|Type	|Description
:------------------------------|:--------|:------------|:-----------------------------------------
valid_period_id     |Yes      |integer      |A system generated primary key to identify a valid time period for the metadata/annotation.
metadata_id     |No     |integer      |A foreign key to the Metadata table to identify the affected metadata record.
annotation_id     |No     |integer      |A foreign key to the Annotation table to identify the affected annotation record.
reference_id      |No     |integer      |A foreign key to the Reference table to identify the affected reference record.
valid_period_start_datetime     |Yes      |datetime     |A date and time within the data when the metadata or annotation starts being valid.
valid_period_end_datetime     |Yes      |datetime     |A date and time within the data when the metadata or annotation stops being valid.

### Conventions

  * As this table is a one-to-many from the metadata/annotation/reference tables, multiple non-overlapping valid periods can be defined here.
