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
			<th width="18%">Section</th>
			<th width="30%">Description</th>
			<th width="11%">Cardinality</th>
			<th width="11%">MRO*</th>
			<th width="30%">Values</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Clinical summary</td>
			<td>A brief description of the encounter.</td>
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
			<td>Clinical summary</td>
			<td>Summary of the encounter. Where possible, very brief. This may include interpretation of findings and results; differential diagnoses, opinion and specific action(s). Planned actions will be recorded under 'plan'.</td>
			<td>1 only</td>
			<td>mandatory</td>
			<td>Free text</td>
		</tr>
	</tbody>
</table>

##  Example Clinical Summary Section ##

<script src="https://gist.github.com/IOPS-DEV/77620f7d132b195c42b5f2fee5f39172.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK3 FHIR eDischarge does not currently support a coded clinical summary.






