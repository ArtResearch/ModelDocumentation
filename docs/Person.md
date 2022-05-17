# fc:person Reference Data Model

__Author:__ __the name of the author__

__Version:__ __current version__


#### Fundamental  Relationships 

Fundamental relationships were created for the implementation of the Advanced Search and filtering functionality. Their extensive use was deemed necessary in order to improve the efficiency of the platform. The fundamental relationships was based on __what ?__ 

|Name|Relationship|Range|Description|
|--|--|--|---|
|is related to|fr:Person_related_to_Person|fc:artist fc:person|This relationship is used to record the person who are related with the documented person.|
|born in|fr:Person_has_Date_of_Birth|xsd:date|This relationship is used to record the date of birth of the documented person.|
|died in|fr:Person_has_Date_of_Death|xsd:date|This relationship is used to record the date of death of the documented person.|
|born at place|fr:Person_has_Place_of_Birth|fc:place|This relationship is used to record the place of birth of the documented person.|
|died at place|fr:Person_has_Place_of_Death|fc:place|This relationship is used to record the place of death of the documented person.|
|has gender|fr:Person_has_Gender|fc:gender|This relationship is used to record the gender of the documented person.|
|has nationality|fr:Person_has_Nationality|fc:natioality|This relationship is used to record the nationality of the documented person.|
|student of|fr:Person_student_of_Person|fc:person|This relationship is used to record students of the documented person.|
|child of|fr:Person_child_of_Person|fc:person|This relationship is used to record the child of the documented person.|
|parent of|fr:Person_parent_of_Person|fc:person|This relationship is used to record the parent of the documented person.|
|sibling of|fr:Person_sibling_of_Person|fc:person|This relationship is used to record the sibling of the documented person.|
|assisted by|fr:Person_assisted_by_Person|fc:person|This relationship is used to record the person who was assisted by the documented person.|
|partner of|fr:Person_partner_of_Person|fc:person|This relationship is used to record the partner of the documented person.|
|spouse of|fr:Person_spouse_of_Person|fc:person|This relationship is used to record the spouse of the documented person.|
|teacher of|fr:Person_teacher_of_Person|fc:person|This relationship is used to record the teacher of the documented person.|
|apprentice of|fr:Person_apprentice_of_Person|fc:person|This relationship is used to record the apprentice of the documented person.|
|collaborated with|fr:Person_collaborated_with_Person|fc:person|This relationship is used to record collaborators of the documented person.|
|was apprentice of|fr:Person_was_apprentice_of_Person|fc:person|This relationship is used to record the person whose apprentice the documented person was.|
|active at place|fr:Person_active_at_Place|fc:place|This relationship is used to record the place where the documented person was active.|
|depicted by|fr:Person_depicted_by|extranle link|this relationship is used to record an photo which depicts the documeted person.|
|member of|fr:Person_member_of_Group|fc:group|This relationship is used to record the Group of which the documented person is member.|
|active at Place|fr:Person_active_at_Place|fc:place|This relationship is used to record the place in which the documented person was active.|
|parent of Person|fr:Person_parent_of_Person|fc:person|This relationship is used to record the person whose parent the documented person is.|
|child of Person|fr:Person_child_of_Person|fc:person|This relationship is used to record the person whose child the documented person is .|
|influenced Person|fr:Person_influenced_Person|fc:person|This relationship is used to record the person who was influenced by the documented person.|
|influenced by Person|fr:Person_influenced_by_Person|fc:person|This relationship is used to record the person who influenced the documented person.|
|has Sexual Orientation|fr:Person_has_Sexual_Orientation|wiki data link|This relationship is used to record the sexual orientation of the documented person.|
|member of Person|fr:Person_member_of_Person|fc:person|This relationship is used to record the Group of persons whose the documented person is member.|



#### custom Relationships 

custom relationships have been used

|Name|Paths|Description|
|----|----|----|
|has provider|custom:has_provider|This relationship is used to recorde the provider of the documented person|
|has type|custom:has_type|This relationship is used to record that the documented type is of type https://artresearch.net/resource/type/pharos.|



#### Providers

