The AUTHOR table captures the creator of the metadata/annotation records.

Field					|Required	|Type	|Description
:------------------------------|:--------|:------------|:-----------------------------------------
author_id     |Yes      |varchar(250)     |A system generated primary key or a foreign key to Shiro (humans only) to identify an author.
author_type_concept_id      |Yes      |integer      |A standard concept identifying the type of author.
author_human_first_name     |No     |varchar(250)     |If a human, the author's first name.
author_human_last_name      |No     |varchar(250)     |If a human, the author's last name.
author_human_suffix     |No     |varchar(100)     |If a human, the author's suffix or degrees.
author_algorithm_name     |No     |varchar(250)     |The name of the algorithm used to generate the metadata or annotation.
author_algorithm_version      |No     |varchar(100)     |The version of the algorithm used to generate the metadata or annotation.
author_description      |No     |varchar(1000)      |A text description about the author's background or qualifications; or, a description of the algorithm's steps.

### Conventions

  * If using WebAPI and Shiro authentication, this table is not utilized to track human authors so as to avoid duplication of author names.
  * Regardless of Shiro availability, all algorithms used to create metadata are to be tracked in this table.
