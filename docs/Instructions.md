# Instructions

Each information category is represented here both in the form of a table and a semantic graph model. The graph presents an overview of the semantic model formed by the suggested descriptors, while the table provides for each descriptor both an explanatory description of its intended function and a mapping of this intended function to a [CIDOC-CRM](cidoc-crm.org) path expressions.

The mappings presented in the table use only the class and property identifiers of [CIDOC-CRM](cidoc-crm.org) adopting the formalism of:

* Classes: **E** + _ID_
* Properties: **P** + _ID_

Moreover, when it is necessary to make explicit that the same node is referenced across descriptors in a semantic path variable [n] (where n is a number) is placed next to a class to indicate its reuse across mapping constructs.

For example, the descriptor ‘identifier’ for an instance of person is mapped as:

1.  __crm:E21 &rarr; crm:P1 &rarr; crm:E42 [1]__

The descriptor for the provider of this identifier, ‘Identifier Provider’ refers back semantically to the ‘Identifier’ descriptor (qua appellation), hence in the semantic mapping the particular individual node is referred back to as the subject of the act of being given an appellation. Expressed in our formalism this becomes:

1.  __crm:E21 &rarr; crm:P1 &rarr; crm:E42 [1]__ &rarr; crm:P37i &rarr; crm:E15 &rarr; crm:P14 &rarr; crm:E39 

The variable [1] in the second mapping is provided to signal to the reader that the same node (instance of class E42) is being referred to across two mappings, the first of the identifier as such and the second of its being attributed by some organization.

The classes and properties used in this document belong to the following namespaces using the following prefixes:

rdf: [http://www.w3.org/1999/02/22-rdf-syntax-ns#](http://www.w3.org/1999/02/22-rdf-syntax-ns#)

rdfs: [http://www.w3.org/2000/01/rdf-schema#](http://www.w3.org/2000/01/rdf-schema#)

crm: [http://http://www.cidoc-crm.org/cidoc-crm/](http://http://www.cidoc-crm.org/cidoc-crm/)

xsd: [http://www.w3.org/2001/XMLSchema#](http://www.w3.org/2001/XMLSchema#)

crmdig: [http://www.ics.forth.gr/isl/CRMext/CRMdig.rdfs/](http://www.ics.forth.gr/isl/CRMext/CRMdig.rdfs/)

owl: [http://www.w3.org/2002/07/owl#](http://www.w3.org/2002/07/owl#)

custom: [https://artresearch.net/custom/](https://artresearch.net/custom/)

fc: [https://artresearch.net/resource/fc/](https://artresearch.net/resource/fc/)

fr: [https://artresearch.net/resource/fr/](https://artresearch.net/resource/fr/)

cfc: [https://artresearch.net/resource/custom/fc/](https://artresearch.net/resource/custom/fc/)

cfr: [https://artresearch.net/resource/custom/fr/](https://artresearch.net/resource/custom/fr/)

skos: [http://www.w3.org/2004/02/skos/core#](http://www.w3.org/2004/02/skos/core#)

geo: [http://www.geonames.org/ontology#](http://www.geonames.org/ontology#)