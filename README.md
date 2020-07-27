# Question-and-Answers

**How shall a link to a website be entered in an AAS, as File or as ReferenceElement object?**

Links to websites shall be entered as File object (physical reference). ReferenceElement  objects represent logical references.
A typical usage for logical references is in the description of a topology of the asset or „consist of” hierarchies.


**If the same properties are use in several submodels, shall they also be entered several times or shall they be referenced?**

Submodels shall be as independent as possible so that they can be changed and developed separately.
Consequently, the same properties shall be copied to another submodel and references shall not be used in such case. 
The concept description referenced in semanticId, however, should be the same.

**How to use physical units for quantifiable properties?**

AAS defines specific constructs of unit and unitID for concept descriptions (template DataSpecificationIEC61360).
We advise you to use unitIDs  that refer to pre-defined eCl@ss IRDIs, e.g., 0173-1#05-AAA480#002  for millimeters. 
In a non-likely case of non-existent global IRDI for a unit, please follow the general guidance for custom semantic IDs
to create a custom unitID.
