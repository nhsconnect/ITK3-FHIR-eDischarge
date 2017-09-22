---
title: Observation
keywords: design, build,
tags: [design]
sidebar: foundations_sidebar
permalink: build_observations.html
summary: "Constructing a observation"
---

{% include important.html content="The resources referenced in this section are the FHIR base resources which will be constrained by the profiles used by eDischarge, the profiles should be referred to for the actually allowable structure and content." %}

## Overview ##
This section details the design approach using FHIR resources to support the AoMRC heading model which use the observation resource. The observation resource is referenced from the Condition resource.


## Resources Used for Profile Design ##
The following FHIR resources are profiled to create the observation.

- **Observation** profiled as [CareConnect-Observation-1](http:\\xxxx)

## Observation ##
This resource is used to record information tracking the current and historical observations that have been made for a patient.The following is a example of the elements that can be used: 

- identifier - uniquely identifies this observation (UUIDs)
- Status - 	registered,preliminary,final,amended etc
- code - identification of the observation
- performer - who made the observation
- subject - the patient
- interpretation - High,Low, Normal etc
- bodySite - the part of the body the observation was made about
- method - How it was done 


**Observation Example**

To Follow.


 
{% include custom/provide_messaging.svg %}

