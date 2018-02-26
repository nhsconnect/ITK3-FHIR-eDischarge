---
title: GP Practice Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_gp_practice.html
summary: "Gives information about the patient's GP Practice"
---
{% include custom/section.warnbanner.html %}


## GP Practice Section Content##

The GP practice section contains details of the patients GP practice, subheadings should be rendered as such in any html sent:
 
<table width="100%">
<tr>
<th width="25%">Sub-section</th>
<th width="45%">Description</th>
<th width="15%">Cardinally</th>
<th width="15%">Conformance</th>
</tr>
<tr>
<td>GP practice identifier</td>
<td>The identifier of the registered GP Practice.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>GP name</td>
<td>Where the patient or patient's representative offers the name of a GP as their usual GP.</td>
<td>0..1</td>
<td>Required</td>
</tr>
<tr>
<td>GP practice details</td>
<td>Name and address of the patient's registered GP Practice.
</td>
<td>0..1</td>
<td>Required</td>
</tr>
</table>

The PractitionerRole resource is included to allow identification of the practitioner in the role of GP. 

## Example GP Practice Using Organization Resource ##

<script src="https://gist.github.com/IOPS-DEV/96ebbfe2e8f8f58ca820c7fb0a278bd5.js"></script>

## Example GP Name Using Practitioner Resource ##

Note: The GP is linked to the GP Practice by the Practitioner resource referencing the organization resource using the managingOrganization element. The PractitionerRole resource identifies the practitioner in the role of GP.

<script src="https://gist.github.com/IOPS-DEV/3f5d3d112a125a0d28f449964e0a26c5.js"></script>




