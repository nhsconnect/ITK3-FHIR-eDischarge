---
title: Medication List
keywords: design, build,
tags: [design]
sidebar: foundations_sidebar
permalink: build_medication_lists.html
summary: "Constructing a medication list"
---

{% include important.html content="The resources referenced in this section are the FHIR base resources which will be constrained by the profiles used by eDischarge, the profiles should be referred to for the actually allowable structure and content." %}

## Overview ##
This section details the design approach using FHIR resources to support the AoMRC heading model for medication and devices.


## Medication Snapshot ##
The medication list is a “Snapshot” of the medication at a point in time (for example on discharge from hospital). It is not a master list of the patient’s medications. Other lists of medications for the patient may exist on other systems. 

## Resources Used for Profile Design ##
The FHIR resources are profiled to create the medication list as below:

- **[ITK-Medication-List-1](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-Medication-List-1)** - An NHS Digital Profile for recording a snapshot of the list of Medications for the patient.
- **[CareConnect-MedicationStatement-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-MedicationStatement-1)** - A CareConnect Profile for medication statements. The MedicationStatement Resource is a record of a medication that is being consumed by a patient.
- **[CareConnect-Medication-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Medication-1)** - A CareConnect Profile for medication. The Medication Resource is primarily used for the identification and definition of a medication.
- **[CareConnect-ITK-Medication-Flag-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Medication-Flag-1)** - An NHS Digital Profile for medication flags. The Flag Resource carries prospective warnings of potential issues related to the patient's medications.

## List ##
This resource acts as a container for the medication. The following is a example of the elements which can be used:

- identifier - uniquely identifies this list of medication (UUIDs)
- status - active, completed, stopped etc
- subject - reference to the patient whose medication list this is
- encounter - reference to the context in which the list was created (the inpatient stay)
- date - when the list was prepared
- source - who or what defined the list
- entry - a reference to the MedicationStatement resource entry
- flag - the type of medication entry (additional, discontinued etc.)

## MedicationStatement ##
A record of a medication that is being consumed by a patient.The following is a example of the elements that can be used:

- identifier - uniquely identifies this medication statement (UUID)
- clinicStatus - should always be active
- category - should be inpatient
- medication -the medication coded (a SNOMED CT Concept that identifies this medication) or a reference to the medication resource which details the medication. Note: the reference to medication resource allows a much richer description of the medication and should always be used if possible. 
- effective - the date/time or interval when the medication was taken
- dateAsserted - When the statement was asserted?
- informationSource - Person or organization that provided the information about the taking of this medication
-  reasonCode - Reason for why the medication is being/was taken
-  reasonReference - a reference to the condition or observation resource that supports why the medication is being/was taken 
-  dosage - Details of how medication is/was taken or should be taken

## Medication ##
The Medication resource allows for medications to be characterized by the form of the drug and the ingredient (or ingredients), as well as how it is packaged. The medication will include the ingredient(s) and their strength(s) and the package can include the amount (for example, number of tablets, volume, etc.) that is contained in a particular container (for example, 100 capsules of Amoxicillin 500mg per bottle).The following is a example of the elements that can be used:

- code - a SNOMED CT Concept that identifies this medication
- form - powder, tablets, capsule etc SNOMED CT form concepts
- ingredient - active or inactive ingredient
- package - details about packaged medications
- batch - 	Identifies a single production run 
 
## How the Medication Record is Constructed ##
The medication record is constructed as a single list. The diagram below shows the Resources used and relationship between the Resources.

<img src="images/build/medication_basic_structure.png" style="width:50%;max-width: 50%;">


There will be one medication statement for each of the medication items contained in the list.
Each medication statement should have a medication, however it is possible in some cases that the medication is described in the medication statement because the medication cannot be fully coded within the medication Resource. 
The medication Flag element of the List Resource will indicate the context of the medication statement(for example additional, discontinuation etc). the list of values for this is based on the FHIR value set [Patient Medicine Change Types](http://hl7.org/fhir/valueset-list-item-flag.html)  with additional and/or different values for NHS/ITK use. 

## Changing Medication Illustration ##

The list will use the FHIR Flag element of the list resource to indicate the context of the medication of statement, in this case the first in the list will be flagged as a discontinuation and the second as an additional medication. 

<img src="images/build/medication_change.png" style="width:80%;max-width: 80%;">

## Do Not Discontinue Medication Illustration ##
In the illustration below, a new medication is flagged as “Do not Discontinue” using the Flag resource. The Flag resource references the medication statement resource using the common extension.

<img src="images/build/medication_do_not_discon.png" style="width:80%;max-width: 80%;"> 

## Medication List Item Example ##
Example to show a discontinuation of a drug, which is replaced by a stronger dose with a Flag to show that the new medication should not be discontinued.

**Medication List**

The list part of the record. 
<script src="https://gist.github.com/IOPS-DEV/396128c150948b3de78014ad7f2b8e4e.js"></script>

**Medication Discontinuation**

The medication being discontinued.
<script src="https://gist.github.com/IOPS-DEV/608bf5c9d3e200ef19f10ff1bf33244c.js"></script>

**Medication Addition**

The replacement for the medication discontinued.
<script src="https://gist.github.com/IOPS-DEV/3e1e9c7cbab951dbb7d2861b63d811d4.js"></script>

**Do Not Discontinue Flag**

This is a flag to indicate that the new stronger medication should not be discontinued.
<script src="https://gist.github.com/IOPS-DEV/368ab3e1b84967a7ca9ce098f40c9a0b.js"></script>
 



