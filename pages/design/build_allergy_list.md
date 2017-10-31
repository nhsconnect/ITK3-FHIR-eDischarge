---
title: Allergy List
keywords: design, build,
tags: [design]
sidebar: foundations_sidebar
permalink: build_allergy_lists.html
summary: "Constructing an allergy list"
---

{% include important.html content="The resources referenced in this section are the FHIR base resources which will be constrained by the profiles used by eDischarge, the profiles should be referred to for the actually allowable structure and content." %}

## Overview ##
This section details the design approach using FHIR resources to support the AoMRC heading model for allergies.
It is important to distinguish between two kinds of allergic reaction / adverse reaction entry in the medical record:
## Allergic Response or Adverse Reaction Event and Propensity ##
<ol>
<li>Recording an Allergic Response or Adverse Reaction to an item of medication or a substance</li>
<li>Recording a clinician’s opinion about future risk of (or propensity to) an Allergy or other Adverse Reaction if the patient is exposed to a substance.</li></ol> 

The eDischarge only records the first type of Allergic Response or Adverse Reaction i.e. the allergic event not the propensity. However there is an extension which has been added to allow recording of the probability of recurrence of the reaction (allergic, adverse, intolerant) occurring. 

## Resources Used for Profile Design ##
The FHIR resources are profiled to create the allergy list as below:

- **[ITK-Allergies-List-1](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-Allergies-List-1)** - An NHS Digital profile for recording a snapshot of the list of Allergies for the patient.
- **[CareConnect-AllergyIntolerance-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-AllergyIntolerance-1)** - A careConnect Profile for Allergies and adverse reactions. The AllergyIntolerance Resource records Risk of harmful or undesirable, physiological response which is unique to an individual and associated with exposure to a substance.
- **[ITK-Allergy-Flag-1](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-Allergy-Flag-1)** - An NHS Digital profile used to record prospective warnings of potential issues related to the patient's allergies.

## List ##
This resource acts as a container for the allergies. The following is a example of the main elements used:

- identifier - uniquely identifies this list of allergies (UUIDs)
- status - should always be "current"
- mode - should always be "snapshot" 
- subject - reference to the patient whose allergy list this is
- encounter - reference to the context in which the list was created (the inpatient stay)
- date - when the list was prepared
- source - who or what defined the list
- entry - a reference to the allergyIntolerance resource entry

## AllergyIntolerance ##
This resource details the actual allergy or adverse reaction. The following is a example of the main elements used: 

- identifier - uniquely identifies this allergy or adverse reaction (UUID)
- clinicStatus - should always be active
- category - whether the allergy or adverse reaction is to food, medication etc
- criticality - low, high, unable-to-assess etc
- code - identifies the allergy
- patient - a reference to the patient
- asserted date - date record was believed accurate
- asserter - source of the information about the allergy (patient,related person, practitioner)
- lastOccurrence - when it last occurred if known
- reaction - details of the reaction

## Flag ##
This resource is used to flag to users and systems that a allergy or adverse reaction exists. The following is an example of the main elements used: 
- identifier - uniquely identifies this flag (UUID) 
- category - of the flag
- subject - who the flag is about in this case its always the patient
- period - when flag is active
- encounter - alert relevant during encounter
- author - flag creator (practitioner, device , organization etc)

## Causative Agents ##
It is acceptable to have entries for causative agents which are similar, e.g. penicillin and amoxicillin, but have different causative agent codes. The causative agent is carried in the AllergyIntolerance resource substance element.

Where the causative agent is a drug then:

- Drug Constraint (drug) codes from the following
- NHS dm+d AMP

Or

- NHS dm+d VMP

Or

- NHS dm+d VTM

Or

- Drug Categories subset original ID 7851000000131

Where the causative agent is a food then

Food Constraint (food) codes from the following
- Food allergens subset original ID 2001000000137

Non Food Constraint (non food) codes from the following

- Non-food substance allergens subset original ID 1991000000135

It should be noted that there is overlap of content between the subsets used for food, non food and drug. E.g. it is entirely reasonable for a food to be an ingredient of a drug. 

## Allergy Snapshot ##
The allergies list is a “Snapshot” of the known allergies at a point in time (for example on discharge from hospital). It is not a master list of the patient’s allergies. Other lists of allergies for the patient may exist on other systems. 

## How the Allergy Record is constructed ##
The allergy record is constructed as a single list. The diagram below shows the Resources used and relationship between the Resources.

<img src="images/build/allergy_basic_structure.png" style="width:50%;max-width: 50%;">


Each allergy in the list will use the FHIR list resource Flag element to indicate the context of the allergy (For example addition,new etc). The Flag resource will use the common extension to reference the allergy resource.

## Allergy List Item Example ##
Example to show a allergy list.

**Allergy List**

<script src="https://gist.github.com/IOPS-DEV/cc4bc6b89141b22e06abc917b327f523.js"></script>

**Allergy Flag**

<script src="https://gist.github.com/IOPS-DEV/4a8328bfc518b7008bd7c805cde73d49.js"></script>

**AllergyIntolerance**

<script src="https://gist.github.com/IOPS-DEV/baa79022e1517c5dfebe3b5f1b8f178f.js"></script>


 



