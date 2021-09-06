# Asset Administration Shell Reading Guide

## Preamble
This is a "living" version of the [PDF document](https://www.plattform-i40.de/PI40/Redaktion/EN/Downloads/Publikation/Asset_Administration_Shell_Reading_Guide.html) published by Plattform Industrie 4.0. Copyrights are with the respective authors: Dr.  Jörg Neidig (Siemens  AG),  Andreas Orzelski (Phoenix Contact GmbH &  Co.  KG),  Stefan Pollmeier (ESR Pollmeier GmbH),  Jörg  Wende (IBM Deutschland GmbH).

## Aim of this document
Over  the  course  of  the  last  years  the  Plattform Industrie 4.0 and related organizations have published numerous  papers concerning the Asset Administration Shell. This  document  acts  as  a  guide  by  recommending  selected „must-read”  documents  for  different  reader  groups  and  will  be  updated  regularly.

## Goals  of  Industrie 4.0
Industrie 4.0 (I4.0) refers to the intelligent networking of machines and processes for industry with the help of information and communication technology. Today's rigid and strictly defined value chains are replaced by flexible, highly dynamic and globally connected value networks with new forms of cooperation. The Asset Administration Shell helps implementing digital twins for I4.0 and creating interoperability across the solutions of different suppliers.

## Asset  Administration Shell in  a nutshell
The Asset Administration Shell (AAS) is the digital representation of an asset. The AAS consists of a number of submodels in which all the information and functionalities of a given asset – including its features, characteristics, properties, statuses, parameters, measurement data and capabilities – can be described. It allows for the use of different communication channels and applications and serves as the link between objects and the connected, digital and distributed world.

The structure of the AAS is defined via a technology independent meta-model and several technology specific serialization mappings such as XML, JSON or OPC UA. Its contents are defined via domain-specific submodel templates.
 
The interaction with the AAS can follow different patterns which have different technical requirements, i.e. file exchange, server-client and peer-to-peer interaction (Figure 1).
**TODO Figure 1**

## Recommended documents
For this reading guide the documents have been sorted by interest groups rather than topics. In some cases, only specific pages or sections are recommended reading material.
* [Where to start](#where-to-start): If you have never heard of the AAS
* [For the generally interested reader](#for-the-generally-interested-reader): If you want to learn more about the subject
* [For decision makers](#for-decision-makers): If you are interested in the business side of I4.0
* [For software developers and architects](#for-software-developers-and-architects): If you want to know how to create software for the AAS
* [For users of the AAS and domain experts](#for-users-of-the-aas-and-domain-experts): If you are interested in using the AAS for specific tasks
* [Security and AI](#security-and-ai): If you want to deep dive into these special topics.

## Where to start
When completely new to the topic of I4.0 and the AAS we highly recommend visiting the [website of the Plattform Industrie 4.0 [1]](#1-what-is-industrie-40-httpsbitly3karz2n). Then start with the [Two-Pager [2]](#2the-asset-administration-shell-implementing-digital-twins-for-use-in-industrie-40-a-starter-kit-for-developers-122019-httpsbitly3kzzspl) and the [presentation slides [3]](#3der-digitale-zwilling-in-industrie-40---eine-kurz--einführung-zu-merkmalen-teilmodellen--verwal--tungsschalen-english-version-pending-102020-httpsbitly3e6za08). The first few slides of the [Presentation [4]](#4-details-of-the-administration-shell---from-idea-to-implementation-072019-httpsbitly2h8c2hn) cover general AAS topics, later slides introduce some advanced topics. All these should provide a brief and quick introduction into the topic in general. For a [deep dive [5]](#5-fortschrittsbericht-2020-industrie-40-gestalten-souverän-interoperabel-nachhaltig-english-version-pending-062020-httpsbitly3oarvje) gives a comprehensive overview of recent and current activities of the Plattform I4.0.

## For the generally interested reader
The most extensive introduction into I4.0 can be found in [the book [6]](#6-the-reference-architecture-model-rami-40-and-the-industrie-40-component-isbn-978-3-8007-4990-4-2018). The introduction and the chapters on how to transport semantic information are insightful, but the more technical sections are partially outdated. [[7]](#7-structure-of-the-administration-shell-042018-httpsbitly34jbhdo) gives a condensed overview of the concepts and serves in many ways as a leading picture. It also outlines how existing and future standards shall be brought into alignment to these concepts. [[9]](#9drive-40---vision-becomes-reality-042018-httpsbitly388st35) is recommended, because it covers all major aspects of I4.0 (including finding use cases, creating semantic models, and operation) by using a drive as an example. The described concepts can easily be transferred to sensors and actors in general.

## For decision makers
[[8]](#8what-is-the-asset-administration-shell-from-a-technical-perspective-042021-httpsbitly3d0kvbw) answers why semantic interoperability will become crucial for future manufacturing. [Publication [10]](#10-which-criteria-do-industrie-40-products-need-to-fulfil-122020-httpsbitly2tdti0d) includes a detailed list of technical criteria that need to be fulfilled for an I4.0 component. It also includes a technology roadmap and lists several examples of commercially available products that fulfill these criteria. [Reference [11]](#11-interoperability-by-standardized-properties-082019-available-upon-request-httpsbitly3ovqplh) provides companies with support in determining how their own data organization can be revised and gives step by step realization guidelines.

## For software developers and architects
The most important documents are [[12]](#12-details-of-the-asset-administration-shell-part-1-112020-httpsbitly3phsuyb) and [[13]](#13-details-of-the-asset-administration-shell-part-2-112020-httpsbitly3phsuyb). Part 1 of the Series “Asset Administration Shell in Detail” covers the AAS meta model and its technology specific serializations, whereas Part 2 focuses on the concept and realization of the common AAS API. For implementations the open source projects on https://github.com/admin-shell-io and others (see below) are highly recommended. As an overview [[8]](#8what-is-the-asset-administration-shell-from-a-technical-perspective-042021-httpsbitly3d0kvbw) describes the different shapes of the AAS from a technical perspective including security.

Whereas the technical details for composite AAS (AAS for assets composed of multiple assets) are given in [[12]](#12-details-of-the-asset-administration-shell-part-1-112020-httpsbitly3phsuyb), the introduction to the concept can be found in [[14]](#14-relationships-between-i40-components--compo--site-components-and-smart-production-062017-httpsbitly37ufwp3).

## For users of the AAS and domain experts
If you are interested in using or creating AAS we recommend to start by looking into the software tool AASX package explorer (see below) and the screencasts at http://admin-shell-io.com/screencasts/. The first submodel templates have been released to define the contents of the submodels „Digital Nameplate“ (https://bit.ly/2PmdHgr) and „Technical Data“ (https://bit.ly/31zY0os). More will follow. [[11]](#11-interoperability-by-standardized-properties-082019-available-upon-request-httpsbitly3ovqplh) and [[15]](#15-secure-implementation-of-opc-ua-for-operators-integrators-and-manufacturers-042018-httpsbitly3kzm2kj) might also be of interest. [[16]](#16-examples-of-the-asset-administration-shell-for-indus--trie-40-components-042017-httpsbitly2ti9tvc) gives an introduction and example on how to model an asset using standardized properties, however some technical details might be outdated.

## Security and AI
Although it does not deal specifically with the AAS, [[15]](#15-secure-implementation-of-opc-ua-for-operators-integrators-and-manufacturers-042018-httpsbitly3kzm2kj) highlights requirements for the secure use of OPC UA for communication in I4.0 scenarios and presents implementa- tion options. [[17]](#17-secure-download-service-102020-httpsbitly3cpsq6a) describes requirements and implemen- tations of a secure communication in the engineering process.
 
[[18]](#18-access-control-for-industrie-40-components-for-app--lication-by-manufacturers-operators-and-integrators-122018-httpsbitly37qajjq) explains different secure data access architectures and looks at questions regarding at implementation and applicability. [[19]](#19-ai-application-guide-092020-httpsbitly2gphas6) focusses on the application of AI in industrial production and analyses different use cases for potential impact and questions. [[22]](#22-describing-capabilities-of-industrie-40-compo--nents-122020-httpsbitly3tk1uao) discusses the means of capability and skill to provide standardized information about an assets functionality.

## Tools, examples and prototypes
The website [https://github.com/admin-shell-io](https://github.com/admin-shell-io)  contains  the latest version of the **AASX package explorer**, which  can  be  used  to  create,  edit  and  view  AAS  file  serializations (*.aasx).  The  site  also  includes  the  **AASX-server** which  makes AASX  packages  accessible  via  REST,  OPC  UA and  MQTT,  [a  highly  recommended  FAQ](https://github.com/admin-shell-io/questions-and-answers/)  with  best  practices  and  further  resources.

BaSyx ([https://bit.ly/3mNRe85](https://bit.ly/3mNRe85)) provides various modules  to  cover  a  broad  scope  of  I4.0  (including AAS). Hence  its  substantially more  complex  architecture. PyI40AAS  ([https://bit.ly/307hPmJ](https://bit.ly/307hPmJ))  is  a  Python  module  for  manipulating and validating AAS. On [http://www.i40-aas.de/](http://www.i40-aas.de/) one  can  access  numerous  AAS  examples  of  different  vendors  based  on  the  use  case  of  a  digital  nameplate.

## References
###### [1]: „What is Industrie 4.0?“: https://bit.ly/3kaRz2N.
###### [2]: „The Asset Administration Shell: Implementing digital twins for use in Industrie 4.0, A starter kit for developers,“ 12/2019: https://bit.ly/3kZZSPl.
###### [3]: „Der Digitale Zwilling in Industrie 4.0 - Eine Kurz- Einführung zu Merkmalen, Teilmodellen & Verwal- tungsschalen. (English version pending),“ 10/2020: https://bit.ly/3e6Za08.
###### [4]: „Details of the Administration Shell - from idea to implementation,“ 07/2019: https://bit.ly/2H8c2Hn.
###### [5]: „Fortschrittsbericht 2020. Industrie 4.0 gestalten. Souverän. Interoperabel. Nachhaltig (English version pending),“ 06/2020: https://bit.ly/3oaRVJe.
###### [6]: The Reference Architecture Model RAMI 4.0 and the Industrie 4.0 component, ISBN: 978-3-8007-4990-4, 2018.
###### [7]: „Structure of the Administration Shell,“ 04/2018: https://bit.ly/34jbHdo.
###### [8]:	„What is the Asset Administration Shell from a technical perspective?“ 04/2021: https://bit.ly/3d0kvbw
###### [9]:	„Drive 4.0 - Vision becomes Reality,“ 04/2018: https://bit.ly/388ST35.
###### [10]: „Which criteria do Industrie 4.0 products need to fulfil?,“ 12/2020: https://bit.ly/2Tdti0d.
###### [11]: „Interoperability by standardized properties,“ 08/2019: (available upon request) https://bit.ly/3oVQpLh.
###### [12]: „Details of the Asset Administration Shell, Part 1,“ 11/2020: https://bit.ly/3phSUYB.
###### [13]: „Details of the Asset Administration Shell, Part 2,“ 11/2020: https://bit.ly/3phSUYB.
###### [14]: „Relationships between I4.0 Components – Compo- site Components and Smart Production,“ 06/2017: https://bit.ly/37ufwP3.
###### [15]: „Secure Implementation of OPC UA for operators, integrators and manufacturers,“ 04/2018: https://bit.ly/3kZm2kJ.
###### [16]: „Examples of the Asset Administration Shell for Indus- trie 4.0 Components,“ 04/2017: https://bit.ly/2Ti9tVC.
###### [17]: „Secure Download Service,“ 10/2020: https://bit.ly/3cPSq6A
###### [18]: „Access control for Industrie 4.0 components for app- lication by manufacturers, operators and integrators,“ 12/2018: https://bit.ly/37qAJJQ.
###### [19]: „AI Application Guide,“ 09/2020: https://bit.ly/2GpHaS6.
###### [20]: „German Standardization Roadmap Industrie 4.0,“ 03/2020: https://bit.ly/3dKrRQj.
###### [21]: „Digital business models for Industrie 4.0,“ 02/2019: https://bit.ly/2FOroA6.
###### [22]: „Describing Capabilities of Industrie 4.0 Compo- nents,“ 12/2020: https://bit.ly/3tK1Uao
