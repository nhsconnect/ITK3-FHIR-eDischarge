---
title: Clinical Summary Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_clinical_summary.html
summary: "Gives information about the Clinical summary section"
---

{% include custom/section.warnbanner.html %}

## Clinical Summary Section Content##
The Clinical summary section carries a narrative summary of the episode, where possible very brief. Elements should be formatted as subheadings in any HTML sent.

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
			<td>Clinical summary</td>
			<td>A brief description of the encounter.</td>
			<td>1 only</td>
			<td>M</td>
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
			<td>Clinical summary</td>
			<td>Summary of the encounter. Where possible, very brief. This may include interpretation of findings and results; differential diagnoses, opinion and specific action(s). Planned actions will be recorded under 'plan'.</td>
			<td>1 only</td>
			<td>M</td>
			<td>Free text</td>
		</tr>
		<tr>
		<td colspan="5"><b>* M=Mandatory R=Required O=Optional</b></td>
		</tr>
	</tbody>
</table>

##  Example Clinical Summary Section ##

<script src="https://gist.github.com/IOPS-DEV/721d38297900a223f98cbd1b1c1f4e5b.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK3 FHIR eDischarge does not currently support a coded clinical summary.






