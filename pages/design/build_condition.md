---
title: Condition List
keywords: design, build,
tags: [design]
sidebar: foundations_sidebar
permalink: build_conditions.html
summary: "Constructing a condition list"
---


## Overview ##
This section details the design approach using FHIR resources to support the PRSB heading model for a condition list. The condition resource is reference via the List resource.

## Resources Used for Profile Design ##
The following FHIR resources are profiled to create the condition list.

- **[CareConnect-ITK-Condition-List-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Condition-List-1)** - A CareConnect derived NHS Digital Profile for recording a snapshot of the list of Conditions for the patient.
- **[CareConnect-ITK-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Condition-1)** -	A CareConnect derived NHS Digital Profile for conditions. The Condition resource records detailed information about conditions (diagnoses) recognised by a clinician.

## List ##
This resource acts as a container for the conditions. The following is an example of the main elements used:

- identifier - uniquely identifies this list of conditions (UUIDs)
- status - should always be "current"
- mode - should always be "snapshot" 
- subject - a reference to the patient whose condition list this is
- encounter - a reference to the context in which the list was created (the inpatient stay for example)
- date - when the list was prepared
- source - who or what defined the list
- entry - a reference to the condition resource entry

## Condition ##
This resource is used to record detailed information about a condition, problem, diagnosis, or other event, situation, issue, or clinical concept that has risen to a level of concern.The following is an example of the elements that can be used: 

- identifier - uniquely identifies this condition (UUIDs)
- clinicalStatus - 	active, recurrence, inactive, remission, resolved etc
- category - for eDischarge this will normally be encounter-diagnosis
- Severity - subjective severity of condition
- code - identification of the condition, problem or diagnosis
- bodySite - anatomical location, if relevant
- subject - the patient
- onset - estimated or actual date, date-time, or age
- abatement - if/when in resolution/remission
- stage - stage/grade, usually assessed formally
- evidence - supporting evidence

## How the Condition List is Constructed ##
The condition list is constructed as a single list. The diagram below shows the Resources used and relationships between the Resources.

<img src="images/build/condition_basic_structure.png" style="width:100%;max-width: 100%;">

Each condition in the list will use the FHIR list resource Flag element to indicate the context of the condition (For example primary, secondary etc). 

**Important Note - The value set for the condition list flag element is currently under review and subject to change.**

## Condition Flag Structures ##

<img src="images/build/condition_flag_structure.png" style="width:100%;max-width: 100%;">

## Condition List Item Example ##

Example to show an condition list.

**Condition List**

<script src="https://gist.github.com/IOPS-DEV/91086467307034d0267855f23b37c503.js"></script>

**Condition**

<script src="https://gist.github.com/IOPS-DEV/ea2e64e747535e801f2451f6fec044c3.js"></script>




 



