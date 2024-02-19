# Person Reference Data Model

__Author:__ __the name of the author__

__Version:__ __current version__

## Introduction

The __fc:person__ semantic annotation refers to the persons which are shared by the Photo Archives and relate to the artists involved in the production of the [works of art](http://vocab.getty.edu/page/aat/300133025) & [built works](http://vocab.getty.edu/page/aat/300265418) that are part of the Artresearch project and is the domain used for the semantic modeling described below.

## Relationships
### Fundamental  Relationships 

Fundamental relationships were created for the implementation of the Structured Search and filtering functionality. Their extensive use was deemed necessary in order to improve the efficiency of the platform. Most of the fundamental relationships have been materialized based on the [Relationships](../Artist.md#enrichment-relationships) of the Authority.

|Name|Relationship|Range|Description|
|--|--|--|---|
|is related to|fr:Person_related_to_Person|fc:artist fc:person|Refers to the person who are related with the documented person.|
|born in|fr:Person_has_Date_of_Birth|xsd:date|Refers to the date of birth of the documented person.|
|died in|fr:Person_has_Date_of_Death|xsd:date|Refers to the date of death of the documented person.|
|born at place|fr:Person_has_Place_of_Birth|fc:place|Refers to the place of birth of the documented person.|
|died at place|fr:Person_has_Place_of_Death|fc:place|Refers to the place of death of the documented person.|
|has gender|fr:Person_has_Gender|fc:gender|Refers to the gender of the documented person.|
|has nationality|fr:Person_has_Nationality|fc:natioality|Refers to the nationality of the documented person.|
|student of|fr:Person_student_of_Person|fc:person|Refers to students of the documented person.|
|child of|fr:Person_child_of_Person|fc:person|Refers to the child of the documented person.|
|parent of|fr:Person_parent_of_Person|fc:person|Refers to the parent of the documented person.|
|sibling of|fr:Person_sibling_of_Person|fc:person|Refers to the sibling of the documented person.|
|assisted by|fr:Person_assisted_by_Person|fc:person|Refers to the person who was assisted by the documented person.|
|partner of|fr:Person_partner_of_Person|fc:person|Refers to the partner of the documented person.|
|spouse of|fr:Person_spouse_of_Person|fc:person|Refers to the spouse of the documented person.|
|teacher of|fr:Person_teacher_of_Person|fc:person|Refers to the teacher of the documented person.|
|apprentice of|fr:Person_apprentice_of_Person|fc:person|Refers to the apprentice of the documented person.|
|collaborated with|fr:Person_collaborated_with_Person|fc:person|Refers to collaborators of the documented person.|
|was apprentice of|fr:Person_was_apprentice_of_Person|fc:person|Refers to the person whose apprentice the documented person was.|
|active at place|fr:Person_active_at_Place|fc:place|Refers to the place where the documented person was active.|
|depicted by|fr:Person_depicted_by|extranle link|Refers to an photo which depicts the documeted person.|
|member of|fr:Person_member_of_Group|fc:group|Refers to the Group of which the documented person is member.|
|active at Place|fr:Person_active_at_Place|fc:place|Refers to the place in which the documented person was active.|
|parent of Person|fr:Person_parent_of_Person|fc:person|Refers to the person whose parent the documented person is.|
|child of Person|fr:Person_child_of_Person|fc:person|Refers to the person whose child the documented person is .|
|influenced Person|fr:Person_influenced_Person|fc:person|Refers to the person who was influenced by the documented person.|
|influenced by Person|fr:Person_influenced_by_Person|fc:person|Refers to the person who influenced the documented person.|
|has Sexual Orientation|fr:Person_has_Sexual_Orientation|wiki data link|Refers to the sexual orientation of the documented person.|
|member of Person|fr:Person_member_of_Person|fc:person|Refers to the Group the documented person is a member.|

### Custom Relationships 

Custom relationships have been used

|Name|Paths|Description|
|----|----|----|
|has provider|custom:has_provider| Referes to the Photo Archive that provided the information of the referenced entity|
|has type|custom:has_type| Referes to the custom type of refrerenced entity|


## Model Section Description

The fields used to describe a person can be functionally grouped according to higher level units in order to allow for an easier approach to the entry and navigation of the data by information category. The information categories identified have been enumerated in the following table.

|        #  |   Name             |    Description                                                 |   
|----------:|:-------------------|:---------------------------------------------------------------|
|        1  |   Person Info      |    This information category gathers  together descriptos  used for assigning names,types to a person, both at present and  historically, as well as descriptors relevant to the tracking of the birth and death of a person |
|        2  |   Person Relationships |  This information category presents information of relationships related to the documented person.|



### Person Info

The attribution of names and types to persons is a basic human activity. A chief factor in disambiguating which person is referred to in historical texts is understanding the various names and identifiers that have been given to an individual at different moments. Likewise, additional classifiers of the individual as such, such as gender, help in the disambiguation, in an information system, of the reference to one real-world individual from another and biographical information, such as their birth and death. 

|Name|Description|Path|
|:--|:---------|:--|
|Identifier|This field is used to indicate an identifier attributed to the documented person.|crm:P1 &rarr; crm:E42 &rarr; rdfs:label|
|Residence/Location|this field is used to indicate the residnce/location attributed to the person| crm:P74 &rarr; rdfs:label|
|Name|This field is used to record the main name attributed to the documented person.|crm:P1 &rarr; crm:E41 &rarr; rdfs:label|
|Name Type|This field is used to indicate a type of a specific part of the name attributed to the documented person.|crm:P1 &rarr; crm:E41 &rarr; crm:P2_has_type &rarr; crm:E55_Type|
|Place of Birth|This field is used to indicate the place of birth of the documented person.|fr:Person_has_Place_of_Birth|
|Place of Death|This field is used to indicate the place of death of the documented person.|fr:Person_has_Place_of_Death|
|Active|This field is used to indicate the period within the documented person was active.| crm:P14i &rarr; crm:F51_Pursuit &rarr; crm:P4 &rarr; crm:E52 &rarr; crm:P82 |
|Active in|This fields is used to indicate where the documented person is active in| crm:P74|crm:P55 &rarr; |
|Institution|This field is used to record the institution to which the documented person is or was memebr of.|crm:P107 &rarr; custom:noType|
|Nationality|This field is used to record the association of the documented person to a national body, usually indicating citizenship.|fr:Person_has_Nationality &rarr; fc:Person|
|Gender|This field is used to record the gender ascribed of the documented person.|fr:Person_has_Gender &rarr; xsd:string|
|Roles|This field is used to record the roles attributed to the documented person.|fr:Person_has_Role|
|Date of Birth|This field is used to record the  date for the birth of the documented person.|fr:Person_has_Date_of_Birth\|fr:Artist_has_Date_of_Birth &rarr; xsd:date|
|Date of Death|This field is used to record the  date for the death of the documented person.|fr:Person_has_Date_of_Death\|fr:Artist_has_Date_of_Death &rarr; xsd:date|
|Partner|This field is used to record the partners attributed to the documented person.|fr:Person_partner_of_Person &rarr; fc:Person|

### Person Relationships

|Name|Description|Path|
|:--|:---------|:--|
|Teachers|This field is used to indicate the theachers who are attributed to the documented person.| fr:Person_student_of_Person\|fr:Person_apprentice_of_Person &rarr; fc:person|
|School Of|This field is used to indicate the person who is school of the dociumented person.|fr:Person_school_of_Person &rarr; fc:person|
|Influenced by|This field is used to indicate the person who influenced the dociumented person.|fr:Person_influenced_by_Person &rarr; fc:person|
|Collaborators|This field is used to indicate Collaborators of the documented person, retrieved from ULAN.|fr:Person_collaborated_with_Person\|fr:Person_assisted_by_Person &rarr; fc:person|
|Students|This field is used to indicate the students of the documented person|fr:Person_teacher_of_Person &rarr; fc:person|
|Influenced|This field is used to indicate the persons which influenced the documented person|fr:Person_influenced_Person &rarr; fc:person|
|Member Of|This field is used to indicate the Person or Group of which the documented person is member of|fr:Person_member_of_Group\|fr:Person_member_of_Person &rarr; fc:person\|fc:group|
|Parents|This field is used to indicate the parents of the documented person |fr:Person_child_of_Person &rarr; fc:person|
|Siblings|This field is used to indicate the siblings of the documented person|fr:Person_sibling_of_Person &rarr; fc:person|
|Partner|This field is used to indicate the partners of the documented person|fr:Person_partner_of_Person &rarr; fc:person|
|Spouse|This fields is used to indicate the spouse of the documented person|fr:Person_spouse_of_Person &rarr; fc:person|
|Children|This field is used to indicate the children of the documented person|fr:Person_parent_of_Person &rarr; fc:person|




