---
title: Diagnoses Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_diagnoses.html
summary: "Gives information about the Diagnoses section"
---

{% include custom/section.warnbanner.html %}

## Diagnoses Section Content##
The Diagnoses section carries information about Diagnoses, elements should be formatted as sub headings in any html sent.

<table>
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
			<td>Diagnoses</td>
			<td>A list of the patient's diagnoses.</td>
			<td>1 only</td>
			<td>mandatory</td>
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
			<td>Diagnosis name</td>
			<td>Confirmed diagnosis (or symptom); active diagnosis being treated.</td>
			<td>1 only</td>
			<td>mandatory</td>
			<td>Choice of free text or text derived from SNOMED CT concepts</td>
		<tr>
			<td>Stage</td>
			<td>Stage of the disease, where relevant</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>Text.</td>
		</tr>
		<tr>
			<td>Comment</td>
			<td>Supporting text may be given covering diagnosis confirmation, active diagnosis being treated.</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>Free text.</td>
		</tr>
		<tr>
			<td>Supporting text may be given covering diagnosis confirmation, active diagnosis being treated.</td>
		</tr>
	</tbody>
</table>



##  Example Diagnoses Section ##

This section example includes a reference to a coded diagnosis.

<script src="https://gist.github.com/IOPS-DEV/6903725738cefc330a8964316f0a5e9d.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- Condition
 
See constructing coded clinical structures - [Condition](build_conditions.html)






