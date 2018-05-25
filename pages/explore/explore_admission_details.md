---
title: Admission Details Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_admission_details.html
summary: "Gives information about the Admission details section"
---

{% include custom/section.warnbanner.html %}

## Admission Details Section Content##
The Admission details section carries information about the patient's admission. Elements should be formatted as sub headings in any HTML sent.

<table style="width:100%;max-width: 100%;">
	<thead>
		<tr>
			<th width="18%">Section</th>
			<th width="30%">Description</th>
			<th width="11%">Cardinality</th>
			<th width="11%">MRO*</th>
			<th width="30%">Values</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Admission details</td>
			<td>Details of the patient's admission and reason for admission</td>
			<td>0..1</td>
			<td>required</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<th>Element</th>
			<th>Description</th>
			<th>Cardinality</th>
			<th>MRO*</th>
			<th>Values</th>
		</tr>
		<tr>
			<td>Reason for admission</td>
			<td>The health problems and issues experienced by the patient that prompted the decision to admit to hospital e.g. chest pain, mental health crisis, blackout, fall,  a specific procedure, intervention, investigation or treatment, non compliance with treatment.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>May be a SNOMED CT concept and/or free text.</td>
		</tr>
		<tr>
			<td>Admission method</td>
			<td>How the patient was admitted to hospital. For example: elective, emergency, maternity, transfer etc.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>One of the codes and description from the NHS Data Dictionary Admission Method</td>
		</tr>
		<tr>
			<td>Source of admission</td>
			<td>Where the patient was immediately prior to admission, e.g. usual place of residence, temporary place of residence, penal establishment. National code.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>One of the codes and description from the NHS Data Dictionary Source of Admission</td>
		</tr>
		<tr>
			<td>Date/time of admission</td>
			<td>Date and time patient admitted to hospital.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>The date and time of admission as recorded on the Patient Administration System (PAS)</td>
		</tr>
	</tbody>
</table>


##  Example Admission Details Section ##

<script src="https://gist.github.com/IOPS-DEV/063615bfb87522015e0c37ef7f06d4fd.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- [Encounter](workflow_encounter.html)






