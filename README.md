This Q&A has been created by a Task Force of "ZVEI SG Modelle und Standards".

# Questions-and-Answers

**How shall a link to a website be entered in an AAS, as File or as ReferenceElement object?** <!-- ID: 2 -->

Links to websites shall be entered as File object (physical reference). ReferenceElement  objects represent logical references.
A typical usage for logical references is in the description of a topology of the asset or „consist of” hierarchies.
(Answered: 2020-08-13)

**If the same properties are use in several submodels, shall they also be entered several times or shall they be referenced?** <!-- ID: 5, 23 -->

Submodels shall be as independent as possible so that they can be changed and developed separately.
Consequently, the same properties shall be copied to another submodel and references shall not be used in such case. 
The concept description referenced in semanticId, however, should be the same.
(Answered: 2020-08-13)

**How to use physical units for quantifiable properties?** <!-- ID: 7, 20 -->

AAS defines specific constructs of unit and unitID for concept descriptions (template DataSpecificationIEC61360).
We advise you to use unitIDs  that refer to pre-defined eCl@ss IRDIs, e.g., 0173-1#05-AAA480#002  for millimeters. 
In a non-likely case of non-existent global IRDI for a unit, please follow the general guidance for custom semantic IDs
to create a custom unitID.
(Answered: 2020-08-13)

**What shall be entered for the semanticId attribute if a related concept description does not exist in eCl@ss or IEC CDD?** <!-- ID: 3 -->

Besides eCl@ss and IEC CCD also other domain specific dictionaries may be used. The only prerequisite is that the id can be uniquely resolved.

This also holds true for proprietary dictionaries. For example, the id of a proprietary concept description defined by your own company could be <CompanyName>/<FurtherHierarchicalName>/<PropertyName>”. This id is also used as semanticId of the property then.

Alternatively, an agile flexible approach using GITHUB has been defined. You may store your CDs there which are defined as “http://admin-shell.io/<sub-namespace>[/<version>[/<revision>]]/<ShortId>”. The working draft repository is placed at https://github.com/admin-shell-io/id.
(Answered: 2020-08-13)

