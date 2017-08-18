---
title: Resource referencing
keywords: resource
tags: [development,fhir,profiles]
sidebar: overview_sidebar
permalink: explore_resource_referencing.html
summary: "Resource referencing explained."
---

{% include custom/search.warnbanner.html %}

## Overview ##
This section details the reference between resources.

## ITK eDischarge FHIR Document Profile Referencing ##

The diagram shows the referencing between the profiles in the bundle which make up the ITK eDischarge FHIR Document.

When using ITK3 there is an outer bundle structure which is called the [ITK3 send payload bundle structure](https://nhsconnect.github.io/ITK3-FHIR-Messaging-Distribution/explore_messages.html#itk-send-payload-bundle-diagram) for use with ITK3.

<img src="images/explore/eDischarge_message_bundle.png" style="width: 75%;max-width: 75%;"> 



## Practitioner and Organization Referencing Diagram ##

The diagram shows the referencing between organization, practitioner and practitionerRole which applies to all the message in the ITK eDischarge specification.


<img src="images/explore/org_pra_references.png" style="width: 75%;max-width: 75%;"> 
