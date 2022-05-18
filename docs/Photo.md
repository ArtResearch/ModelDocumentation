# fc:work Reference Data Model

__Author:__ __the name of the author__

__Version:__ __current version__



#### Introduction

The __fc:photo__ semantic annotation refers to the photographs which are shared by the providers and depicts the artworks. 
In this section will be presented all the relationships which are connected to the photographs, as well as the providers of the photographs.






#### Fundamental Relationships 

Fundamental relationships were created for the implementation of the Advanced Search and filtering functionality. Their extensive use was deemed necessary in order to improve the efficiency of the platform. 

|Name|Relationship|Range|Description|
|--|--|--|---|
|consists of|fr:Photo_consists_of_Material|fc:material|This relationship is used to record the artist crated the documented work.|
|created by|fr:Photo_created_by_Photographer|fc:photographer|This relationship is used to record the artist who infulenced the documented work.|
|is held by|fr:Work_created_by_student_of_Artist|fc:artist|This relationship is used to record the teacher of the artist who created the documented work.|
|held by|fr:Photo_has_provider_Institution|fc:institution|This relationship is used to record the institution which kept the documented work.|
|depicts|fr:Photo_depicts_Work|fc:work|This relationship is used to record the provider institution of the documented work.|
|has production|fr:Photo_from_Date|xsd:date|This relationship is used to record a place related to the documented work.|
|produced using|fr:Photo_produced_using_Technique|fc:technique|This relationship is used to record the subject the documented work shows.|
|kept by|fr:Photo_kept_by_Institution|fc:institution|This Relationship is used to record the institution who had kept the photo.|



#### Custom Relationships 

|Name|Relationship|Description|
|--|--|--|
|has provider|custom:has_provider|This relationship is used to indicate the provider of the photo
|has type|custom:has_type| This relationship is used to indicate if the photo is a primary photography and/or photomechanical prints of the documented photography
|recto has sequence|custom:recto_has_sequence|This relationship is used to indicate if the recto view of the photography has a sequence|
|verso has sequence|custom:verso_has_sequence|This relationship is used to indicate if the verso view of the photography has a sequence|
|has original record|custom:has_original_record|This relationship is used to indicate the original records of the documented photography|



#### CRMdig Relationships 

|Name|Relationship|Description|
|--|--|--|
|has thumbnail|crmdig:L58_has_thumbnail|This relationship is used to indicate if the documented phot has a thumbnail image.|
|was digitized by|crmdig:L1i_was_digitized_by|This relationship is used to indicate information related to the digitization of the documented photo



#### Providers

