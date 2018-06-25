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
The Discharge details section carries details of the patient's discharge. Elements should be formatted as subheadings in any HTML sent.

<table style="width:100%;max-width: 100%;">
	<thead>
		<tr>
			<th width="15%">Section</th>
			<th width="35%">Description</th>
			<th width="5%">Card.</th>
			<th width="5%">MRO*</th>
			<th width="40%">FHIR Target and Guidance</th>
		</tr>
	<tbody>
		<tr>
			<td>Discharge details</td>
			<td>The details of the patient's discharge from hospital.</td>
			<td></td>
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
			<td>Discharging consultant</td>
			<td>The consultant responsible for the patient at time of discharge</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>The name and identifier of the consultant from a recognised source such as the Spine Directory Service, or a local identifier. Any identifiers <b>MUST NOT</b> be carried as text. The following FHIR Elements <b>SHOULD</b> be populated in the Practitioner and PractitionerRole Resouces: 
			<ul>
			<li><b>Encounter.participant.individual.<br/>Reference.Practitioner.identifier</b></li>
			<li><b>Encounter.participant.individual.<br/>Reference.Practitioner.name</b></li>
			<li><b>PractitionerRole.code</b></li>
			<li><b>PractitionerRole.identifier</b></li></ul></td>
		</tr>

	
		<tr>
		<td colspan="5"><b>* M=Mandatory R=Required O=Optional</b></td>
		</tr>
	</tbody>
</table>


##  Example Discharge Section ##

<script src="https://gist.github.com/IOPS-DEV/1bfa7a1c00147c6bc5b1fc98aaa51029.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- [Encounter](workflow_encounter.html)






