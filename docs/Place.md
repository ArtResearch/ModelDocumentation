# fc:place Reference Data Model

__Author:__ __the name of the author__

__Version:__ __current version__



#### Introduction

The __fc:place__ semantic annotation refers to the places which are related to the works, institutions and persons shared by the providers. 
In this section will be presented all the relationships which are connected to the places.



#### cidoc crm Relationships 

cidoc crm relationships have been used

|Name|Paths|
|----|----|
|identifier|crm:P1 -> crm:E42 -> rdfs:label|
|type|crm:P2 -> crm:E55|





#### Fundamental  Relationships 

Fundamental relationships were created for the implementation of the Advanced Search and filtering functionality. Their extensive use was deemed necessary in order to improve the efficiency of the platform.

|Name|Relationship|Range|Description|
|--|--|--|---|
|Place of Work|fr:Place_of_Work|fc:work|This relationship is used to record the work which is related to the documented place.|
|Place depicted by|fr:Place_depicted_by|fc:photo|This relationship is used to record the photo that depicts the documented place.|
|Place of Artist|fr:Place_of_Artist|fc:artist|This relationship is used to record the relationship between an artist and the documented place.|
|Place was birthplace of Artist|fr:Place_was_birthplace_of_Artist|fc:artist|This relationship is used to record the artist who was born at the the documented place.|
|Place was worklocation of Artist|fr:Place_was_worklocation_of_Artist|fc:artist|This relationship is used to record that the documented place was a worklocation of the Artist.|
|Place was deathplace of Artist|fr:Place_was_deathplace_of_Artist|fc:artist|This relationship is used to record the artist who died at the the documented place.|
|Place of Institution|fr:Place_of_Institution|fc:institution|This relationship is used to record the institution which is located at the documented place.|
|Place was birthplace of Photographer|fr:Place_was_birthplace_of_Photographer|fc:photographer|This relationship is used to record the photographer who was born at the the documented place.|
|Place was deathplace of Photographer|fr:Place_was_deathplace_of_Photographer|fc:photographer|This relationship is used to record the photographer who died at the the documented place.|



#### GeoLocation  Relationships 

GeoLocation relationships were used in order to specify the location of the place

|Name|Relationship|Range|Description|
|--|--|--|---|
|latitude|geo:lat|xsd:string|This relationship is used to record the latitude of the documented place.|
|longitude|geo:long|xsd:string|This relationship is used to record the longitude of the documented place.|



#### GeoNames  Relationships 

GeoNames Location were used __?__

* [alternateName](http://www.geonames.org/ontology#alternateName)
* [countryCode](http://www.geonames.org/ontology#countryCode)
* [featureClass](http://www.geonames.org/ontology#featureClass)
* [featureCode](http://www.geonames.org/ontology#featureCode)
* [locationMap](http://www.geonames.org/ontology#locationMap)
* [nearbyFeatures](http://www.geonames.org/ontology#nearbyFeatures)
* [parentADM2](http://www.geonames.org/ontology#parentADM2)
* [parentADM3](http://www.geonames.org/ontology#parentADM3)
* [parentFeature](http://www.geonames.org/ontology#parentFeature)
* [wikipediaArticle](http://www.geonames.org/ontology#wikipediaArticle)
* [name](http://www.geonames.org/ontology#name)
* [parentADM1](http://www.geonames.org/ontology#parentADM1)
* [parentCountry](http://www.geonames.org/ontology#parentCountry)
* [population](http://www.geonames.org/ontology#population)


#### Model Section Description

A combination of cidoc crm ontology, fundamental categories and relationships was used in order to achieve the most efficient way for the retrieval of the semantic data. The fields used to describe a place can be functionally grouped according to higher level units in order to allow for an easier approach to the navigation of the data by information category. The information categories identified have been enumerated in the following table.

|        #  |   Name             |    Description                                                 |   
|----------:|:-------------------|:---------------------------------------------------------------|
|        1  |Place Info|This information category gathers  together descriptos  used for assigning names,types to a place, both at present and  historically.|
|        2  |External Info|This information category is used to show on map the documented place and the tree of places starting from the higher in the hiererchy (for example the country) and moving to the documented place(for example the city). |




##### Place Info

|Name|Description|Path|
|:--|:---------|:--|
|Title|This field is used to indicate the title which are attributed to the documented place.|crm:P1 -> E41 [1] -> rdfs:label|
|Title Type|-|crm:P1 -> E41 [1] -> crm:P2 -><[http://vocab.getty.edu/aat/300417193](http://vocab.getty.edu/aat/300417193)>|
|Name|This field is used to indicate the name which are attributed to the documented place.|rdfs:label|
|Population|This field is used to indicate the population of the documented place.|geo:population|



##### External Info

This information category is used to
1. show the exact location of a place on the map 
2. show a tree of other documented Places in which the current places is falling in. 