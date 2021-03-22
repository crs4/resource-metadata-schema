# EJPRD RESOURCES METADATA SCHEMA


Here you will find the *EJPRD Resources Metadata schema* - the JSON schema version of the [EJPRD Resources Metadata schema](https://github.com/ejp-rd-vp/resource-metadata-schema) - a data model for describing EJPRD resources in the virtual platform catalog.

Production
----------
The metadata has three major modules
* [catalog_of_registries.json](https://github.com/ejp-rd-vp/resource-metadata-schema/blob/master/docs/catalog_of_registries.json): this describes the catalogs / registries properties of the virtual platform catalogs resource. The catalog properties and description detailed [here](https://ejp-rd-vp.github.io/resource-metadata-schema/catalog_of_registries.html).


* [Location]()

* [Organisation]()

* [PatientRegistryDataset]()

* [DiseaseCode]()

* [DiseaseCodeSystem]()


* []()


* []()

To make catalog_of_registries.json easy to understand and maintain, it uses JSON schema [definitions and references](https://cswr.github.io/JsonSchema/spec/definitions_references/) for objects, and properties with regex patterns, which are re-used in the schema:  
<p align="center">
<img src="assets/types.png" />
</p>






biotoolsj.json mirrors biotoolsSchema XML schema (XSD) as closely as possible where possible and desirable:
* XML elements [1] are preserved as JSON properties
* XML element structure / nesting is preserved (whilst discarding XSD design patterns not applicable in JSON schema)
* XML element names are preserved as JSON property names
* XML comments are preserved in JSON ```title```, ```description``` and ```$comment``` properties.

[1] In biotoolsSchema 3.3.0 "organisational" elements (whose purpose was only to structure the schema) were discarded: ```summary```, ```labels```

Structure
---------
To make biotoolsj.json easy to understand and maintain, it uses JSON schema [definitions and references](https://cswr.github.io/JsonSchema/spec/definitions_references/) for objects, and properties with regex patterns, which are re-used in the schema:  
<p align="center">
<img src="assets/types.png" />
</p>

Of these, **tool** is the top-level object. **dataType** and **ontologyConcept** are defined but not actually used (they're retained for now in case they find future use).  All the others are definitions that are refered to in multiple places within the schema.


Documentation (for latest stable version)
-----------------------------------------
Technical docs formatted for website are maintained in [biotoolsSchemaJ repo](https://github.com/bio-tools/biotoolsSchemaJ) and hosted [here](http://bio-tools.github.io/biotoolsSchemaJ) (uses files copied from "stable" folder)


# Files

File                            | Description
----                            | -----------
biotoolsj.json                  | biotoolsSchema (JSON schema)
LICENSE                         | Schema license information
assets                          | Folder for images and other assets
assets/biotoolsSchema_json.xsd  | Ignore (biotoolsSchema 3.2.0 (XSD schema) produced for initial reverse-engineering of the JSON schema)
stable                          | (not used yet) - current stable version of the schema
versions                        | (not used yet) - older stable versions of the schema
README.md		        | This file
