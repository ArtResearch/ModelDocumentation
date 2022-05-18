# fc:photographer Reference Data Model

__Author:__ __the name of the author__

__Version:__ __current version__



#### Fundamental  Relationships 

Fundamental relationships were created for the implementation of the Advanced Search and filtering functionality. Their extensive use was deemed necessary in order to improve the efficiency of the platform.

|Name|Relationship|Range|Description|
|--|--|--|---|
|born in|fr:Photographer_has_Date_of_Birth|xsd:date|This relationship is used to record the date when the documented Photographer was born.|
|died in|fr:Photographer_has_Date_of_Death|xsd:date|This relationship is used to record the date when the documented Photographer died.|
|born at place|fr:Photographer_has_Place_of_Birth|fc:place|This relationship is used to record the place where the documented Photographer was born. |
|died at place|fr:Photographer_has_Place_of_Death|fc:place|This relationship is used to record the place where the documented Photographer died. |
|photographed|fr:Photographer_photographed_Work|fc:work|This relationship is used to record the works which the documented Photographer depicted. |
|created|fr:Photographer_created_Photo|fc:photo|This relationship is used to record the photos which the documented Photographer created.|
|used|fr:Photographer_used_Technique|fc:technique|This relationship is used to record the technique that the documented Photographer used.|
|has gender|fr:Photographer_has_Gender|fc:gender|This relationship is used to record the gender of the documented Photographer.|
|has nationality|fr:Photographer_has_Nationality|fc:nationality|This relationship is used to record the nationality of the documented Photographer.|



#### custom Relationships 

custom relationships have been used

|Name|Paths|Description|
|----|----|----|
|has provider|custom:has_provider|This relationship is used to recorde the provider of the documented photgrapher|
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

The fields used to describe a photographer can be functionally grouped according to higher level units in order to allow for an easier approach to the entry and navigation of the data by information category. The information categories identified have been enumerated in the following table.

|        #  |   Name             |    Description                                                 |   
|----------:|:-------------------|:---------------------------------------------------------------|
|        1  |   Person Info      |    this information category gathers  together descriptor  used for assigning names,types to a photographer,  as well as descriptors relevant to the tracking of the birth and death of a photographer |



#### Person Info

This information category gathers  together descriptors  used for assigning names,types to a photographer,  as well as descriptors relevant to the tracking of the birth and death of a photographer

|Name|Description|Path|
|:--|:---------|:--|
|Identifier|This field is used to indicate an identifier attributed to the documented photographer.|crm:P1 -> crm:E42 -> rdfs:label|
|Name|This field is used to record the main name attributed to the documented photographer.|crm:P1 -> crm:E41 -> rdfs:label|
|Name Type|This field is used to indicate a type of a specific part of the name attributed to the documented photographer.|crm:P1 -> crm:E41 -> crm:P2_has_type -> crm:E55_Type|
|Place of Birth|This field is used to indicate the place of birth of the documented photographer.|fr:Person_has_Place_of_Birth|
|Place of Death|This field is used to indicate the place of death of the documented photographer.|fr:Person_has_Place_of_Death|
|Active|This field is used to indicate the period within the documented photographer was active.| crm:P14i -> crm:F51_Pursuit -> crm:P4 -> crm:E52 -> crm:P82 |
|Nationality|This field is used to record the association of the documented photographer to a national body, usually indicating citizenship.|fr:Person_has_Nationality -> fc:Person|
|Gender|This field is used to record the gender ascribed of the documented photographer.|fr:Person_has_Gender -> xsd:string|
|Date of Birth|This field is used to record the  date for the birth of the documented photographer.|fr:Person_has_Date_of_Birth\|fr:Artist_has_Date_of_Birth -> xsd:date|
|Date of Death|This field is used to record the  date for the death of the documented photographer.|fr:Person_has_Date_of_Death\|fr:Artist_has_Date_of_Death -> xsd:date|







