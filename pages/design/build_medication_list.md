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
This section details the design approach using FHIR Resources to support the AoMRC heading model for medication and devices.


## Medication Snapshot ##
The medication list is a “Snapshot” of the medication at a point in time (for example on discharge from hospital). It is not a master list of the patient’s medications. Other lists of medications for the patient may exist on other systems. 

## Resources Used for Profile Design ##
The FHIR Resources are profiled to create the medication list as below:

- **[CareConnect-ITK-Medication-List-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Medication-List-1)** - An NHS Digital Profile for recording a snapshot of the list of Medications for the patient.
- **[CareConnect-ITK-MedicationStatement-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-MedicationStatement-1)** - An NHS Digital Profile for medication statements. The MedicationStatement Resource is a record of a medication that is being consumed by a patient.
- **[CareConnect-ITK-Medication-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Medication-1)** - An NHS Digital Profile for medication. The Medication Resource is primarily used for the identification and definition of a medication.

## List ##
This Resource acts as a container for the medication items. The following is an example of the elements which can be used:

- identifier - uniquely identifies this list of medication (UUID)
- status - active, completed, stopped etc
- subject - a reference to the patient whose medication list this is
- encounter - a reference to the context in which the list was created (the inpatient stay)
- date - when the list was prepared
- source - who or what defined the list
- entry - a reference to the MedicationStatement Resource entry
- flag - the type of medication entry (additional, discontinued etc.)

## MedicationStatement ##
A record of a medication that is being consumed by a patient. The following is an example of the elements that can be used:

- identifier - uniquely identifies this medication statement (UUID)
- clinicalStatus - should always be active
- category - should be inpatient
- medication - the medication coded (a SNOMED CT Concept that identifies this medication), this is done by reference to the Medication Resource which details the medication. 
- effective - the date/time or interval when the medication was taken
- dateAsserted - When the statement was asserted?
- informationSource - Person or organization that provided the information about the taking of this medication
- reasonCode - Reason for why the medication is being/was taken
- reasonReference - a reference to the condition or observation Resource that supports why the medication is being/was taken 
- dosage - Details of how medication is/was taken or should be taken

## Medication ##
The Medication Resource allows for medications to be characterized by the form of the drug and the ingredient (or ingredients), as well as how it is packaged. The medication will include the ingredient(s) and their strength(s) and the package can include the amount (for example, number of tablets, volume, etc.) that is contained in a particular container (for example, 100 capsules of Amoxicillin 500mg per bottle).The following is a example of the elements that can be used:

- code - a SNOMED CT Concept that identifies this medication
- form - powder, tablets, capsule etc SNOMED CT form concepts
- ingredient - active or inactive ingredient
- package - details about packaged medications
- batch - 	Identifies a single production run 
 
## How the Medication List is Constructed ##
The medication record is constructed as a single list. The diagram below shows the Resources used and the relationship between the Resources.

<img src="images/build/medication_basic_structure.png" style="width:100%;max-width: 100%;">


There will be one medication statement for each of the medication items contained in the list.
Each medication statement should have a medication, however it is possible in some cases that the medication is described in the medication statement because the medication cannot be fully coded within the medication Resource. 
The entry.flag element of the List Resource will indicate the context of the medication statement(for example additional, discontinuation etc). the list of values for this is based on the FHIR value set [Patient Medicine Change Types](http://hl7.org/fhir/valueset-list-item-flag.html)  with additional and/or different values for NHS/ITK3 use. 

## Medication Flag Structures ##

<img src="images/build/medication_flag_structure.png" style="width:100%;max-width: 100%;">

## Changing Medication Illustration ##

The list will use the FHIR Flag element of the List Resource to indicate the context of the MedicationStatement, in this case the first in the list will be flagged as obsolete and the second as a new medication. 

<img src="images/build/medication_change_structure.png" style="width:100%;max-width: 100%;">

## Changing Medication Example ##

### Medication List ###

**The list part of the record.** 

<script src="https://gist.github.com/IOPS-DEV/396128c150948b3de78014ad7f2b8e4e.js"></script>

### Medication Changed ###

**The medication being stopped.**

<script src="https://gist.github.com/IOPS-DEV/608bf5c9d3e200ef19f10ff1bf33244c.js"></script>

<script src="https://gist.github.com/IOPS-DEV/5141e4cfc8480c8b4638d30ad03c564b.js"></script>

**The new medication.** 

<script src="https://gist.github.com/IOPS-DEV/eaf5f7159b9925448d8b479177c244f3.js"></script>

<script src="https://gist.github.com/IOPS-DEV/71435b5b230677181ded2c81506f3e21.js"></script>


 



