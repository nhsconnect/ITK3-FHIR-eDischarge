---
title: Procedure
keywords: design, build,
tags: [design]
sidebar: foundations_sidebar
permalink: build_procedures.html
summary: "Constructing a procedure"
---

{% include important.html content="The resources referenced in this section are the FHIR base resources which will be constrained by the profiles used by eDischarge, the profiles should be referred to for the actually allowable structure and content." %}

## Overview ##
This section details the design approach using FHIR resources to support the AoMRC heading model which use the procedure resource. The procedure resource is directly referenced from the procedure section and may also used by other resources such as indication within the encounter resource.


## Resources Used for Profile Design ##
The following FHIR resources are profiled to create the condition.

- **Procedure** profiled as [CareConnect-ITK-Procedure-1](http:\\xxxx)

## Procedure ##
This resource is used to record detailed information about a procedure.The following is a example of the elements that can be used: 

- identifier - uniquely identifies this procedure (UUIDs)
- category - surgical, diagnostic etc 
- Severity - subjective severity of condition
- code - identification of the procedure
- bodySite - anatomical location, if relevant
- subject - the patient
- outcome - the result of procedure


**Condition Example**

<script src="https://gist.github.com/IOPS-DEV/8744f772a7e09e862fbb8714c1647e0a.js"></script>




 
{% include custom/provide_messaging.svg %}