* [I Tatti](http://itatti.harvard.edu/berenson-library/collections/photograph-archives)
* [Zerri](https://fondazionezeri.unibo.it/en/photo-archive/zeri-collection)
* [Frick](https://www.frick.org/research/photoarchive)
* [Malburg](https://www.uni-marburg.de/de/fotomarburg)
* [KHI](https://www.khi.fi.it/index.php)
* [Hertziana](https://www.biblhertz.it/en/photographic-collection/)
* [Paul Mellon Centre for Studies in British Art](https://www.paul-mellon-centre.ac.uk/archives-and-library/photo-archive)



#### Model Section Description

The fields used to describe a person can be functionally grouped according to higher level units in order to allow for an easier approach to the entry and navigation of the data by information category. The information categories identified have been enumerated in the following table.

|        #  |   Name             |    Description                                                 |   
|----------:|:-------------------|:---------------------------------------------------------------|
|        1  |   Person Info      |    this information category gathers  together descriptos  used for assigning names,types to a person, both at present and  historically, as well as descriptors relevant to the tracking of the birth and death of a person |
|        2  |   Person Relationships |  This information category is used to bring together information of relationships related to the documented person.|



##### Person Info

The attribution of names and types to persons is a basic human activity. A chief factor in disambiguating which person is referred to in historical texts is understanding the various names and identifiers that have been given to an individual at different moments. Likewise, additional classifiers of the individual as such, such as gender, help in the disambiguation, in an information system, of the reference to one real-world individual from another and biographical information, such as their birth and death. 

|Name|Description|Path|
|:--|:---------|:--|
|Identifier|This field is used to indicate an identifier attributed to the documented person.|crm:P1 -> crm:E42 -> rdfs:label|
|Residence/Location|this field is used to indicate the residnce/location attributed to the person| crm:P74 -> rdfs:label|
|Name|This field is used to record the main name attributed to the documented person.|crm:P1 -> crm:E41 -> rdfs:label|
|Name Type|This field is used to indicate a type of a specific part of the name attributed to the documented person.|crm:P1 -> crm:E41 -> crm:P2_has_type -> crm:E55_Type|
|Place of Birth|This field is used to indicate the place of birth of the documented person.|fr:Person_has_Place_of_Birth|
|Place of Death|This field is used to indicate the place of death of the documented person.|fr:Person_has_Place_of_Death|
|Active|This field is used to indicate the period within the documented person was active.| crm:P14i -> crm:F51_Pursuit -> crm:P4 -> crm:E52 -> crm:P82 |
|Active in|This fields is used to indicate where the documented person is active in| crm:P74|crm:P55 -> |
|Institution|This field is used to record the institution to which the documented person is or was memebr of.|crm:P107 -> custom:noType|
|Nationality|This field is used to record the association of the documented person to a national body, usually indicating citizenship.|fr:Person_has_Nationality -> fc:Person|
|Gender|This field is used to record the gender ascribed of the documented person.|fr:Person_has_Gender -> xsd:string|
|Roles|This field is used to record the roles attributed to the documented person.|fr:Person_has_Role|
|Date of Birth|This field is used to record the  date for the birth of the documented person.|fr:Person_has_Date_of_Birth\|fr:Artist_has_Date_of_Birth -> xsd:date|
|Date of Death|This field is used to record the  date for the death of the documented person.|fr:Person_has_Date_of_Death\|fr:Artist_has_Date_of_Death -> xsd:date|
|Partner|This field is used to record the partners attributed to the documented person.|fr:Person_partner_of_Person -> fc:Person|



##### Person Relationships
|Name|Description|Path|
|:--|:---------|:--|
|Teachers|This field is used to indicate the theachers who are attributed to the documented person.| fr:Person_student_of_Person\|fr:Person_apprentice_of_Person -> fc:person|
|School Of|This field is used to indicate the person who is school of the dociumented person.|fr:Person_school_of_Person -> fc:person|
|Influenced by|This field is used to indicate the person who influenced the dociumented person.|fr:Person_influenced_by_Person -> fc:person|
|Collaborators|This field is used to indicate Collaborators of the documented person, retrieved from ULAN.|fr:Person_collaborated_with_Person\|fr:Person_assisted_by_Person -> fc:person|
|Students|This field is used to indicate the students of the documented person|fr:Person_teacher_of_Person -> fc:person|
|Influenced|This field is used to indicate the persons which influenced the documented person|fr:Person_influenced_Person -> fc:person|
|Member Of|This field is used to indicate the Person or Group of which the documented person is member of|fr:Person_member_of_Group\|fr:Person_member_of_Person -> fc:person\|fc:group|
|Parents|This field is used to indicate the parents of the documented person |fr:Person_child_of_Person -> fc:person|
|Siblings|This field is used to indicate the siblings of the documented person|fr:Person_sibling_of_Person -> fc:person|
|Partner|This field is used to indicate the partners of the documented person|fr:Person_partner_of_Person -> fc:person|
|Spouse|This fields is used to indicate the spouse of the documented person|fr:Person_spouse_of_Person -> fc:person|
|Children|This field is used to indicate the children of the documented person|fr:Person_parent_of_Person -> fc:person|