**How shall the eCl@ss group “Zusatzdokumentation (e.g. IRDI 0173-1#02-ADN464#..)” be used for documentation?** <!-- ID: 8 -->

Please use the submodel template based on VDI 2770 for documentation instead. It will be released soon.
(Updated: 2020-08-14)

**How to treat values of Properties with values in multiple languages?** <!-- ID: 9 -->

Details of the Asset Administration Shell Part 1 provides the **MultiLanguageProperty** entity for this case since version 2.0.
(Answered: 2020-08-13)

**How shall a document be handled which includes different content according to VDI 2770 and the related DocumentClassIDs?** <!-- ID: 10 -->

Currently VDI 2770 only allows exactly one DocumentClassID per document. A proposal has been already made to the VDI 2770 workgroup to extend this. In AAS it is suggested to list several properties with different DocumentClassIDs for such a multipurpose document.
(Answered: 2020-08-13)

**Which names are already defined for important submodels?** <!-- ID: 12, 21, 24 -->

The following names shall be used for submodels:

- **Identification** defines supplier and product, 
- **TechnicalData** for technical data of a product,
- **ConfigurationData** for setpoints of a production process,
- **OperationalData** for actual values of a production process,
- **Documentation** to store documents for a product and to classify the documentation according to VDI 2770,
- **CertificatesAndDeclaration** for storing certificates and conformance classes.
(Answered: 2020-08-13)

**How to store certificates and conformance declarations within AAS/Submodels?** <!-- ID: 13 -->

A dedicated submodel with IdShort “CertificatesAndDeclarations” with ID https://admin-shell.io/submodels/CertificatesAndDeclarations is proposed. This model shall contain boolean properties or text-properties indicating conformance to certificates. Actual certificate documents, e.g., scanned TÜV reports, shall be contained in the “Documentation” submodel and referenced from “CertificatesAndDeclarations” elements.

Examples are the boolean property **0173-1#02-BAF053#008** set to true if a CE qualification is present, or the text-property **0173-1#02-AAE327#001** for a textual name of the fulfilled conformance.
(Answered: 2020-08-13)

**Which mechanisms can be used to structure complex data?** <!-- ID: 15 -->

Collections can be used to “physically” separate and structure submodel elements into different topics.

Qualifiers can be used to add additional meta-information to AAS elements that is not included in the model of AAS. 
Currently (Details of AAS Part 1 Version 2), concrete qualifiers are not specified, however the document provides some non-normative examples for qualifiers:
e.g. the indication of a lifecycle state of a value by “as-specified” or “as-measured”, or
e.g. the indication of multiplicity of allowed components for modelling by “greater than 0” and others.
(Answered: 2020-08-13)

**Where are examples of AAS available?** <!-- ID: 16 -->

Examples of several suppliers are found at: http://admin-shell-io.com/samples/ 
(Answered: 2020-08-13)

**What are best practices for creating custom IRI identifiers for generic concepts.** <a name="id18"></a><!-- ID: 18 -->

What are best practices for creating custom IRI identifiers for generic concepts.
We advise using “https://admin-shell.io/” prefix for those identifiers (see guides via https://github.com/admin-shell-io/id/) for generic concepts. Note that we advise to use “https:” protocol and avoid adding “www.” subdomain into admin-shell.io naming scheme.
Furthermore, in practical implementations we advise to “filter” out protocol and schema for comparing IRI identifiers. For example, following IDs should be considered equal:
-	https://admin-shell.io/some_id_example
-	http://admin-shell.io/some_id_example
-	ftp://admin-shell.io/some_id_example
-	https://www.admin-shell.io/some_id_example
-	http://www.admin-shell.io/some_id_example
(Answered: 2020-08-19)

**Which submodel shall contain the serial number of a device?** <!-- ID: 23 -->

Serial number is a submodel element of “Identification” submodel referenced in AAS for an asset with Type=Instance, i.e. instance’s AAS. 
(Answered: 2020-08-19)

**How to refer to semantic concepts of existing standards like VDI 2770 properties or OPC UA companion specifications (e.g. “Serial number” property from OPC UA DI companion spec)?** <!-- ID: 27, 28 -->

Map concepts to “admin-shell.io” namespace (see [custom identifier best practices](#id18)). Within the concept description itself use “sourceOfDefinition” or “isCaseOf” to link to “original” concept. (Answered: 2020-08-24)

**How is the relation between idShort, shortName and preferredName for a submodel element and the related concept description?** <!-- ID: 30 -->

If an English shortname is available in a related concept description, the English shortName shall be also used as idShort. If only a preferredName is available, that shall be translated to idShort, e.g. the preferredName “Maximum rotation speed” becomes translated to “maximumRotationSpeed”.
In case a submodel template specification is used as a base, the idShort defined in this submodel template shall be used.

Note: currently there is ongoing work on a “displayName” concept. When the according specification is completed, this question will also be updated.
(Answered: 2020-09-21)

**Where shall images (products or icons) of an asset be stored, e.g. for the use in dashboards?** <!-- ID: 31 -->

Such images may be included in the “TechnicalData” submodel as File submodel elements. It is recommended to distinguish between product photos and functional icons. Product photos shall get the idShort = "productPicture", functional icons shall get the idShort = "functionalSymbol".
(Answered: 2020-09-21)

**How shall properties be entered which are defined both in eCl@ss and in CDD?** <!-- ID: 34 -->

If definitions for several product application areas are needed (e.g. eCL@ss for factory automation and CDD for process automation), the related properties (e.g. ManufacturerName) shall be entered twice. At each of the properties one of the concept descriptions (eCl@ss or CDD) is entered. The name of a property shall be either counted up (e.g. ManufactureName1) or extended by a suffix (e.g. ManufacturerNameCDD).

Alternatively an own concept description may be defined and "isCaseOf" may be used, so that both IRDIs can be entered in the concept description.
(Answered: 2020-09-21)

**Is the following IRI-based ID with a query parameter valid “http://vendor.com/suffx?a=abc&b=xyz”?** <!-- ID: 38 -->

Yes, this is a valid ID. (Answered: 2020-09-21)

**Are semanticID(s) optional or mandatory?** <!-- ID: 40 -->

SemanticIDs shall always be used for submodels and for submodelElements. Since idShort(s) or Submodel ID(s) may differ between assets and suppliers, only semanticID(s) can be identical. If semanticIDs are not available in eCl@ss or CDD, it is suggested to define an own semanticID as company specific or on GITHUB at admin-shell-io (https://github.com/admin-shell-io/id ).

In AAS Part 1 V2.0 semanticId(s) are mandatory for submodel elements and are recommendeded for submodels with kind=Instance. For submodels with kind=Template the semanticId is optional.
(Answered: 2020-09-21)

**Can semantic ID(s) be used without defining a concept description within the AAS package?** <!-- ID: 41 -->

Yes. Please use the following alternatives:
•	type=ConceptDescription, local=True: the concept description is within the package or deployed on the same server like the element referring to it
•	type=ConceptDescription, local=False: the concept description is located within a different pakckage or possibly deployed on a different server than the element referring to it
•	type=GlobalReference, local=False: a concept description object is not defined, just a reference to an external source is made
(Answered: 2020-09-21)


# Essential AAS documents
- Details of the AAS Part 1, Version 2.0.1 - https://www.plattform-i40.de/PI40/Redaktion/DE/Downloads/Publikation/Details-of-the-Asset-Administration-Shell-Part1.html

