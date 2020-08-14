# Questions-and-Answers

**How shall a link to a website be entered in an AAS, as File or as ReferenceElement object?**

Links to websites shall be entered as File object (physical reference). ReferenceElement  objects represent logical references.
A typical usage for logical references is in the description of a topology of the asset or „consist of” hierarchies.
(Answered: 2020-08-13)

**If the same properties are use in several submodels, shall they also be entered several times or shall they be referenced?**

Submodels shall be as independent as possible so that they can be changed and developed separately.
Consequently, the same properties shall be copied to another submodel and references shall not be used in such case. 
The concept description referenced in semanticId, however, should be the same.
(Answered: 2020-08-13)

**How to use physical units for quantifiable properties?**

AAS defines specific constructs of unit and unitID for concept descriptions (template DataSpecificationIEC61360).
We advise you to use unitIDs  that refer to pre-defined eCl@ss IRDIs, e.g., 0173-1#05-AAA480#002  for millimeters. 
In a non-likely case of non-existent global IRDI for a unit, please follow the general guidance for custom semantic IDs
to create a custom unitID.
(Answered: 2020-08-13)

**What shall be entered for the semanticId attribute if a related concept description does not exist in eCl@ss or IEC CDD?**

Besides eCl@ss and IEC CCD also other domain specific dictionaries may be used. The only prerequisite is that the id can be uniquely resolved.

This also holds true for proprietary dictionaries. For example, the id of a proprietary concept description defined by your own company could be <CompanyName>/<FurtherHierarchicalName>/<PropertyName>”. This id is also used as semanticId of the property then.

Alternatively, an agile flexible approach using GITHUB has been defined. You may store your CDs there which are defined as “http://admin-shell.io/<sub-namespace>[/<version>[/<revision>]]/<ShortId>”. The working draft repository is placed at https://github.com/admin-shell-io/id.
(Answered: 2020-08-13)

**How shall the eCl@ss group “Zusatzdokumentation (e.g. IRDI 0173-1#02-ADN464#..)” be used for documentation?**

Please use the submodel template based on VDI 2770 for documentation instead. It will be released soon.
(Answered: 2020-08-13)

**How to treat values of Properties with values in multiple languages?**

Details of the Asset Administration Shell Part 1 provides the **MultiLanguageProperty** entity for this case since version 2.0.
(Answered: 2020-08-13)

**How shall a document be handled which includes different content according to VDI 2770 and the related DocumentClassIDs?**

Currently VDI 2770 only allows exactly one DocumentClassID per document. A proposal has been already made to the VDI 2770 workgroup to extend this. In AAS it is suggested to list several properties with different DocumentClassIDs for such a multipurpose document.
(Answered: 2020-08-13)

**Which names are already defined for important submodels?**

The following names shall be used for submodels:

**Identification** defines supplier and product 
**TechnicalData** for technical data of a product
**ConfigurationData** for setpoints of a production process
**OperationalData** for actual values of a production process
**Documentation** to store documents for a product and to classify the documentation according to VDI 2770
**CertificatesAndDeclaration** for storing certificates and conformance classes
(Answered: 2020-08-13)

**How to store certificates and conformance declarations within AAS/Submodels?**

A dedicated submodel with IdShort “CertificatesAndDeclarations” with ID https://admin-shell.io/submodels/CertificatesAndDeclarations is proposed. This model shall contain boolean properties or text-properties indicating conformance to certificates. Actual certificate documents, e.g., scanned TÜV reports, shall be contained in the “Documentation” submodel and referenced from “CertificatesAndDeclarations” elements.

Examples are the boolean property **0173-1#02-BAF053#008** set to true if a CE qualification is present, or the text-property **0173-1#02-AAE327#001** for a textual name of the fulfilled conformance.
(Answered: 2020-08-13)

**Which mechanisms can be used to structure complex data?**

Collections can be used to “physically” separate and structure submodel elements into different topics.

Qualifiers can be used to add additional meta-information to AAS elements that is not included in the model of AAS. 
Currently (Details of AAS Part 1 Version 2), concrete qualifiers are not specified, however the document provides some non-normative examples for qualifiers:
e.g. the indication of a lifecycle state of a value by “as-specified” or “as-measured”, or
e.g. the indication of multiplicity of allowed components for modelling by “greater than 0” and others.
(Answered: 2020-08-13)

**Where are examples of AAS available?**

Examples of several suppliers are found at: http://admin-shell-io.com/samples/ 
(Answered: 2020-08-13)



