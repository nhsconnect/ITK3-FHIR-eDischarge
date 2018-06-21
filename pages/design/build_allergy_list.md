---
title: Allergy List
keywords: design, build,
tags: [design]
sidebar: foundations_sidebar
permalink: build_allergy_lists.html
summary: "Constructing an allergy list"
---

## Overview ##
This section details the design approach using FHIR Resources to support the PRSB heading model for allergies.
It is important to distinguish between two kinds of allergic reaction / adverse reaction entry in the medical record.
## Allergic Response or Adverse Reaction Event and Propensity ##
<ol>
<li>Recording an Allergic Response or Adverse Reaction to an item of medication or a substance</li>
<li>Recording a clinician’s opinion about future risk of (or propensity to) an Allergy or other Adverse Reaction if the patient is exposed to a substance.</li></ol> 

Transfer of Care only records the first type of Allergic Response or Adverse Reaction i.e. the allergic event not the propensity.

## Resources Used for Profile Design ##
The FHIR Resources are profiled to create the allergy list as below:

- **[CareConnect-ITK-Allergy-List-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Allergy-List-1)** - An NHS Digital Profile derived from the CareConnect Profile for recording a snapshot of the list of Allergies for the patient.
- **[CareConnect-ITK-AllergyIntolerance-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-AllergyIntolerance-1)** - A NHS Digital Profile derived from the CareConnect Profile for Allergie and adverse reactions. The AllergyIntolerance Resource records risk of harmful or undesirable, physiological response which is unique to an individual and associated with exposure to a substance.

## List ##
This Resource acts as a container for the allergies. The following is an example of the main elements used:

- identifier - uniquely identifies this list of allergies (UUIDs)
- status - should always be "current"
- mode - should always be "snapshot" 
- subject - a reference to the patient whose allergy list this is
- Encounter - a reference to the context in which the list was created (the inpatient stay)
- date - when the list was prepared
- source - who or what defined the list
- entry - a reference to the allergyIntolerance Resource entry

## AllergyIntolerance ##
This Resource details the actual allergy or adverse reaction. The following is an example of the main elements used: 

- identifier - uniquely identifies this allergy or adverse reaction (UUID)
- clinicalStatus - should always be active
- category - whether the allergy or adverse reaction is to food, medication etc
- criticality - low, high, unable-to-assess etc
- code - identifies the allergy
- patient - a reference to the patient
- assertedDate  - date record was believed accurate
- asserter - the source of the information about the allergy (patient, related person, practitioner)
- lastOccurrence - when it last occurred if known
- reaction - details of the reaction

## Causative Agents ##

Guidance of the use of SNOMED CT for causative agents is as follows

Everything from the Product <b>(373873005|Pharmaceutical/biologic product(product)|)</b> hierarchy and everything from the substance <b>(105590001|substance|)</b> hierarchy. 

For pre-coordinated allergy terms use a degrade code - see below:

Degrade codes <b>(196461000000101|transfer-degraded drug allergy(record artifact)|&amp;196471000000108|transfer-degraded non-drug allergy(record artifact)|)</b> can be used if only a text representation of the allergy is known & pre coordinated allergy codes <b>(for example 213020009|egg protein allergy|)</b>.

As a SNOMED CT expression

<table><tr><td>(&lt;&lt;105590001 |Substance|
OR &lt;&lt;373873005 |Pharmaceutical / biologic product|
OR &lt;&lt;716186003 |No known allergy|
OR 196461000000101 |Transfer-degraded drug allergy|
OR 196471000000108 |Transfer-degraded non-drug allergy|)</td></tr>

(^999000801000001108 |Allergy Archetypes Drug Groups simple reference set|      
OR ^999000631000001100|National Health Service dictionary of medicines and
devices trade family simple reference set|             
OR ^999000641000001107|National Health Service dictionary of medicines and devices trade family group simple reference set|            
OR ^999000771000001105|National Health Service dictionary of medicines and devices combination drug virtual therapeutic moiety simple reference set|             
OR ^999000561000001109|National Health Service dictionary of medicines and devices virtual medicinal product simple reference set|         
OR ^999000541000001108|National Health Service dictionary of medicines and devices actual medicinal product simple reference set|             
OR ^999000791000001109|NHS dm+d (dictionary of medicines and devices) ingredient simple reference set|OR <<716186003 |No known allergy| OR 196461000000101 |Transfer-degraded drug allergy| OR 196471000000108 |Transfer-degraded non-drug allergy|)

## Severity ##

"PRSB valueSet
Mild [The reaction was mild.][SNOMED-CT::255604002] (Mild (qualifiervalue))
Moderate [The reaction was moderate.][SNOMED-CT::6736007] (Moderate (severity modifier) (qualifier value))
Severe [The reaction was severe.][SNOMED-CT::24484000] (Severe (severity modifier) (qualifier value))
Life threatening [The reaction was life-threatening.][SNOMED-CT::442452003] (Life threatening severity (qualifier value))
Fatal [The reaction was fatal.][SNOMED-CT::399166001] (Fatal (qualifier value))

reaction.severity is a Required code (mild | moderate | severe)

What about Life threatening & Fatal?

If Life threatening then map to Severe (is this OK?)

For Fatal there may be a ToC discharge, and a death notification.

No longer have a UK severity extension

As SNOMED Expression but see note above on not using 'life threatening' or 'severe':

