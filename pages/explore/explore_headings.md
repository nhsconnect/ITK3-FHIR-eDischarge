---
title: eDischarge Headings
keywords:  messaging
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_headings.html
summary: "Overview of the eDischarge headings"
---

{% include custom/search.warnbanner.html %}

## Overview ##

This section provides a list of the AMoRC headings used for text sections in the ITK3 FHIR eDischarge based on the "Standards for the clinical structure and content of patient records" documentation. 

This section lists the following

- The headings used
- An overview of the type of information carried within the text section
- An example of a text section instance
- A list of the coded resources which may be used to give the text carried in the section in a coded format. 

## Typical Text Section Content ##
This diagram shows a typical text section.
Note: the examples of section html in this specification show only example html format such as tables. This is a exemplar format. There is no mandated format for the section html. 

<img src="images/explore/section_description.png" style="width:90%;max-width: 90%;">
 
The text sections are carried in the FHIR composition resource. 

This is profiled as the [ITK3-EDIS-Compostion](http://FHIRxxxxxxxxxxxx)


{% include custom/section.warnbanner.html %}


{% include custom/messaging_overview.svg %}