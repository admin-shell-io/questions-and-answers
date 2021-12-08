# Asset Administration Shell Body of Knowledge (AASBOK)

## Specification papers
### Onboarding material 
* [AAS specification reading guide (04.20)](https://www.plattform-i40.de/PI40/Redaktion/EN/Downloads/Publikation/Asset_Administration_Shell_Reading_Guide.html)
* [AAS from technical perspective (04.21)](https://www.plattform-i40.de/PI40/Redaktion/EN/Downloads/Publikation/2021_What-is-the-AAS.html)
### Core specifications
* [Part 1 v3](https://www.plattform-i40.de/PI40/Redaktion/EN/Downloads/Publikation/Details_of_the_Asset_Administration_Shell_Part1_V3.html)
* [Part 2 v1RC01](https://www.plattform-i40.de/PI40/Redaktion/EN/Downloads/Publikation/Details_of_the_Asset_Administration_Shell_Part2_V1.html)
  * [Open API definitions of RESTful interfaces](https://app.swaggerhub.com/search?type=API&owner=Plattform_i40)
### Standardized submodels
* [Technical Data Submodel (11.20)](https://www.plattform-i40.de/PI40/Redaktion/EN/Downloads/Publikation/Submodel_templates-Asset_Administration_Shell-Technical_Data.html)
* [Digital Nameplate (11.20)](https://www.plattform-i40.de/PI40/Redaktion/EN/Downloads/Publikation/Submodel_templates-Asset_Administration_Shell-digital_nameplate.html)
* [BOM Submodel (theoretical foundations only) (04.18)](https://www.plattform-i40.de/PI40/Redaktion/DE/Downloads/Publikation/hm-2018-relationship.html)
### Security
### Semantic ID repositories
* [ID repository](https://github.com/admin-shell-io/id)
### OPC UA Companion Spec OPC 30270
* [Specification v1.00 (06.21)](https://opcfoundation.org/developer-tools/specifications-opc-ua-information-models/opc-ua-for-i4-asset-administration-shell/)
* [Node set files](https://github.com/OPCFoundation/UA-Nodeset/tree/v1.04/I4AAS)
### ECLASS
* [Whitepaper: Modelling the Semantics of Data of an Asset Administration Shell with Elements of ECLASS (06.21)](https://www.eclass.eu/fileadmin/downloads/2021-06-29_Whitepaper_PlattformI40-ECLASS.pdf)

## Tools and SDKs <!-- overview based on https://www.iiconsortium.org/pdf/2021_March_JoI_Open_Source_Drives_Digital_Twin_SA.pdf -->
### Tools (which meta-model level, which interfaces (AASX (XML, JSON), OPC UA, RESTful), infrastructure (registry)... )
* [AASX Package Explorer](https://github.com/admin-shell-io/aasx-package-explorer) (Apache License 2.0; C#) 
  * [Online version](https://admin-shell-io.com:5005/)
* [AASX Server](https://github.com/admin-shell-io/aasx-server) (Apache License 2.0; C#)
* [Web AAS Client](https://github.com/admin-shell-io/web-aas-client) (Apache License 2.0, JavaScript)
* [AAS Manager](https://github.com/zrgt/pygui40aas/) (GPLv3, Pyhton): Python and QT based AAS browser and editor

### SDKs
* [Eclipse BaSyx](https://www.eclipse.org/basyx/) (EPLv2; Java, C++, C#)
   * [Getting started video](https://www.youtube.com/watch?v=9HKd0vLHTMA)
* [Nova AAS](https://gitlab.com/novaas/catalog/nova-school-of-science-and-technology/novaas/) (EUPL; JavaScript/Node Red)
   * [Introduction video](https://www.youtube.com/watch?v=jXQ8Nq4yjS4&t=30m30s)
* [PyI40AAS](https://git.rwth-aachen.de/acplt/pyi40aas) (EPLv2; Python)
* [SAP i40-aas](https://github.com/SAP/i40-aas) (APL-v2; JavaScript)

### Example AAS models 
* http://www.admin-shell-io.com/samples/
