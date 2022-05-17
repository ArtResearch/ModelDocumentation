# Instruction

Each information category is represented here both in the form of a table and in the form of a semantic graph model. The graph presents an overview of the semantic model formed by the suggested descriptors, while the table provides for each descriptor, both an explanatory description of its intended function and a mapping of this intended function to a CIDOC-CRM path expression.

The mappings present in the table, for readability purpose, use only the class and property identifiers of CIDOC-CRM adopting the formalism of:

* Classes: E+ID
* Properties: P+ID

Moreover, when it is necessary to make explicit that the same node is referenced across descriptors in a semantic path variable [n] (where n is a number) is placed next to a class to indicate its reuse across mapping constructs.

For example, the descriptor ‘identifier’ for an instance of person is mapped as:

1.  __E21 -> P1 -> E42 [1]__

The descriptor for the provider of this identifier, ‘Identifier Provider’ refers back semantically to the ‘Identifier’ descriptor (qua appellation), hence in the semantic mapping the particular individual node is referred back to as the subject of the act of being given an appellation. Expressed in our formalism this becomes:

1.  __E21 -> P1 -> E42 [1]__ -> P37i -> E15 -> P14 -> E39 

The variable [1] in the second mapping is provided to signal to the reader that the same node (instance of class E42) is being referred to across two mappings, the first of the identifier as such and the second of its being attributed by some organization.

The classes and properties used in this document belong to the following namespaces using the following prefixes:

rdf: [http://www.w3.org/1999/02/22-rdf-syntax-ns#](http://www.w3.org/1999/02/22-rdf-syntax-ns#)

rdfs: [http://www.w3.org/2000/01/rdf-schema#](http://www.w3.org/2000/01/rdf-schema#)

crm: [http://http://www.cidoc-crm.org/cidoc-crm/](http://http://www.cidoc-crm.org/cidoc-crm/)

xsd: [http://www.w3.org/2001/XMLSchema#](http://www.w3.org/2001/XMLSchema#)

crmdig: [http://www.ics.forth.gr/isl/CRMext/CRMdig.rdfs/](http://www.ics.forth.gr/isl/CRMext/CRMdig.rdfs/)

ssw: [http://catalog.sharedshelf.artstor.org/ssw](http://catalog.sharedshelf.artstor.org/ssw)

display: [http://catalog.sharedshelf.artstor.org/display](http://catalog.sharedshelf.artstor.org/display)

vocab: [https://artresearch.net/resource/midas/vocabulary/](https://artresearch.net/resource/midas/vocabulary/)

owl: [http://www.w3.org/2002/07/owl#](http://www.w3.org/2002/07/owl#)

original: [http://foto.biblhertz.it/](http://foto.biblhertz.it/)

iiif_image: [https://ids.lib.harvard.edu/ids/iiif/](https://ids.lib.harvard.edu/ids/iiif/)

image: [http://fotothek.biblhertz.it/bh/320px/](http://fotothek.biblhertz.it/bh/320px/)

iiif_json: [https://foto.biblhertz.it/exist/foto/](https://foto.biblhertz.it/exist/foto/)

ico: [http://iconclass.org/](http://iconclass.org/)

custom: [https://artresearch.net/custom/](https://artresearch.net/custom/)

fc: [https://artresearch.net/resource/fc/](https://artresearch.net/resource/fc/)

fr: [https://artresearch.net/resource/fr/](https://artresearch.net/resource/fr/)

skos: [http://www.w3.org/2004/02/skos/core#](http://www.w3.org/2004/02/skos/core#)

voc: [http://vocab.getty.edu/ontology#](http://vocab.getty.edu/ontology#)