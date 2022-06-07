# Repository Reference Data Model

__Author:__ __the name of the author__

__Version:__ __current version__

## Introduction

The __fc:institution__ semantic annotation refers to the repositories which are shared by the Photo Archives and might relate to all the entities that are part of the Artresearch project and is the domain used for the semantic modeling described below.

## Relationships
### Fundamental  Relationships 

Fundamental relationships were created for the implementation of the Contextual Search and filtering functionality. Their extensive use was deemed necessary in order to improve the efficiency of the platform. 

|Name|Relationship|Range|Description|
|--|--|--|---|
|Institution_provides_Work|fr:Institution_provides_Work|fc:work|Refers to the works which the documented institution provides.|
|Institution_keeps_Work|fr:Institution_keeps_Work|fc:work|Refers to the works which the documented institution keeps.|
|Institution_from_Place|fr:Institution_from_Place|fc:place|Refers to the loacation of the documented institution.|
|Institution_has_Original_Link|fr:Institution_has_Original_Link| - |Refers to the original link of the documented institution.|
|Institution_depicted_by|fr:Institution_depicted_by|fc:photo|Refers to the photo which depicts the documented institution.|
|Institution_has_Latitude|fr:Institution_has_Latitude|xsd:string|Refers to the Latitude of the documente institution.|
|Institution_has_Longitude|fr:Institution_has_Longitude|xsd:string|Refers to the Longitude of the documents institution.|
|Institution_provides_Artist|fr:Institution_provides_Artist|fc:artist|Refers to the artists that the documented institution provides|
|Institution_keeps_Photo|fr:Institution_keeps_Photo|fc:photo|Refers to the photos that the documented institution provides|



### Custom Relationships 

|Name|RelationShip|Description
|----|----|----|
|has provider|custom:has_provider|Refers to the provider of the documented institution.|
|has type|custom:has_type|Refers to that the documented institution is of type 'Pharos'.|

### [CIDOC-CRM](https://www.cidoc-crm.org/) Relationships 

[CIDOC-CRM](https://www.cidoc-crm.org/) relationships were used

|Name|Paths|
|----|----|
|identifier|crm:P1 &rarr; crm:E42 &rarr; rdfs:label|
|type|crm:P2_has_type &rarr; custom:noType|


## Model Section Description

The fields used to describe a person can be functionally grouped according to higher level units in order to allow for an easier approach to the entry and navigation of the data by information category. The information categories identified have been enumerated in the following table.

|        #  |   Name             |    Description                                                 |   
|----------:|:-------------------|:---------------------------------------------------------------|
|        1  |   Repository info      |    this information category gathers  together descriptors  used for assigning names and types to institutions|




## Repository info

|Name|Description|Path|
|:--|:---------|:--|
|Title|This field is used to indicate the preferred identifier attributed to the documented instance of the documented institution.|crm:P1 &rarr; crm:E42 [1] &rarr; rdfs:label|
|Title Type|-|crm:P1 &rarr; crm:E42 [1] &rarr; crm:P2 &rarr; <[http://vocab.getty.edu/aat/300417193](http://vocab.getty.edu/aat/300417193)> |
|Types|This field is used to indicate the types which are related to the documented instituion.| crm:P2 &rarr; crm:E55|




