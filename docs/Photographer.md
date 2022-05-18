# Photographer Reference Data Model

__Author:__ __the name of the author__

__Version:__ __current version__

## Introduction

The __fc:photographer__ semantic annotation refers to the photographers which are shared by the Photo Archives and are involved in the production of [photographs](http://vocab.getty.edu/aat/300046300), [photographic prints](http://vocab.getty.edu/aat/300127104) or [digital photographs](http://vocab.getty.edu/aat/300417379) that are part of the Artresearch project and is the domain used for the semantic modeling described below.

## Relationships
### Fundamental  Relationships 

Fundamental relationships were created for the implementation of the Contextual Search and filtering functionality. Their extensive use was deemed necessary in order to improve the efficiency of the platform.

|Name|Relationship|Range|Description|
|--|--|--|---|
|born in|fr:Photographer_has_Date_of_Birth|xsd:date|Refers to the date when the documented Photographer was born.|
|died in|fr:Photographer_has_Date_of_Death|xsd:date|Refers to the date when the documented Photographer died.|
|born at place|fr:Photographer_has_Place_of_Birth|fc:place|Refers to the place where the documented Photographer was born. |
|died at place|fr:Photographer_has_Place_of_Death|fc:place|Refers to the place where the documented Photographer died. |
|photographed|fr:Photographer_photographed_Work|fc:work|Refers to the works which the documented Photographer depicted. |
|created|fr:Photographer_created_Photo|fc:photo|Refers to the photos which the documented Photographer created.|
|used|fr:Photographer_used_Technique|fc:technique|Refers to the technique that the documented Photographer used.|
|has gender|fr:Photographer_has_Gender|fc:gender|Refers to the gender of the documented Photographer.|
|has nationality|fr:Photographer_has_Nationality|fc:nationality|Refers to the nationality of the documented Photographer.|



### Custom Relationships 

Custom relationships have been used

|Name|Paths|Description|
|----|----|----|
|has provider|custom:has_provider| Referes to the Photo Archive that provided the information of the referenced entity|
|has type|custom:has_type| Referes to the custom type of refrerenced entity|

## Model Section Description

The fields used to describe a photographer can be functionally grouped according to higher level units in order to allow for an easier approach to the entry and navigation of the data by information category. The information categories identified have been enumerated in the following table.

|        #  |   Name             |    Description                                                 |   
|----------:|:-------------------|:---------------------------------------------------------------|
|        1  |   Person Info      |    This information category gathers  together descriptor  used for assigning names,types to a photographer,  as well as descriptors relevant to the tracking of the birth and death of a photographer |



### Person Info

This information category gathers  together descriptors  used for assigning names,types to a photographer,  as well as descriptors relevant to the tracking of the birth and death of a photographer

|Name|Description|Path|
|:--|:---------|:--|
|Identifier|This field is used to indicate an identifier attributed to the documented photographer.|crm:P1 &rarr; crm:E42 &rarr; rdfs:label|
|Name|This field is used to record the main name attributed to the documented photographer.|crm:P1 &rarr; crm:E41 &rarr; rdfs:label|
|Name Type|This field is used to indicate a type of a specific part of the name attributed to the documented photographer.|crm:P1 &rarr; crm:E41 &rarr; crm:P2_has_type &rarr; crm:E55_Type|
|Place of Birth|This field is used to indicate the place of birth of the documented photographer.|fr:Person_has_Place_of_Birth|
|Place of Death|This field is used to indicate the place of death of the documented photographer.|fr:Person_has_Place_of_Death|
|Active|This field is used to indicate the period within the documented photographer was active.| crm:P14i &rarr; crm:F51_Pursuit &rarr; crm:P4 &rarr; crm:E52 &rarr; crm:P82 |
|Nationality|This field is used to record the association of the documented photographer to a national body, usually indicating citizenship.|fr:Person_has_Nationality &rarr; fc:Person|
|Gender|This field is used to record the gender ascribed of the documented photographer.|fr:Person_has_Gender &rarr; xsd:string|
|Date of Birth|This field is used to record the  date for the birth of the documented photographer.|fr:Person_has_Date_of_Birth\|fr:Artist_has_Date_of_Birth &rarr; xsd:date|
|Date of Death|This field is used to record the  date for the death of the documented photographer.|fr:Person_has_Date_of_Death\|fr:Artist_has_Date_of_Death &rarr; xsd:date|







