---
title: Procedure List
keywords: design, build,
tags: [design]
sidebar: foundations_sidebar
permalink: build_procedures.html
summary: "Constructing a procedure list"
---

## Overview ##
This section details the design approach using FHIR resources to support the PRSB heading model which use the procedure resource. The Procedure resource is referenced via the List resource.

## Resources Used for Profile Design ##
The FHIR resources are profiled to create the procedure list as follows:

- **[CareConnect-ITK-Procedure-List-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Procedure-List-1)** - A CareConnect derived NHS Digital Profile for recording a snapshot of the list of Procedures for the patient.
- **[CareConnect-ITK-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Procedure-1)** - A CareConnect derived NHS Digital Profile for procedures. The Procedure resource is used to record an action that is or was performed on a patient.

## List ##
This resource acts as a container for the procedures. The following is an example of the main elements used:

- identifier - uniquely identifies this list of procedures (UUIDs)
- status - should always be "current"
- mode - should always be "snapshot" 
- subject - a reference to the patient whose procedure list this is
- encounter - a reference to the context in which the list was created (the inpatient stay for example)
- date - when the list was prepared
- source - who or what defined the list
- entry - a reference to the procedure resource entry

## Procedure ##
This resource is used to record detailed information about a procedure.The following is a example of the elements that can be used: 

- identifier - uniquely identifies this procedure (UUIDs)
- status - completed, aborted etc 
- category - Classification of the procedure
- code - identification of the procedure
- performed - when procedure was performed
- subject - the patient
- outcome - the result of procedure

## How the Procedure List is Constructed ##
The Procedure list is constructed as a single list. The diagram below shows the Resources used and relationships between the Resources.

<img src="images/build/procedure_basic_structure.png" style="width:100%;max-width: 100%;">

## Procedure List Item Example ##

Example to show an procedure list

**Procedure List**

<script src="https://gist.github.com/IOPS-DEV/204999ed7c143fe59fa754b8f0b49bad.js"></script>

**Procedure Example**

<script src="https://gist.github.com/IOPS-DEV/8744f772a7e09e862fbb8714c1647e0a.js"></script>

 



