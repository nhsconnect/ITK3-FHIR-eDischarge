---
title: Participation in Research Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_part_research.html
summary: "Gives information about the Participation in research section"
---

{% include custom/section.warnbanner.html %}

## Participation in Research Section Content##
This is to flag participation in a clinical trial.Subheadings should be formatted as such in any html sent:

<table width="100%">
<tr>
<th width="25%">Sub-section</th>
<th width="45%">Description</th>
<th width="15%">Cardinally</th>
<th width="15%">Conformance</th>
</tr>
<tr>
<td>Participation in research</td>
<td>This may include whether participation in a trial has been offered, refused or
accepted, the name of the trial, drug/intervention tested, enrolment date, duration
of treatment and follow up, and contact number for adverse events or queries.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
</table> 

##  Example Participation in Research Section ##

<script src="https://gist.github.com/IOPS-DEV/9cd8f422a7c1e323ed42ac424a5830db.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK FHIR eDischarge does not currently support coded participation in research information.






