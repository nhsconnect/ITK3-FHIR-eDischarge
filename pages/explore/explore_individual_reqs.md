---
title:  Individual Requirements Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_individual_reqs.html
summary: "Gives information about the Individual requirements section"
---

{% include custom/section.warnbanner.html %}

## Individual Requirements Section Content ##
The Individual requirements section carries information about the individual requirements of the patient,items in bold are subheadings and should be formatted as such in any html sent:


 
<table width="100%">
<tr>
<th width="25%">Sub-section</th>
<th width="45%">Description</th>
<th width="15%">Cardinally</th>
<th width="15%">Conformance</th>
</tr>
<tr>
<td>Individual requirement</td>
<td>Individual requirements that a person has. These may be communication, cultural, cognitive or mobility needs.
</td>
<td>0..1</td>
<td>Required</td>
</tr>
</table>

##  Example Individual Requirements Section ##

<script src="https://gist.github.com/IOPS-DEV/497e71d591b9041c318dc4c88517287b.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK FHIR eDischarge does not currently support coded individual requirements information.






