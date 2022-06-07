#Artwork 

The __artwork__ reference data model provides a list of standard fields that are typically present in the general description of an artwork in a cultural heritage data system. The artwork is taken here in the sense of a movable, physical work of some sort such as would be typically inventoried by a museum. Specific documentation of elements of an artwork depends highly upon the kind of artwork it is. This reference model does not intend to cover such specificities but to remain at a general level description, providing a consolidated, high-level reference data model of most commonly reused descriptors for an artwork and to provide for these, in turn, a set of standard semantic mappings to the [CIDOC-CRM](https://www.cidoc-crm.org/).
Moreover, each field is marked with regards to its potential functionality with regards to instance matching between overlapping datasets. This reference data model aims to serve a number of functions including:


* to be adopted by institutions acting as aggregation hubs in order to create consistent re-expressions of extant reference information in a common [CIDOC-CRM](https://www.cidoc-crm.org/) based expression.
* to guide mapping processes of extant data sources with common mapping patterns


The [CIDOC-CRM](https://www.cidoc-crm.org/) entity E22 Man-Made Object was used for the semantic annotation of the artworks as well as for the photogrpahs. In order to distinguish these two, custom categories were created, the __[work](Artwork.md)__ category(fc:work) and the __[photo](Photo.md)__ category(fc:photo), which were used to represent the artworks and the photographs respectively.

