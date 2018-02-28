---
title: Safety alerts Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_safety_alerts.html
summary: "Gives information about the Safety alerts section"
---

{% include custom/section.warnbanner.html %}

## Safety Alerts Section Content##
The Safety alerts section carries safety alerts associated with the patient, subheadings should be formatted as such in any html sent:

<table width="100%">
<tr>
<th width="25%">Sub-section</th>
<th width="45%">Description</th>
<th width="15%">Cardinally</th>
<th width="15%">Conformance</th>
</tr>
<tr>
<td>Risks to self</td>
<td>Risks the patient poses to themself, eg, suicide, overdose, self-harm, self-neglect.</td>
<td>0..1</td>
<td>Required</td>
</tr>
<tr>
<td>Risks to others</td>
<td>Risks to care professional or third party.</td>
<td>0..1</td>
<td>Required</td>
</tr>
</table>

##  Example Safety Alerts Section ##

<script src="https://gist.github.com/IOPS-DEV/598b9ff335715b03d0264a03f2442d34.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK FHIR eDischarge does not currently support a coded safety alerts.


