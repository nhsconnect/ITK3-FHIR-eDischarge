---
title: Person Completing Record Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_per_com_record.html
summary: "Gives information about the Person completing record section"
---

{% include custom/section.warnbanner.html %}

## Person Completing Record Section Content##
The Person completing record section carries information about the person who completed the record.Subheadings  should be formatted as such in any html sent.

<table width="100%">
<tr>
<th width="25%">Sub-section</th>
<th width="45%">Description</th>
<th width="15%">Cardinally</th>
<th width="15%">Conformance</th>
</tr>
<tr>
<td>Name</td>
<td></td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Designation or role</td>
<td></td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Grade</td>
<td></td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Specialty</td>
<td></td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<td>Date completed</td>
<td></td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
</table> 

## Example Person Completing Record Section ##

<script src="https://gist.github.com/IOPS-DEV/4eceababbca389067cde4aefd2d61cde.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK FHIR eDischarge does not currently support coded Person completing record information.






