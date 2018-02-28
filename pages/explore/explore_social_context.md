---
title: Social Context Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_social_context.html
summary: "Gives information about the Social context section"
---

{% include custom/section.warnbanner.html %}

## Social Context Section Content##
The Social context section carries information about the social context of the patient, subheadings should be formatted as such in any html sent:

<table width="100%">
<tr>
<th width="25%">Sub-section</th>
<th width="45%">Description</th>
<th width="15%">Cardinally</th>
<th width="15%">Conformance</th>
</tr>
<tr>
<td>Household composition</td>
<td>Eg: lives alone, lives with family, lives with partner, etc. This may be plain text.>/td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Occupational history</td>
<td>The current and/or previous relevant occupation(s) of the patient/individual.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Educational history</td>
<td>The current and/or previous relevant educational history of the patient/individual.</TD>
<td>1..1</td>
<td>Mandatory</td>
</tr>
</table>

##  Example Social Context Section ##

<script src="https://gist.github.com/IOPS-DEV/73932c1d2ee99e5fd832bcbfa1922092.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK FHIR eDischarge does not currently support coded Social context information.






