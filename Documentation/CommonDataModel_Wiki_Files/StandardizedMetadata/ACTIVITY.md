The ACTIVITY table captures the transactional activity of the Metadata schema's usage.

Field					|Required	|Type	|Description
:------------------------------|:--------|:------------|:-----------------------------------------
activity_id     |Yes      |integer      |A system generated primary key to identify an activity.
author_id     |Yes      |varchar(250)     |Either a user name from Shiro, or a foreign key to the author table to identify the author information.
metadata_id     |No     |integer      |A foreign key to the Metadata table to identify the affected metadata record.
annotation_id     |No     |integer      |A foreign key to the Annotation table to identify the affected annotation record.
reference_id      |No     |integer      |A foreign key to the Reference table to identify the affected reference record.
activity_datetime       |Yes      |datetime     |The date and time of the activity.
activity_concept_id     |Yes      |integer      |A standard concept identifying the type of activity being conducted.


### Conventions

  * Any insert/update/delete to the Metadata schema should be tracked in the Activity table and linked to the Author table by author_id.
  * Based on the activity, a link to the Metadata, Annotation, or Reference table could be made.
  * Use the Metadata Vocabulary domain to obtain the appropriate activity_concept_id that describes the action being executed.
