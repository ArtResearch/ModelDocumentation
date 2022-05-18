# fc:work Reference Data Model

__Author:__ __the name of the author__

__Version:__ __current version__



#### Introduction

The __fc:work__ semantic annotation refers to the artworks which are shared by the providers. 
In this section will be presented all the relationships which are connected to the artworks, the providers of the artworks and the Authority which was used for the artworks alignment throught the different providers, as well as for the enrichment of the initial data.







#### Fundamental  Relationships 

Fundamental relationships were created for the implementation of the Advanced Search and filtering functionality. Their extensive use was deemed necessary in order to improve the efficiency of the platform. 

|Name|Relationship|Range|Description|
|--|--|--|---|
|created by|fr:Work_created_from_Artist|fc:artist|This relationship is used to record the artist crated the documented work.|
|influenced by|fr:Work_influenced_by_Artist|fc:artist|This relationship is used to record the artist who infulenced the documented work.|
|created by student of|fr:Work_created_by_student_of_Artist|fc:artist|This relationship is used to record the teacher of the artist who created the documented work.|
|held by|fr:Work_kept_by_Institution|fc:institution|This relationship is used to record the institution which kept the documented work.|
|is documented by|fr:Work_has_provider_Institution|fc:institution|This relationship is used to record the provider institution of the documented work.|
|has location|fr:Work_from_Place|fc:place|This relationship is used to record a place related to the documented work.|
|depicts|fr:Work_shows_Subject|fc:subject|This relationship is used to record the subject the documented work shows.|
|depicted by|fr:Work_depicted_by_Photo|fc:photo|This relationship is used to record the photo depicts the documented work.|
|has production|fr:Work_from_Date|xsd:date|This relationship is used to record the start date of the documented work.|
|to|fr:Work_to_Date|xsd:date|This relationship is used to record the end date of the documented work.|
|has modification|fr:Work_has_modification_Date|xsd:date|This relationship is used to record the modification date of the documented work.|
|has destruction|fr:Work_has_destruction_Date|xsd:date|This relationship is used to record the destruction date of the documented work.|
|has acquisition|fr:Work_has_acquisition_Date|xsd:date|This relationship is used to record the acquisition date of the documented work.|
|consists of|fr:Work_consists_of_Material|fc:material|This relationship is used to record materials consists the documented work.|
|produced using|fr:Work_produced_using_technique_Technique|fc:technique|This relationship is used to record the technique which was used for the documented work.|
|photographed by|fr:Work_photographed_by_Photographer|fc:photographer|This relationship is used to record the photographer who photographed the documented work.|



#### Custom Relationships 

|Name|Relationship|Description|
|--|--|--|
|has provider|custom:has_provider|This relationship is used to indicate the provider of the photo
|has type|custom:has_type| This relationship is used to indicate if the photo is a primary photography and/or photomechanical prints of the documented photography



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

A combination of cidoc crm ontology, fundamental categories and relationships was used in order to achieve the most efficient way for the retrieval of the semantic data. The fields used to describe a work can be functionally grouped according to higher level units in order to allow for an easier approach to the navigation of the data by information category. The information categories identified have been enumerated in the following table.

|        #  |   Name             |    Description                                                 |   
|----------:|:-------------------|:---------------------------------------------------------------|
|        1  |Artwork / Monument|This information category gathers  together descriptos  used for assigning names,types to a work, both at present and  historically.|
|        2  |Creator / Attribution|This information category is used to bring together information related to artists and persons related to the documented work.|
|        3  |Physical Properties|This information category is used to bring together information related to physical properties of the documented work|
|        4  |Provenance|This information category is used to bring together information related to the provenance of the documented work.|
|        5  |Subjects|This information category is used to bring together information related to the subject of the documented work.|
|        6  |Dating|This information category is used to bring together dates related to the documented work.|
|        7  |References|This information category is used to bring together references related to the documented work.|



##### Artwork / Monument

