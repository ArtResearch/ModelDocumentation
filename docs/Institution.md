# fc:institution Reference Data Model


#### cidoc crm Relationships 

cidoc crm relationships have been used

|Name|Paths|
|----|----|
|identifier|crm:P1 -> crm:E42 -> rdfs:label|
|type|crm:P2_has_type -> custom:noType|



#### Fundamental  Relationships 

Fundamental relationships were created for the implementation of the Advanced Search and filtering functionality. Their extensive use was deemed necessary in order to improve the efficiency of the platform. 

|Name|Relationship|Range|Description|
|--|--|--|---|
|Institution_provides_Work|fr:Institution_provides_Work|fc:work|This relationship is used to record the works which the documented institution provides.|
|Institution_keeps_Work|fr:Institution_keeps_Work|fc:work|This relationship is used to record the works which the documented institution keeps.|
|Institution_from_Place|fr:Institution_from_Place|fc:place|This relationship is used to record the loacation of the documented institution.|
|Institution_has_Original_Link|fr:Institution_has_Original_Link|__what's the range__ |This relationship is used to record the original link of the documented institution.|
|Institution_depicted_by|fr:Institution_depicted_by|fc:photo|This relationship is used to record the photo which depicts the documented institution.|
|Institution_has_Latitude|fr:Institution_has_Latitude|xsd:string|This relationship is used to record the Latitude of the documente institution.|
|Institution_has_Longitude|fr:Institution_has_Longitude|xsd:string|This relationship is used to record the Longitude of the documents institution.|
|Institution_provides_Artist|fr:Institution_provides_Artist|fc:artist|This relationship is used to record the artists that the documented institution provides|
|Institution_keeps_Photo|fr:Institution_keeps_Photo|fc:photo|This relationship is used to record the photos that the documented institution provides|



#### custom Relationships 

|Name|RelationShip|Description
|----|----|----|
|has provider|custom:has_provider|This relationship is used to record the provider of the documented institution.|
|has type|custom:has_type|This relationship is used to record that the documented institution is of type 'Pharos'.|



#### Model Section Description

The fields used to describe a person can be functionally grouped according to higher level units in order to allow for an easier approach to the entry and navigation of the data by information category. The information categories identified have been enumerated in the following table.

|        #  |   Name             |    Description                                                 |   
|----------:|:-------------------|:---------------------------------------------------------------|
|        1  |   Repository info      |    this information category gathers  together descriptors  used for assigning names and types to institutions|




#### Repository info

|Name|Description|Path|
|:--|:---------|:--|
|Title|This field is used to indicate the preferred identifier attributed to the documented instance of the documented institution.|crm:P1 -> crm:E42 [1] -> rdfs:label|
|Title Type|-|crm:P1 -> crm:E42 [1] -> crm:P2 -> <[http://vocab.getty.edu/aat/300417193](http://vocab.getty.edu/aat/300417193)> |
|Types|This field is used to indicate the types which are related to the documented instituion.| crm:P2 -> crm:E55|




