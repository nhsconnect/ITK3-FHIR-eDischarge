---
title: Condition
keywords: design, build,
tags: [design]
sidebar: foundations_sidebar
permalink: build_conditions.html
summary: "Constructing a condition"
---

{% include important.html content="The resources referenced in this section are the FHIR base resources which will be constrained by the profiles used by eDischarge, the profiles should be referred to for the actually allowable structure and content." %}

## Overview ##
This section details the design approach using FHIR resources to support the AoMRC heading model which use the condition resource. The condition resource is directly referenced from the Diagnosis section and may also used as the reason for medication.


## Resources Used for Profile Design ##
The following FHIR resources are profiled to create the condition.

- **[CareConnect-ITK-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Condition-1)** -	A CareConnect derived NHS Digital Profile for conditions. The Condition resource records detailed information about conditions or diagnoses recognised by a clinician.

## Condition ##
This resource is used to record detailed information about a condition, problem, diagnosis, or other event, situation, issue, or clinical concept that has risen to a level of concern.The following is a example of the elements that can be used: 

- identifier - uniquely identifies this condition (UUIDs)
- clincalStatus - 	active, recurrence, inactive, remission, resolved etc
- category - for eDischarge this will normally be encounter-diagnosis
- Severity - subjective severity of condition
- code - identification of the condition, problem or diagnosis
- bodySite - anatomical location, if relevant
- subject - the patient
- onset - estimated or actual date, date-time, or age
- abatement - if/when in resolution/remission
- stage - stage/grade, usually assessed formally
- evidence - supporting evidence


**Condition Example**

<script src="https://gist.github.com/IOPS-DEV/ea2e64e747535e801f2451f6fec044c3.js"></script>




 
{% include custom/provide_messaging.svg %}


