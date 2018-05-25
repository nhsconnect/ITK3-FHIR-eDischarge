---
title: Allergy List
keywords: design, build,
tags: [design]
sidebar: foundations_sidebar
permalink: build_allergy_lists.html
summary: "Constructing an allergy list"
---

## Overview ##
This section details the design approach using FHIR resources to support the PRSB heading model for allergies.
It is important to distinguish between two kinds of allergic reaction / adverse reaction entry in the medical record:
## Allergic Response or Adverse Reaction Event and Propensity ##
<ol>
<li>Recording an Allergic Response or Adverse Reaction to an item of medication or a substance</li>
<li>Recording a clinician’s opinion about future risk of (or propensity to) an Allergy or other Adverse Reaction if the patient is exposed to a substance.</li></ol> 

Transfer of Care only records the first type of Allergic Response or Adverse Reaction i.e. the allergic event not the propensity.

## Resources Used for Profile Design ##
The FHIR resources are profiled to create the allergy list as below:

- **[CareConnect-ITK-Allergy-List-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Allergy-List-1)** - An NHS Digital Profile for recording a snapshot of the list of Allergies for the patient.
- **[CareConnect-ITK-AllergyIntolerance-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-AllergyIntolerance-1)** - A CareConnect derived Profile for Allergies and adverse reactions. The AllergyIntolerance Resource records risk of harmful or undesirable, physiological response which is unique to an individual and associated with exposure to a substance.

## List ##
This Resource acts as a container for the allergies. The following is an example of the main elements used:

- identifier - uniquely identifies this list of allergies (UUIDs)
- status - should always be "current"
- mode - should always be "snapshot" 
- subject - a reference to the patient whose allergy list this is
- encounter - a reference to the context in which the list was created (the inpatient stay)
- date - when the list was prepared
- source - who or what defined the list
- entry - a reference to the allergyIntolerance Resource entry

## AllergyIntolerance ##
This Resource details the actual allergy or adverse reaction. The following is an example of the main elements used: 

- identifier - uniquely identifies this allergy or adverse reaction (UUID)
- clinicStatus - should always be active
- category - whether the allergy or adverse reaction is to food, medication etc
- criticality - low, high, unable-to-assess etc
- code - identifies the allergy
- patient - a reference to the patient
- asserted date - date record was believed accurate
- asserter - the source of the information about the allergy (patient, related person, practitioner)
- lastOccurrence - when it last occurred if known
- reaction - details of the reaction

## Causative Agents ##
It is acceptable to have entries for causative agents which are similar, e.g. penicillin and amoxicillin, but have different causative agent codes. The causative agent is carried in the AllergyIntolerance Resource substance element.

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

It should be noted that there is an overlap of content between the subsets used for food, non food and drug. E.g. it is entirely reasonable for a food to be an ingredient of a drug. 

## Allergy Snapshot ##
The allergies list is a “Snapshot” of the known allergies at a point in time (for example on discharge from hospital). It is not a master list of the patient’s allergies. Other lists of allergies for the patient may exist on other systems. 

## How the Allergy List is Constructed ##
The allergy record is constructed as a single list. The diagram below shows the Resources used and relationships between the Resources.

<img src="images/build/allergy_basic_structure.png" style="width:100%;max-width: 100%;">


Each allergy in the list will use the FHIR list Resource Flag element to indicate the context of the allergy (For example unchanged, new etc). 

## Allergy Flag Structures ##

<img src="images/build/allergy_flag_structure.png" style="width:100%;max-width: 100%;">

## How to Represent "No Know Allergies" ## 
When there is a positive statement that the patient has "No know allergies" then no coded structure is sent. Please refer to the [Allergy and Adverse Reactions](explore_allergies_and_adverse_reactions.html) section for how to send the information as narrative text.

## Allergy List Item Example ##

Example to show an allergy list.

**Allergy List**

<script src="https://gist.github.com/IOPS-DEV/cc4bc6b89141b22e06abc917b327f523.js"></script>


**AllergyIntolerance**

<script src="https://gist.github.com/IOPS-DEV/baa79022e1517c5dfebe3b5f1b8f178f.js"></script>


 



