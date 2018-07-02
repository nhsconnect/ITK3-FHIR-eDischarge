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
This is to flag participation in a clinical trial. PRSB Elements should be formatted as subheadings in any HTML sent.

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
			<td>Participation in research</td>
			<td>The details of any research studies participated in.</td>
			<td>&nbsp;</td>
			<td>O</td>
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
			<td>Name of research study</td>
			<td>Name of the research study/trial and/or drug/intervention</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Record(s) of participation in clinical trial(s). Each record should include information about the trial and the patient's participation, as recorded by the clinician. Text only.</td>
		</tr>
		<tr>
		<td colspan="5"><b>* M=Mandatory R=Required O=Optional</b></td>
		</tr>
	</tbody>
</table>

##  Example Participation in Research Section ##

<script src="https://gist.github.com/IOPS-DEV/9cd8f422a7c1e323ed42ac424a5830db.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK3 FHIR eDischarge does not currently support coded participation in research information.






