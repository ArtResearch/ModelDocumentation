# fc:artist Reference Data Model

__Author:__ __the name of the author__

__Version:__ __current version__



#### Fundamental  Relationships 

Fundamental relationships were created for the implementation of the Advanced Search and filtering functionality. Their extensive use was deemed necessary in order to improve the efficiency of the platform. The fundamental relationships was based on __what ?__ 

|Name|Relationship|Range|Description|
|--|--|--|---|
|Artist_created_Work|fr:Artist_created_Work|fc:work|This relationship is used to record all the works created by the documented artist.|
|Artist_archives_at_Repository|fr:Artist_archives_at_Repository|fc:institution|This relationship is used to record the institution __?__ the documented artist.|
|Artist_has_Copyright_Status|fr:Artist_has_Copyright_Status|fc:copyright_status|This relationship is used to record the copyright status related with the documented artist.|
|Artist_influenced_creation_of_Work|fr:Artist_influenced_creation_of_Work|fc:work|This relationship is used to record the works influenced by the documented artist.|
|Artist_influenced_Artist|fr:Artist_influenced_Artist|fc:artist|This relationship is used to record the artists who were influenced by the documented artist.|
|Artist_from_Place|fr:Artist_from_Place|fc:place|This relationship is used to record the place of origin of the documented artist.|



#### custom Relationships 

custom relationships have been used

|Name|Paths|Description|
|----|----|----|
|has provider|custom:has_provider|This relationship is used to recorde the provider of the documented artist|
|has type|custom:has_type|This relationship is used to record that the documented type is of type https://artresearch.net/resource/type/pharos.|



#### ULAN Relationships 

Ulan relationships have been used

