---
title: Discharge Details Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_discharge_details.html
summary: "Gives information about the Discharge details section"
---

{% include custom/section.warnbanner.html %}

## Discharge Details Section Content##
The Discharge details section carries details of the patient's discharge, items in bold are subheadings and should be formatted as such in any html sent:

<table width="100%">
<tr>
<th width="25%">Sub-section</th>
<th width="45%">Description</th>
<th width="15%">Cardinally</th>
<th width="15%">Conformance</th>
</tr>
<tr>
<td>Discharging consultant</td>
<td>The consultant responsible for the patient at time of discharge.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Discharging specialty/department</td>
<td>The specialty/department responsible for the patient at the time of discharge.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Discharge location</td>
<td>The ward or unit the patient was in immediately prior to discharge.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Date/time of discharge</td>
<td>The actual date of discharge</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Discharge method</td>
<td>The method of discharge from hospital. National codes:
eg, patient discharged on clinical advice or with clinical consent; patient discharged
him/herself or was discharged by a relative or advocate, patient died, stillbirth.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Discharge destination</td>
<td>Discharge destination comprising:</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<table>
<tr>
<td>Discharge type</td> 
<td>The destination of the patient on discharge from hospital. National codes e.g.. NHS-run care home.
</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Discharge address</td> 
<td>Address to which patient discharged. Only completed where this is not the usual
place of residence.Eg NHS-run care home.</td>
<td>1..1</td>
<td>Mandatory</td>
</td>
</tr>
</table>

</table>

##  Example Discharge Section ##

<script src="https://gist.github.com/IOPS-DEV/8af6e4182fad6c0ce91e46e6d17563b5.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- [Encounter](workflow_encounter.html)






