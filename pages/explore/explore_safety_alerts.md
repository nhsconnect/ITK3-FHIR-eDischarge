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
The Safety alerts section carries safety alerts associated with the patient. PRSB Elements should be formatted as subheadings in any HTML sent.

<table style="width:100%;max-width: 100%;">
	<thead>
		<tr>
			<th width="15%">Section</th>
			<th width="35%">Description</th>
			<th width="5%">Card.</th>
			<th width="5%">MRO*</th>
			<th width="40%">FHIR Target and Guidance</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Safety alerts</td>
			<td>The details of any risks the patient poses to themselves or others.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>Carried in the CodeableConcept of <b>Composition.section.code</b> FHIR element.</td>
		</tr>
		<tr>
			<th>PRSB Element</th>
			<th>Description</th>
			<th>Card.</th>
			<th>MRO*</th>
			<th>FHIR Target and Guidance</th>		
		</tr>
		<tr>
			<td>Risks to self</td>
			<td>Risks the patient poses to themselves, e.g., suicide, overdose, self-harm, self-neglect.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>A statement of any risks identified by the clinician or healthcare professional. Text only.</td>
		</tr>
		<tr>
			<td>Risks to others</td>
			<td>Risks caring professionals or others.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>A statement of any risks identified by the clinician or healthcare professional. Text only.</td>
		</tr>
		<tr>
			<td>Risk from others </td>
			<td>Details of where an adult or child is at risk from an identified person e.g. family member etc.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>A statement of any risks identified by the clinician or healthcare professional. Text only.</td>
		</tr>
		<tr>
		<td colspan="5"><b>* M=Mandatory R=Required O=Optional</b></td>
		</tr>
	</tbody>
</table>

##  Example Safety Alerts Section ##

<script src="https://gist.github.com/IOPS-DEV/598b9ff335715b03d0264a03f2442d34.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK3 FHIR eDischarge does not currently support a coded safety alerts.


