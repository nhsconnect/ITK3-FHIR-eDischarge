---
title: Bundle Structure
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_bundle_structures.html
summary: "The structures of the bundle used for ITK3 FHIR Documents"
---

{% include custom/search.warnbanner.html %}



## Background ##
To enable a standardised structure to carry information regarding common end-to-end distribution requirements, two profiles have been defined, the ITK Message Bundle and the ITK Message Header that combine to make up the ITK3 Distribution Bundle. This is used with the ITK3 FHIR document Bundle. The combination of these bundles is referred to as the the eDischarge Bundle.

## The ITK3 eDischarge Bundle ##

The diagram below is an example of a ITK FHIR document payload that may be used with the ITK3 eDischarge Bundle. When sending FHIR Documents the is a bundle of type document.

<img src="images/explore/ITKDocExample.png" style="width:60%;max-width: 60%; style="height:100%;max-height: 100%;" >


{% include custom/messaging_overview.svg %}