|Name|Description|Path|
|:--|:---------|:--|
|Title|This field is used to indicate the title who are attributed to the documented work.|crm:P1 -> E41 [1] -> rdfs:label|
|Title Type|-|crm:P1 -> E41 [1] -> crm:P2 -><[http://vocab.getty.edu/aat/300417193](http://vocab.getty.edu/aat/300417193)>|
|Types|This field is used to indicate the types which are attributed to the documented work.|crm:P2 -> rdfs:label |
|Culture|This field is used to indicate the culture of the documented work.|crm:P108i -> crm:E12 -> crm:P137 -> crm:E55 |
|Museum Credit Line|This field is used to indicate the Museum Credit Line which is attributed to the documented work.|crm:P67i -> crm:E73 -> crm:P190 |
|Museum Credit Line Type|-|crm:P67i -> crm:E73 -> crm:P2 -> <[http://vocab.getty.edu/aat/300435418](http://vocab.getty.edu/aat/300435418)>|
|Inscription|This field is used to indicate the inscription which is attributed to the documented work.|crm:P67i -> crm:E73 -> crm:P190|
|Inscription Type|-|crm:P67i -> crm:E73 -> crm:P2 -> <[http://vocab.getty.edu/aat/300028702](http://vocab.getty.edu/aat/300028702)>|
|Object Rights Holder|This field is used to indicate the rights holder of the documented work.|crm:P104 -> crm:E30 -> crm:P105\|crm:P75i|
|Object Rights Type|This field is used to indicate the type of the rights of the documented work.|crm:P104 -> crm:E30 -> crm:P2 -> crm:E55 |
|Related Works Description|This field is used to indicate the related works of the documented work.|crm:P67i -> crm:E73 [1]|
|Related Works Description Type|-|crm:P67i -> crm:E73 [1] -> crm:P2 -> <[http://vocab.getty.edu/aat/300015640](http://vocab.getty.edu/aat/300015640)>|
|Curational Notes|This field is used to indicate the curational notes of the documented work.|crm:P67i -> crm:P67i -> crm:E73 [2] -> crm:P190 |
|Curational Notes Type|-|crm:P67i -> crm:P67i -> crm:E73 [2] -> crm:P2 -> <[http://vocab.getty.edu/aat/300265639](http://vocab.getty.edu/aat/300265639)>|
|Has Part|This fiels is used to indicate the works which are part of the documented work|crm:P46 -> fc:work|
|Is Part Of|This field is used to indicate the works whose part is the documented work|crm:P46i -> fc:work|
|Last Known Location|this field is used to indicate the last known locations of the documented work|crm:P74_has_current_or_former_residence|crm:P55_has_current_location|
|Last Known Location|-||
|Last Known Location|-||
|Related Objects|This fiels is used to indicate the related objects to the documented work|crm:P67i -> crm:E73[3] -> crm:P70i -> fc:work|
|Related Objects Type|-|crm:P67i -> crm:E73[3] -> crm:P2 -> <[http://vocab.getty.edu/aat/300435412](http://vocab.getty.edu/aat/300435412)>|



##### Creator / Attribution

|Name|Description|Path|
|:--|:---------|:--|
|Creator|This field is used to indicate the artist or creator of the documented work.|fr:Work_created_from_Artist -> fc:artist |
|Production Participant|This field is used to indicate a participant in the creation of the documented work.|crm:P108i -> crm:E12 -> fc:artist|
|Influenced By|This field is used to indicate a form of influence of an actor on the documented work.| fr:Work_influenced_by_Artist -> fc:artist|
|Attribution Notes|This field is used to document a description of an attribution of documented work.|crm:P67i -> crm:E73 [1] -> crm:P190|
|Attribution Notes Type|-|crm:P67i -> crm:E73 [1] -> crm:P2 -> <[http://vocab.getty.edu/aat/300056109](http://vocab.getty.edu/aat/300056109)>|
|Attributions|This field contains information on the attribution of the work to diferrent artists|crm:P108i\|crm:P19i -> crm:E12 -> crm:P140i -> crm:E13|
|Variant Attributions Range|-| crm:P19i -> crm:E7 [1] -> crm:P01i -> crm:PC14 -> crm:P02 -> crm:E21 |
|Variant Attributions Type|-| crm:P19i -> crm:E7 [1] -> crm:P2 -> crm:E55 |
|Variant Attributions Role|-| crm:P19i -> crm:E7 [1] -> crm:P14.1 -> fc:type|
|Variant Attributions|This field contains information on the variant attributions of the work to diferrent artists|concatenation of  Variant Attributions Range, Variant Attributions Type and Variant Attributions Role|



##### Physical Properties

|Name|Description|Path|
|:--|:---------|:--|
|Color Information|This field is used to document a description of the colour of a documented work.|crm:P43 -> crm:E54 [1] -> crm:P90|
|Color Information Type|-|crm:P43 -> crm:E54 [1] -> crm:P2 -> <[http://vocab.getty.edu/aat/300127013](http://vocab.getty.edu/aat/300127013)>|
|Dimensions|This field is used to indicate a dimension of an work.|crm:P43 -> crm:E54 [2] -> crm:P90 & crm:P91 |
|Dimensions Type|This field is used to indicate a dimension of an work.|crm:P43 -> crm:E54 [2] -> crm:P2 -> <[http://vocab.getty.edu/aat/300055644](http://vocab.getty.edu/aat/300055644)>|
|Dimension|This field is used to indicate the dimensions of the work (type,unit,value). |	crm:P43 -> crm:E54 -> rdfs:label|
|Technique|This field is used to indicate the specific material / technique used in the production of the documented work. |fr:Work_produced_using_Technique -> fc:technique|
|Technique Description|This field is used to indicate the description of the specific material / technique used in the production of the documented work. | crm:P67i -> crm:E73 [1]|
|Technique Description Type|-| crm:P67i -> crm:E73 [1] -> crm:P2 -> <https://artresearch.net/resource/khi/type/515FBB66-1F1F-3A94-B64D-8BB7CDA5E8D3>|
|Material|This fields is used to indicate the material that the work consists of| crm:P45 -> fc:material  AND  fr:Work_consists_of_Material  -> fc:material|
|Material Description|This field is used to allow a free text description of the material of which the documented work is composed.| crm:P67i -> crm:E73 [2] -> crm:P190|
|Material Description Type|-| crm:P67i -> crm:E73 [2]-> crm:P2 -> <[http://vocab.getty.edu/aat/300435429](http://vocab.getty.edu/aat/300435429)>|
|State of Preservation|This field is used to indicate the assessed state of preservation - using a specified typology of states - of the documented work.|crm:P34i -> crm:E14 -> crm:P35 -> crm:E3 |
|Condition Assessment Description|This field is used to provide a free text description of the conservation status of the documented work.|crm:P67i -> crm:E73 [3] -> crm:P190|
|Condition Assessment Description Type|-|crm:P67i -> crm:E73 [3] -> crm:P2 -> <[http://vocab.getty.edu/aat/300435425](http://vocab.getty.edu/aat/300435425)>|
|Equipment|Equipment used for the production of the documented work| crm:P108i -> crm:E12 -> crm:P125 -> crm:E55|

##### Provenance

|Name|Description|Path|
|:--|:---------|:--|
|History of Ownership|This field is used to provide a free text description of a provenance history of the documented work.| crm:P67i ->  crm:E73 [1] -> crm:P190   AND  crm:P24i -> crm:E8 -> crm:P22\|crm:P23 -> fc:institution|
|History of Ownership Type|-| crm:P67i ->  crm:E73 [1] -> crm:P2 -> <[http://vocab.getty.edu/aat/300055863](http://vocab.getty.edu/aat/300055863)>|
|Acquisition|This field is used to document the acquisition of a documented work.| crm:P24i -> crm:E8|
|Exhibition|This field is used to document the exhibitons in which the documented work was exhibited.| crm:P12i -> crm:E7 [1]|
|Exhibition Type|-| crm:P12i -> crm:E7 [1] -> crm:P2 -> rdfs:label "Exhibition" |
|Exhibition Description|This field is used to document description of the exhibitons in which the documented work was exhibited.|  crm:P67i -> crm:E73 [2]-> crm:P190 |
|Exhibition Description|-|  crm:P67i -> crm:E73 [2]-> crm:P2 -> <[http://vocab.getty.edu/aat/300435424](http://vocab.getty.edu/aat/300435424)>|



##### Subjects

|Name|Description|Path|
|:--|:---------|:--|
|Subject|This field is used to document the subject of the documented work| fr:Work_shows_Subject -> fc:subject|
|Subject Description|This field is used to document the subject description of the documented work|crm:P67i -> crm:E73 [1] -> crm:P190 |
|Subject Description Type||crm:P67i -> crm:E73 [2] -> crm:P2 -> rdfs:label "Subject Description" |
|Iconclass Information Value|-| crm:P138i -> crm:E36 -> crm:P138 [1]|
|Iconclass Information Type|-| crm:P138i -> crm:E36 -> crm:P138 [1]-> crm:P2 -> crm:E55|
|Iconclass Information|This field is used to include information on Iconclass, such as primary iconography, secondary iconography and keywords| concatenation of Iconclass Information Value and Iconclass Information Type|




##### Dating

|Name|Description|Path|
|:--|:---------|:--|
|Production Date|This field is used to indicate the timespan for the creation of the documented work. |crm:P108i -> crm:E12 -> crm:P4 -> crm:E52 -> crm:P82a\|crm:P82b\|crm:P80|
|Production Date - Century||crm:P4 -> crm:E52 -> crm:P10 -> crm:E52 [1] -> crm:P1 -> crm:E41|
|Production Date - Century Type|-|crm:P4 -> crm:E52 -> crm:P10 -> crm:E52 [1] -> crm:P2 -> crm:E55 "Century"|
|Production Date - Alternative|This field is used to indicate an alternative timespan for the creation of the documented work. | crm:P108i -> crm:E12 -> crm:P4 -> crm:E52 [2] -> crm:P82 |
|Production Date - Alternative Type|| crm:P108i -> crm:E12 -> crm:P4 -> crm:E52 [2] -> crm:P2 -> crm:E55 "Alternative Place"|
|Modification|This field is used to provide information on the Modifications of the documented work.| crm:P30i -> crm:E11|
|Destruction|This field is used to provide information on the Destruction of the documented work.| crm:P13i -> crm:E6 |
|Transformation|This field is used to provide information on the Transformations of the documented work.| crm:P124i -> crm:E81 |
|Dating Value|-|crm:P19i -> crm:E7_Activity -> crm:P4 -> crm:E52 [3] -> crm:P82a|
|Dating Type|-|crm:P19i -> crm:E7_Activity -> crm:P4 -> crm:E52 [3] -> crm:P2 -> crm:E55|
|Dating|This field is used to provide Dates information of the documented work|concatenation of Dating Value and Dating Type|



##### References

|Name|Description|Path|
|:--|:---------|:--|
|Bibliography|This field is used to indicate a bibliographic item which acts as a reference document for the documented work.| crm:P67i -> crm:E73 [1] -> rdfs:label |.
|Bibliography Type|-| crm:P67i -> crm:E73 [1] -> crm:P2 -> <[http://vocab.getty.edu/aat/300435419](http://vocab.getty.edu/aat/300435419)>|
|Sourced Documentation Description|This is a long form description of the documented work. This description is grounded on documentation sources indicated in bracket notation.| crm:P67i -> crm:E73 [2] -> rdfs:label |
|Sourced Documentation Description Type|-| crm:P67i -> crm:E73 [2] -> crm:P2 -> <[http://vocab.getty.edu/aat/300404764](http://vocab.getty.edu/aat/300404764)>|