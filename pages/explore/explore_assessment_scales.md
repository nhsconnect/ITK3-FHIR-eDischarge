---
title: Assessment Scales Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_assessment_scales.html
summary: "Gives information about the Assessment scales section"
---

{% include custom/section.warnbanner.html %}

## Assessment Scales Section Content##
The Assessment scales section carries information about assessment scales used. Elements should be formatted as subheadings in any HTML sent.

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
			<td>Assessment scale</td>
			<td>A description of any assessment scales used.</td>
			<td>0 to 1</td>
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
			<td>Assessment scale</td>
			<td>Assessment scale used, eg New York Heart Failure, Activities of Daily Living (ADL)</td>
			<td>0 to many</td>
			<td>O</td>
			<td>Text. Content could include scale name, date and time of assessment and values recorded, including overall score. Format of assessment would be determined locally and may be tabular.</td>
		</tr>
		<tr>
		<td colspan="5"><b>* M=Mandatory R=Required O=Optional</b></td>
		</tr>
	</tbody>
</table>


## Example Assessment Scales Section Example ##

<script src="https://gist.github.com/IOPS-DEV/661246335c1771029116eda10ec1f54b.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK3 FHIR eDischarge does not currently support coded assessment scales.