* [I Tatti](http://itatti.harvard.edu/berenson-library/collections/photograph-archives)
* [Zerri](https://fondazionezeri.unibo.it/en/photo-archive/zeri-collection)
* [Frick](https://www.frick.org/research/photoarchive)
* [Malburg](https://www.uni-marburg.de/de/fotomarburg)
* [KHI](https://www.khi.fi.it/index.php)
* [Hertziana](https://www.biblhertz.it/en/photographic-collection/)
* [Paul Mellon Centre for Studies in British Art](https://www.paul-mellon-centre.ac.uk/archives-and-library/photo-archive)



#### Model Section Description

A combination of cidoc crm ontology, fundamental categories and relationships was used in order to achieve the most efficient way for the retrieval of the semantic data. The fields used to describe a photo  can be functionally grouped according to higher level units in order to allow for an easier approach to the navigation of the data by information category. The information categories identified have been enumerated in the following table.

|        #  |   Name             |    Description                                                 |   
|----------:|:-------------------|:---------------------------------------------------------------|
|        1  |Photograph|This information category gathers  together descriptos  used for assigning names,types to a photograph, both at present and  historically.|
|        2  |Photographer|This information category is used to bring together information related to artists and persons related to the documented photograph.|
|        3  |Physical Properties|This information category is used to bring together information related to physical properties of the documented photograph|
|        4  |Provenance|This information category is used to bring together information related to the provenance of the documented photograph.|
|        5  |Subjects|This information category is used to bring together information related to the subject of the documented photograph.|
|        6  |Dating|This information category is used to bring together dates related to the documented photograph.|
|        7  |Notes|This information category is used to bring together notes related to the documented photograph.|



#### Photograph

|Name|Description|Path|
|:--|:---------|:--|
|Identifiers|This field is used to indicate an identifier attributed to the documented instance of the documented photograph.|crm:P1 -> crm:E42|
|Title|This field is used to indicate the preferred identifier attributed to the documented instance of the documented photograph.|crm:P1 -> crm:E42 [1]|
|Title Type|This field is used to indicate the preferred identifier attributed to the documented instance of the documented photograph.|crm:P1 -> crm:E42 [1] -> crm:P2 -> <[http://vocab.getty.edu/aat/300417193](http://vocab.getty.edu/aat/300417193)>| 
|Types|This field is used to indicate the types related to the documented photograph| crm:P2 -> crm:E55 or Authorities Type|
|Photo Archive|This field is used to indicate the institution which provides the documented photograph| fr:Photo_has_provider_Institution -> fc:institution|
|Museum Credit Line|This field is used to document the credit line that should be used in relation to the documented photograph.| crm:P67i -> crm:E73 [1] -> crm:P190|
|Museum Credit Line Type|-| crm:P67i -> crm:E73 [1] -> crm:P2 -> <[http://vocab.getty.edu/aat/300435418](http://vocab.getty.edu/aat/300435418)>|
|Acquisition Timespan|This field is used to indicate the timespan for an ownership period of the documented photograph. | crm:P24i -> crm:E8 -> crm:P4 -> crm:E52 -> crm:P82|
|Acquisition Type|This field is used to indicate the kind of transaction by which a period of ownership was established over the documented photograph. | crm:P24i -> crm:E8 -> crm:P2 -> crm:E55|
|Object Rights Holder|This field is used to indicate the right holder for the documented photograph.| crm:P104 -> crm:E30 -> crm:105\|crm:P75i -> crm:E39|
|Object Rights Type|This field is used to indicate the right holder for the documented photograph.| crm:P104 -> crm:E30 -> crm:P2 -> crm:E55|
|Negative|The negative that was used to produce the documeted photograph.| crm:P128 -> crm:E36 -> crm:P128i -> crm:E22 [1]|
|Negative Type|-| crm:P128 -> crm:E36 -> crm:P128i -> crm:E22 [1] -> crm:P2 -> <[http://vocab.getty.edu/aat/300127173](http://vocab.getty.edu/aat/300127173)>|
|Call Numbers|__?__| crm:P1 -> crm:E42 [1]|
|Call Numbers Type|-| crm:P1 -> crm:E42 [1]-> crm:P2 -> <[http://vocab.getty.edu/aat/300311706](http://vocab.getty.edu/aat/300311706)>|

#### Photographer

|Name|Description|Path|
|:--|:---------|:--|
|Photographer|The Person or Institution that carried out the creation of the documented photograph|fr:Photo_created_by_Photographer -> fc:photographer|




#### Physical Properties

|Name|Description|Path|
|:--|:---------|:--|
|Color Information|This field is used to document a description of the colour of a documented photograph.|crm:P43 -> crm:E54 [1] -> crm:P90|
|Color Information Type|-|crm:P43 -> crm:E54 [1] -> crm:P2 -> <[http://vocab.getty.edu/aat/300127013](http://vocab.getty.edu/aat/300127013)>|
|Dimensions|This field is used to indicate a dimension of an photograph.|crm:P43 -> crm:E54 [2] -> crm:P90 & crm:P91 |
|Dimensions Type|This field is used to indicate a dimension of an photograph.|crm:P43 -> crm:E54 [2] -> crm:P2 -> <[http://vocab.getty.edu/aat/300055644](http://vocab.getty.edu/aat/300055644)>|
|Dimension|This field is used to indicate the dimensions of the photograph (type,unit,value). |	crm:P43 -> crm:E54 -> rdfs:label|
|Technique|This field is used to indicate the specific material / technique used in the production of the documented photograph. |fr:photo_produced_using_Technique -> fc:technique|
|Material|This fields is used to indicate the material that the photograph consists of| crm:P45 -> fc:material  AND  fr:Photo_consists_of_Material  -> fc:material|
|Material Description|This field is used to allow a free text description of the material of which the documented photograph is composed.| crm:P67i -> crm:E73 [2] -> crm:P190|
|State of Preservation|This field is used to indicate the assessed state of preservation - using a specified typology of states - of the documented photograph.|crm:P34i -> crm:E14 -> crm:P35 -> crm:E3 |
|Condition Assessment Description|This field is used to provide a free text description of the conservation status of the documented photograph.|crm:P67i -> crm:E73 [3] -> crm:P190|
|Condition Assessment Description Type|-|crm:P67i -> crm:E73 [3] -> crm:P2 -> <[http://vocab.getty.edu/aat/300435425](http://vocab.getty.edu/aat/300435425)>|
|Equipment|Equipment used for the production of the documented photograph.| crm:P108i -> crm:E12 -> crm:P125 -> crm:E55|

#### Provenance

|Name|Description|Path|
|:--|:---------|:--|
|History of Ownership|This field is used to provide a free text description of a provenance history of the documented photograph.|  crm:P24i -> crm:E8 -> crm:P22\|crm:P23 -> fc:institution|
|History of Ownership Type|-| crm:P67i ->  crm:E73 [1] -> crm:P2 -> <[http://vocab.getty.edu/aat/300055863](http://vocab.getty.edu/aat/300055863)>|
|Acquisition|This field is used to document the acquisition of a documented photograph.| crm:P24i -> crm:E8|



#### Subjects

|Name|Description|Path|
|:--|:---------|:--|
|Subject Description|This field is used to document the subject description of the documented photograph|crm:P67i -> crm:E73 [1] -> crm:P190 |
|Subject Description Type||crm:P67i -> crm:E73 [2] -> crm:P2 -> rdfs:label "Subject Description" |
|Related Artwork|This field is used to document related artoworks to the documented photograph|fr:Photo_depicts_Work -> fc:work |


#### Dating

|Name|Description|Path|
|:--|:---------|:--|
|Production Date Start|-|crm:P108i -> crm:E12 -> crm:P4 -> crm:E52 -> crm:P82a\|crm:P82b\|crm:P80|
|Production Date End|-|crm:P108i -> crm:E12 -> crm:P4 -> crm:E52 -> crm:P82a\|crm:P82b\|crm:P80|
|Production Date|This field is used to indicate the timespan for the creation of the documented work. |crm:P108i -> crm:E12 -> crm:P4 -> crm:E52 -> crm:P82a\|crm:P82b\|crm:P80|
|Shot Place|The place of the shot of the photograph.|crm:P128 -> crm:E36 -> crm:P128i -> crm:E22 -> crm:P108i -> crm:E12 -> crm:P7 ->fc:place|
|Shot Date|The date of the shot of the photograph.|crm:P128 -> crm:E36 -> crm:P128i -> crm:E22 -> crm:P108i -> crm:E12 -> crm:P4 -> crm:E52 -> crm:P82a |




#### Notes

|Name|Description|Path|
|:--|:---------|:--|
|Descriptive Notes|This field is used to document, in free text form, general notes regarding the documented photograph.| crm:P67i -> crm:E73 [1] -> crm:P190
|Descriptive Notes Type|-| crm:P67i -> crm:E73 [1] -> crm:P2 -> <[http://vocab.getty.edu/aat/300435416](http://vocab.getty.edu/aat/300435416)>