(255604002 |Mild|
OR 6736007 |Moderate|
OR 24484000 |Severe|
OR 399166001 |Fatal|
442452003 |Life threatening severity|)
"

## certainty ##

"PRSB values are
• Unlikely        [The   reaction is  thought  unlikely  to have  been  caused  by  the  agent.]
[SNOMED-CT::1491118016]
• Likely        [The   reaction is thought  likely  to  have  been  caused  by the agent.]
[SNOMED-CT::5961011]
• Certain        [The agent is thought to be certain to have caused the reaction but this has not been confirmed by challenge testing.]
[SNOMED-CT::255545003]        (Definite        (qualifier value))
• Confirmed by  challenge  testing  [The  reaction to the agent has been confirmed by challenge testing or other concrete evidence.]
[SNOMED-CT::410605003]        (Confirmed present (qualifier value))

verficationStatus is mandatory

verficationStatus has a Required valueSet (unconfirmed | confirmed | refuted | entered-in-error)

""Profile out"" ( refuted | entered-in-error)

Certain & Confirmed by Challenge = confirmed; Likely & Unlikely = unconfirmed [DB post comment on Zulip]

If verificationStatus is not known, then set to unconfirmed. If exta information about certainty is known, this should reported as a note

 remove SNOMED-extension from careconnect
01feb2018: The value set is required in FHIR and can't changed and we have mapped it as above, the proposal is to remove the SNOMED certainty extension. 
Proposed guidance for System suppliers to default to unconfirmed for all meesages.

As SNOMED Expressions (Note that 1491118016 |unlikely| and 5961011 |likely|  above are desription identifiers for synonyms of concepts below)

(385434005 |Improbable diagnosis|
OR 2931005 |Probable diagnosis|
OR 255545003 |Definite|
OR 410605003 |Confirmed present|)"

## Reaction details ##
"This is part of reaction, which is optional (0..*) - so if there is no manifestation known, then don't send a reaction section

Anything from the clinical finding hierarchy ( 404684003 | clinical finding (finding) | ) PLUS the HL7 nullFlavors documented here

CodeableConcept is Extensible

If you have a code, then goes in Manifestation CodeableConcept.

Where no code is known (but a manifestation needs to be recorded) then populate the Manifestation CodeableConcept with the HL7 FHIR nullFlavor ""UNC"" - ""un-encoded"" & text of manifestation in reaction.description

When patient is asked about reaction, but doesn't know the reaction then use HL7 nullFlavor ""ASKU"" - ""asked but unknown""

When the reaction details cannot be determined/verified, then use the HL7 nullFlavor ""NI"" - ""No Information"""

## Type of Reaction ##

"FHIR lists a Required valueSet of (allergy | intolerance) - as this is a required valueSet these values must be used.

What about ""Adverse Reaction"" & ""Not Known""? [See Zulip post https://chat.fhir.org/#narrow/stream/implementers/topic/Extensions.20on.20Required.20Codes for international debate on adding codes to AllergyIntolerance.type]
Adverse reactions is closer to Intoleranceby FHIR definition.
An absence of AllergyIntollerance.type implies Not Known .

15/05/2018: FHIR patient care WGM: adverse reaction recorded under reaction.description."

## Date first experienced ##

"Mapped to the ""higher level""   AllergyIntolerance.onset[x]
Estimated or actual date, date-time, or age when allergy or intolerance was identified.
        
Reaction.onset definittion: Record of the date and/or time of the onset of the Reaction.
The reason for mapping to higher onset is that this is the date when the reaction was experinced by the patient for the first time , the onset under reaction could be multiple. 

Raise to international FHIR re onset reaction having age and text. :Jennifer
"

## Allergy Snapshot ##
The allergies list is a “Snapshot” of the known allergies at a point in time (for example on discharge from hospital). It is not a master list of the patient’s allergies. Other lists of allergies for the patient may exist on other systems. 

## How the Allergy List is Constructed ##
The allergy record is constructed as a single list. The diagram below shows the Resources used and relationships between the Resources.

<img src="images/build/allergy_basic_structure.png" style="width:100%;max-width: 100%;">


Each allergy in the list will use the FHIR list Resource Flag element to indicate the context of the allergy (For example unchanged, new etc). 

## Allergy Flag Structures ##

<img src="images/build/allergy_flag_structure.png" style="width:100%;max-width: 100%;">

## How to Represent "No Known Allergies" ## 
When there is a positive statement that the patient has "No known allergies" then no coded structure is sent. Please refer to the [Allergy and Adverse Reactions](explore_allergies_and_adverse_reactions.html) section for how to send the information as narrative text.

## How to Represent "No Known Allergies" ## 
<br/>First option: Send coded 'No Known Allergies' .Generic issue of handling negation, Initial Proposal :if there are active allergy records , these positive presence of allergies should not be sent with 'No Known Allergies'. Other option is to use the list resource and use 'EmptyReason' to send No Known Allergy as text.
## Allergy List Item Example ##

Example to show an allergy list.

**Allergy List**

<script src="https://gist.github.com/IOPS-DEV/cc4bc6b89141b22e06abc917b327f523.js"></script>


**AllergyIntolerance**

<script src="https://gist.github.com/IOPS-DEV/baa79022e1517c5dfebe3b5f1b8f178f.js"></script>


 



