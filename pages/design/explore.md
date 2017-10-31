---
title: Messaging Architecture Overview
keywords:  messaging
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore.html
summary: "Overview of the Messaging Architecture section"
---

{% include custom/search.warnbanner.html %}


## Pre-Requisites for FHIR ITK3 Messaging Solutions ##

## ITK3 Messaging Requirements ##

- SHALL support HL7 FHIR version STU3
- When using ITK and MESH SHALL Implement ITK Sender and/or Receiver Responsibilities as per [ITK Sender and Receiver Requirements ](..\explore_snd&rec_req.html)
- Resources sent SHALL identify the CareConnect profile where a CareConnect profile is included in the bundle using the [FHIR Base Resource](https://hl7.org/fhir/resource-definitions.html#Resource.meta)
- SHALL support XML format for all NHS Digital ITK interactions.


## FHIR Conformance ##

- SHOULD declare a Conformance identifying the list of profiles and message bundles supported.