|Name|RelationShip|
|----|----|
|agent Type non Preferred|[agentTypeNonPreferred](http://vocab.getty.edu/ontology#agentTypeNonPreferred)|
|studen of|[ulan1102_student_of](http://vocab.getty.edu/ontology#ulan1102_student_of)|
|related to|[ulan1500_related_to](http://vocab.getty.edu/ontology#ulan1500_related_to)|
|employee of|[ulan1217_employee_of](http://vocab.getty.edu/ontology#ulan1217_employee_of)|
|parent of|[ulan1512_parent_of](http://vocab.getty.edu/ontology#ulan1512_parent_of)|
|distinguished from|[ulan1007_distinguished_from](http://vocab.getty.edu/ontology#ulan1007_distinguished_from)|
|student of|[ulan1102_student_of](http://vocab.getty.edu/ontology#ulan1102_student_of)|
|employee of|[ulan1217_employee_of](http://vocab.getty.edu/ontology#ulan1217_employee_of)|
|parent of|[ulan1512_parent_of](http://vocab.getty.edu/ontology#ulan1512_parent_of)|
|memebr of|[ulan1317_member_of](http://vocab.getty.edu/ontology#ulan1317_member_of)|
|child of|[ulan1511_child_of](http://vocab.getty.edu/ontology#ulan1511_child_of)|
|nephew or niece of|[ulan1531_nephew-niece_of](http://vocab.getty.edu/ontology#ulan1531_nephew-niece_of)|
|grandchild of|[ulan1513_grandchild_of](http://vocab.getty.edu/ontology#ulan1513_grandchild_of)|
|great or grandchild of|[ulan1516_great-grandchild_of](http://vocab.getty.edu/ontology#ulan1516_great-grandchild_of)|
|patron was|[ulan1202_patron_was](http://vocab.getty.edu/ontology#ulan1202_patron_was)|
|influenced|[ulan1107_influenced](http://vocab.getty.edu/ontology#ulan1107_influenced)|
|formerly indentified with|[ulan1006_formerly_identified_with](http://vocab.getty.edu/ontology#ulan1006_formerly_identified_with)|
|teacher of|[ulan1101_teacher_of](http://vocab.getty.edu/ontology#ulan1101_teacher_of)|
|apprentice was|[ulan1106_apprentice_was](http://vocab.getty.edu/ontology#ulan1106_apprentice_was)|
|sibling of|[ulan1501_sibling_of](http://vocab.getty.edu/ontology#ulan1501_sibling_of)|
|collaborated with|[ulan1303_collaborated_with](http://vocab.getty.edu/ontology#ulan1303_collaborated_with)|
|founder of|[ulan2572_founder_of](http://vocab.getty.edu/ontology#ulan2572_founder_of)|
|partner of|[ulan1311_partner_of](http://vocab.getty.edu/ontology#ulan1311_partner_of)|
|gandparent of|[ulan1514_gandparent_of](http://vocab.getty.edu/ontology#ulan1514_gandparent_of)|
|uncle or aunt of|[ulan1532_uncle-aunt_of](http://vocab.getty.edu/ontology#ulan1532_uncle-aunt_of)|
|related to|[ulan1000_related_to](http://vocab.getty.edu/ontology#ulan1000_related_to)|
|cousin of|[ulan1521_cousin_of](http://vocab.getty.edu/ontology#ulan1521_cousin_of)|
|parent by marriage of|[ulan1552_parent_by_marriage_of](http://vocab.getty.edu/ontology#ulan1552_parent_by_marriage_of)|
|subling by marriage of|[ulan1551_sibling_by_marriage_of](http://vocab.getty.edu/ontology#ulan1551_sibling_by_marriage_of)|
|assisted by|[ulan1308_assisted_by](http://vocab.getty.edu/ontology#ulan1308_assisted_by)|
|influenced by|[ulan1108_influenced_by](http://vocab.getty.edu/ontology#ulan1108_influenced_by)|
|apprentice of|[ulan1105_apprentice_of](http://vocab.getty.edu/ontology#ulan1105_apprentice_of)|
|employee was|[ulan1218_employee_was](http://vocab.getty.edu/ontology#ulan1218_employee_was)|
|spouse of|[ulan1541_spouse_of](http://vocab.getty.edu/ontology#ulan1541_spouse_of)|
|colleague of|[ulan1301_colleague_of](http://vocab.getty.edu/ontology#ulan1301_colleague_of)|
|worked with|[ulan1305_worked_with](http://vocab.getty.edu/ontology#ulan1305_worked_with)|
|great or grandparent of|[ulan1515_great-grandparent_of](http://vocab.getty.edu/ontology#ulan1515_great-grandparent_of)|
|assistant of|[ulan1307_assistant_of](http://vocab.getty.edu/ontology#ulan1307_assistant_of)|
|possibly identified with|[ulan1005_possibly_identified_with](http://vocab.getty.edu/ontology#ulan1005_possibly_identified_with)|
|estEnd|[estEnd](http://vocab.getty.edu/ontology#estEnd)|
|friend of|[ulan2550_friend_of](http://vocab.getty.edu/ontology#ulan2550_friend_of)|
|step or child of|[ulan1561_step-child_of](http://vocab.getty.edu/ontology#ulan1561_step-child_of)|
|broaderNonConcept|[broaderNonConcept](http://vocab.getty.edu/ontology#broaderNonConcept)|
|broaderPartitive|[broaderPartitive](http://vocab.getty.edu/ontology#broaderPartitive)|
|broaderPartitiveExtended|[broaderPartitiveExtended](http://vocab.getty.edu/ontology#broaderPartitiveExtended)|
|associate of|[ulan1302_associate_of](http://vocab.getty.edu/ontology#ulan1302_associate_of)|
|teacher at|[ulan2676_teacher_at](http://vocab.getty.edu/ontology#ulan2676_teacher_at)|
|court artist_to|[ulan1213_court_artist_to](http://vocab.getty.edu/ontology#ulan1213_court_artist_to)|
|professor at|[ulan2674_professor_at](http://vocab.getty.edu/ontology#ulan2674_professor_at)|
|step-parent of|[ulan1562_step-parent_of](http://vocab.getty.edu/ontology#ulan1562_step-parent_of)|
|master of|[ulan1111_master_of](http://vocab.getty.edu/ontology#ulan1111_master_of)|
|child by marriage of|[ulan1553_child_by_marriage_of](http://vocab.getty.edu/ontology#ulan1553_child_by_marriage_of)|
|worked_with|[ulan1331_worked_with](http://vocab.getty.edu/ontology#ulan1331_worked_with)|
|member_was|[ulan1318_member_was](http://vocab.getty.edu/ontology#ulan1318_member_was)|
|ancestor_of|[ulan1582_ancestor_of](http://vocab.getty.edu/ontology#ulan1582_ancestor_of)|
|partner_in|[ulan1313_partner_in](http://vocab.getty.edu/ontology#ulan1313_partner_in)|
|associated_with|[ulan1003_associated_with](http://vocab.getty.edu/ontology#ulan1003_associated_with)|
|romantic_partner_of|[ulan1547_romantic_partner_of](http://vocab.getty.edu/ontology#ulan1547_romantic_partner_of)|
|master was|[ulan1112_master_was](http://vocab.getty.edu/ontology#ulan1112_master_was)|
|relative by marriage|[ulan1550_relative_by_marriage](http://vocab.getty.edu/ontology#ulan1550_relative_by_marriage)|
|patron of|[ulan1201_patron_of](http://vocab.getty.edu/ontology#ulan1201_patron_of)|
|professor was|[ulan2675_professor_was](http://vocab.getty.edu/ontology#ulan2675_professor_was)|
|fellow student of|[ulan1113_fellow_student_of](http://vocab.getty.edu/ontology#ulan1113_fellow_student_of)|
|donor of|[ulan1203_donor_of](http://vocab.getty.edu/ontology#ulan1203_donor_of)|
|school was|[ulan1322_school_was](http://vocab.getty.edu/ontology#ulan1322_school_was)|
|broaderNonPreferred|[broaderNonPreferred](http://vocab.getty.edu/ontology#broaderNonPreferred)|
|principal in|[ulan1315_principal_in](http://vocab.getty.edu/ontology#ulan1315_principal_in)|
|adoptive parent of|[ulan1554_adoptive_parent_of](http://vocab.getty.edu/ontology#ulan1554_adoptive_parent_of)|
|consort of|[ulan1542_consort_of](http://vocab.getty.edu/ontology#ulan1542_consort_of)|
|president of|[ulan2692_president_of](http://vocab.getty.edu/ontology#ulan2692_president_of)|
|guardian of|[ulan1571_guardian_of](http://vocab.getty.edu/ontology#ulan1571_guardian_of)|
|performs with|[ulan1306_performs_with](http://vocab.getty.edu/ontology#ulan1306_performs_with)|
|dedicatee of|[ulan2781_dedicatee_of](http://vocab.getty.edu/ontology#ulan2781_dedicatee_of)|
|successor of|[ulan1411_successor_of](http://vocab.getty.edu/ontology#ulan1411_successor_of)|
|predecessor of|[ulan1412_predecessor_of](http://vocab.getty.edu/ontology#ulan1412_predecessor_of)|
|student at|[ulan2828_student_at](http://vocab.getty.edu/ontology#ulan2828_student_at)|
|director of|[ulan2574_director_of](http://vocab.getty.edu/ontology#ulan2574_director_of)|
|half-sibling of|[ulan1556_half-sibling_of](http://vocab.getty.edu/ontology#ulan1556_half-sibling_of)|
|broaderGeneric|[broaderGeneric](http://vocab.getty.edu/ontology#broaderGeneric)|
|broaderGenericExtended|[broaderGenericExtended](http://vocab.getty.edu/ontology#broaderGenericExtended)|
|client of|[ulan1205_client_of](http://vocab.getty.edu/ontology#ulan1205_client_of)|
|possibly related to|[ulan1590_possibly_related_to](http://vocab.getty.edu/ontology#ulan1590_possibly_related_to)|
|client was|[ulan1206_client_was](http://vocab.getty.edu/ontology#ulan1206_client_was)|
|owned by|[ulan2779_owned_by](http://vocab.getty.edu/ontology#ulan2779_owned_by)|
|leader of|[ulan2696_leader_of](http://vocab.getty.edu/ontology#ulan2696_leader_of)|
|school of|[ulan1321_school_of](http://vocab.getty.edu/ontology#ulan1321_school_of)|
|artist to|[ulan1211_artist_to](http://vocab.getty.edu/ontology#ulan1211_artist_to)|
|owner of|[ulan2778_owner_of](http://vocab.getty.edu/ontology#ulan2778_owner_of)|
|descendant of|[ulan1581_descendant_of](http://vocab.getty.edu/ontology#ulan1581_descendant_of)|
|adopted child of|[ulan1555_adopted_child_of](http://vocab.getty.edu/ontology#ulan1555_adopted_child_of)|
|representative of|[ulan2794_representative_of](http://vocab.getty.edu/ontology#ulan2794_representative_of)|
|godparent of|[ulan1574_godparent_of](http://vocab.getty.edu/ontology#ulan1574_godparent_of)|
|worker was|[ulan1332_worker_was](http://vocab.getty.edu/ontology#ulan1332_worker_was)|
|representative was|[ulan2795_representative_was](http://vocab.getty.edu/ontology#ulan2795_representative_was)|
|teacher was|[ulan2677_teacher_was](http://vocab.getty.edu/ontology#ulan2677_teacher_was)|
|partner was|[ulan1314_partner_was](http://vocab.getty.edu/ontology#ulan1314_partner_was)|
|ward of|[ulan1573_ward_of](http://vocab.getty.edu/ontology#ulan1573_ward_of)|
|significant other of|[ulan1544_significant_other_of](http://vocab.getty.edu/ontology#ulan1544_significant_other_of)|
|court artist was|[ulan1214_court_artist_was](http://vocab.getty.edu/ontology#ulan1214_court_artist_was)|
|publisher was|[ulan2650_publisher_was](http://vocab.getty.edu/ontology#ulan2650_publisher_was)|
|advisor of|[ulan1309_advisor_of](http://vocab.getty.edu/ontology#ulan1309_advisor_of)|
|meaning-usage overlaps with|[ulan1008_meaning_-usage_overlaps_with](http://vocab.getty.edu/ontology#ulan1008_meaning_-usage_overlaps_with)|
|consort was|[ulan1543_consort_was](http://vocab.getty.edu/ontology#ulan1543_consort_was)|
|step-sibling of|[ulan1557_step-sibling_of](http://vocab.getty.edu/ontology#ulan1557_step-sibling_of)|



#### Skos Relationships 

Skos relationships have been used

|Name|RelationShip|
|----|----|
|alternative label|[altLabel](http://www.w3.org/2004/02/skos/core#altLabel)|
|change Note|[changeNote](http://www.w3.org/2004/02/skos/core#changeNote)|
|note|[note](http://www.w3.org/2004/02/skos/core#note)|
|scopeNote|[scopeNote](http://www.w3.org/2004/02/skos/core#scopeNote)|
|preferable Label|[prefLabel](http://www.w3.org/2004/02/skos/core#prefLabel)|
|is in mapping relation with|[mappingRelation](http://www.w3.org/2004/02/skos/core#mappingRelation)|
|has close match|[closeMatch](http://www.w3.org/2004/02/skos/core#closeMatch)|
|has exact match|[exactMatch](http://www.w3.org/2004/02/skos/core#exactMatch)|
|related|[related](http://www.w3.org/2004/02/skos/core#related)|
|narrower|[narrower](http://www.w3.org/2004/02/skos/core#narrower)|
|broader|[broader](http://www.w3.org/2004/02/skos/core#broader)|
|broaderTransitive|[broaderTransitive](http://www.w3.org/2004/02/skos/core#broaderTransitive)
|member|[member](http://www.w3.org/2004/02/skos/core#member)



#### Authorities

* [ULAN](http://www.getty.edu/research/tools/vocabularies/ulan/)
* [WIKIDATA](https://www.wikidata.org/wiki/Wikidata:Main_Page)



#### Providers

* [I Tatti](http://itatti.harvard.edu/berenson-library/collections/photograph-archives)
* [Zerri](https://fondazionezeri.unibo.it/en/photo-archive/zeri-collection)
* [Frick](https://www.frick.org/research/photoarchive)
* [Malburg](https://www.uni-marburg.de/de/fotomarburg)
* [KHI](https://www.khi.fi.it/index.php)
* [Hertziana](https://www.biblhertz.it/en/photographic-collection/)
* [Paul Mellon Centre for Studies in British Art](https://www.paul-mellon-centre.ac.uk/archives-and-library/photo-archive)



#### Model Section Description

The categories which are used for the representation of the information related to an artist are the same with those of persons.

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







