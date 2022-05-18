# Photograph Reference Data Model

__Author:__ __the name of the author__

__Version:__ __current version__



## Introduction

The __fc:photo__ semantic annotation refers to the photographs which are shared by the Photo Archives and depict the [works of art](http://vocab.getty.edu/page/aat/300133025) & [built works](http://vocab.getty.edu/page/aat/300265418) that are part of the Artresearch project and is the domain used for the semantic modeling described below.

## Relationships

### Fundamental Relationships 

Fundamental relationships were created for the implementation of the Contextual Search and filtering functionality. Their use was deemed necessary in order to improve the efficiency of the platform. 

|Name|Relationship|Range|Description|
|--|--|--|---|
|consists of|fr:Photo_consists_of_Material|fc:material|Referes to record the artist crated the documented work.|
|created by|fr:Photo_created_by_Photographer|fc:photographer|Referes to record the artist who infulenced the documented work.|
|is held by|fr:Work_created_by_student_of_Artist|fc:artist|Referes to record the teacher of the artist who created the documented work.|
|held by|fr:Photo_has_provider_Institution|fc:institution|Referes to record the institution which kept the documented work.|
|depicts|fr:Photo_depicts_Work|fc:work|Referes to record the provider institution of the documented work.|
|has production|fr:Photo_from_Date|xsd:date|Referes to record a place related to the documented work.|
|produced using|fr:Photo_produced_using_Technique|fc:technique|Referes to record the subject the documented work shows.|
|kept by|fr:Photo_kept_by_Institution|fc:institution|Referes to record the institution who had kept the photo.|



### Custom Relationships 

|Name|Relationship|Description|
|--|--|--|
|has provider|custom:has_provider| Referes to the Photo Archive that provided the information of the referenced entity|
|has type|custom:has_type| Referes to the custom type of refrerenced entity|
|recto has sequence|custom:recto_has_sequence| Refers to the sequence of the recto view of the photograph|
|verso has sequence|custom:verso_has_sequence| Refers to the sequence of the verso view of the photograph|
|has original record|custom:has_original_record| Refers to the original records of the documented photograph|


### CRMdig Relationships 

|Name|Relationship|Description|
|--|--|--|
|has thumbnail|crmdig:L58_has_thumbnail|This relationship is used to indicate if the documented photograph has a thumbnail image.|
|was digitized by|crmdig:L1i_was_digitized_by|This relationship is used to indicate information related to the digitization of the documented photo|


## Model Section Description

A combination of cidoc crm ontology, fundamental categories and relationships was used in order to achieve the most efficient way for the retrieval of the semantic data. The fields used to describe a photo  can be functionally grouped according to higher level units in order to allow for an easier approach to the navigation of the data by information category. The information categories identified have been enumerated in the following table.

|        #  |   Name             |    Description                                                 |   
|----------:|:-------------------|:---------------------------------------------------------------|
|        1  |Photograph|This information category gathers  together descriptos  used for assigning names,types to a photograph, both at present and  historically|
|        2  |Photographer|This information category presents information related to artists and persons related to the documented photograph|
|        3  |Physical Properties|This information category presents information related to physical properties of the documented photograph|
|        4  |Provenance|This information category presents information related to the provenance of the documented photograph.|
|        5  |Subjects|This information category presents information related to the subject of the documented photograph.|
|        6  |Dating|This information category presents dates related to the documented photograph.|
|        7  |Notes|This information category presents notes related to the documented photograph.|



### Photograph

|Name|Description|Path|
|:--|:---------|:--|
|Identifiers|This field is used to indicate an identifier attributed to the documented instance of the documented photograph.|crm:P1 &rarr; crm:E42|
|Title|This field is used to indicate the preferred identifier attributed to the documented instance of the documented photograph.|crm:P1 &rarr; crm:E42 [1]|
|Title Type|This field is used to indicate the preferred identifier attributed to the documented instance of the documented photograph.|crm:P1 &rarr; crm:E42 [1] &rarr; crm:P2 &rarr; [titles (general, names)](http://vocab.getty.edu/aat/300417193)| 
|Types|This field is used to indicate the types related to the documented photograph| crm:P2 &rarr; crm:E55 or Authorities Type|
|Photo Archive|This field is used to indicate the institution which provides the documented photograph| fr:Photo_has_provider_Institution &rarr; fc:institution|
|Museum Credit Line|This field is used to document the credit line that should be used in relation to the documented photograph.| crm:P67i &rarr; crm:E73 [1] &rarr; crm:P190|
|Museum Credit Line Type|-| crm:P67i &rarr; crm:E73 [1] &rarr; crm:P2 &rarr; [credit line](http://vocab.getty.edu/aat/300435418)|
|Acquisition Timespan|This field is used to indicate the timespan for an ownership period of the documented photograph. | crm:P24i &rarr; crm:E8 &rarr; crm:P4 &rarr; crm:E52 &rarr; crm:P82|
|Acquisition Type|This field is used to indicate the kind of transaction by which a period of ownership was established over the documented photograph. | crm:P24i &rarr; crm:E8 &rarr; crm:P2 &rarr; crm:E55|
|Object Rights Holder|This field is used to indicate the right holder for the documented photograph.| crm:P104 &rarr; crm:E30 &rarr; crm:105\|crm:P75i &rarr; crm:E39|
|Object Rights Type|This field is used to indicate the right holder for the documented photograph.| crm:P104 &rarr; crm:E30 &rarr; crm:P2 &rarr; crm:E55|
|Negative|The negative that was used to produce the documeted photograph.| crm:P128 &rarr; crm:E36 &rarr; crm:P128i &rarr; crm:E22 [1]|
|Negative Type|-| crm:P128 &rarr; crm:E36 &rarr; crm:P128i &rarr; crm:E22 [1] &rarr; crm:P2 &rarr; [negatives (photographs)](http://vocab.getty.edu/aat/300127173)|
|Call Numbers| A call number indicates the address/location of the photograph in the archive.| crm:P1 &rarr; crm:E42 [1]|
|Call Numbers Type|-| crm:P1 &rarr; crm:E42 [1]&rarr; crm:P2 &rarr; [call numbers](http://vocab.getty.edu/aat/300311706)|

### Photographer

|Name|Description|Path|
|:--|:---------|:--|
|Photographer|The Person or Institution that carried out the creation of the documented photograph|fr:Photo_created_by_Photographer &rarr; fc:photographer|

### Physical Properties

|Name|Description|Path|
|:--|:---------|:--|
|Color Information|This field is used to document a description of the colour of a documented photograph.|crm:P43 &rarr; crm:E54 [1] &rarr; crm:P90|
|Color Information Type|-|crm:P43 &rarr; crm:E54 [1] &rarr; crm:P2 &rarr; [<photographs by form: color\>](http://vocab.getty.edu/aat/300127013)|
|Dimensions|This field is used to indicate a dimension of an photograph.|crm:P43 &rarr; crm:E54 [2] &rarr; crm:P90 & crm:P91 |
|Dimensions Type|This field is used to indicate a dimension of an photograph.|crm:P43 &rarr; crm:E54 [2] &rarr; crm:P2 &rarr; E55_Type|
|Dimension|This field is used to indicate the dimensions of the photograph (type,unit,value). |	crm:P43 &rarr; crm:E54 &rarr; rdfs:label|
|Technique|This field is used to indicate the specific material / technique used in the production of the documented photograph. |fr:photo_produced_using_Technique &rarr; fc:technique|
|Material|This fields is used to indicate the material that the photograph consists of| crm:P45 &rarr; fc:material  AND  fr:Photo_consists_of_Material  &rarr; fc:material|
|Material Description|This field is used to allow a free text description of the material of which the documented photograph is composed.| crm:P67i &rarr; crm:E73 [2] &rarr; crm:P190|
|State of Preservation|This field is used to indicate the assessed state of preservation - using a specified typology of states - of the documented photograph.|crm:P34i &rarr; crm:E14 &rarr; crm:P35 &rarr; crm:E3 |
|Condition Assessment Description|This field is used to provide a free text description of the conservation status of the documented photograph.|crm:P67i &rarr; crm:E73 [3] &rarr; crm:P190|
|Condition Assessment Description Type|-|crm:P67i &rarr; crm:E73 [3] &rarr; crm:P2 &rarr; [condition/examination description](http://vocab.getty.edu/aat/300435425)|
|Equipment|Equipment used for the production of the documented photograph.| crm:P108i &rarr; crm:E12 &rarr; crm:P125 &rarr; crm:E55|

### Provenance

|Name|Description|Path|
|:--|:---------|:--|
|History of Ownership|This field is used to provide a free text description of a provenance history of the documented photograph.|  crm:P24i &rarr; crm:E8 &rarr; crm:P22\|crm:P23 &rarr; fc:institution|
|History of Ownership Type|-| crm:P67i &rarr;  crm:E73 [1] &rarr; crm:P2 &rarr; [provenance (history of ownership)](http://vocab.getty.edu/aat/300055863)|
|Acquisition|This field is used to document the acquisition of a documented photograph.| crm:P24i &rarr; crm:E8|



### Subjects

|Name|Description|Path|
|:--|:---------|:--|
|Subject Description|This field is used to document the subject description of the documented photograph|crm:P67i &rarr; crm:E73 [1] &rarr; crm:P190 |
|Subject Description Type|-|crm:P67i &rarr; crm:E73 [2] &rarr; crm:P2 &rarr; rdfs:label "Subject Description" |
|Related Artwork|This field is used to document related artoworks to the documented photograph|fr:Photo_depicts_Work &rarr; fc:work |


### Dating

|Name|Description|Path|
|:--|:---------|:--|
|Production Date Start|-|crm:P108i &rarr; crm:E12 &rarr; crm:P4 &rarr; crm:E52 &rarr; crm:P82a\|crm:P82b\|crm:P80|
|Production Date End|-|crm:P108i &rarr; crm:E12 &rarr; crm:P4 &rarr; crm:E52 &rarr; crm:P82a\|crm:P82b\|crm:P80|
|Production Date|This field is used to indicate the timespan for the creation of the documented work. |crm:P108i &rarr; crm:E12 &rarr; crm:P4 &rarr; crm:E52 &rarr; crm:P82a\|crm:P82b\|crm:P80|
|Shot Place|The place of the shot of the photograph.|crm:P128 &rarr; crm:E36 &rarr; crm:P128i &rarr; crm:E22 &rarr; crm:P108i &rarr; crm:E12 &rarr; crm:P7 &rarr;fc:place|
|Shot Date|The date of the shot of the photograph.|crm:P128 &rarr; crm:E36 &rarr; crm:P128i &rarr; crm:E22 &rarr; crm:P108i &rarr; crm:E12 &rarr; crm:P4 &rarr; crm:E52 &rarr; crm:P82a |

### Notes

|Name|Description|Path|
|:--|:---------|:--|
|Descriptive Notes|This field is used to document, in free text form, general notes regarding the documented photograph.| crm:P67i &rarr; crm:E73 [1] &rarr; crm:P190|
|Descriptive Notes Type|-| crm:P67i &rarr; crm:E73 [1] &rarr; crm:P2 &rarr; [descriptive note](http://vocab.getty.edu/aat/300435416)|