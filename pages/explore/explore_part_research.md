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
This is to flag participation in a clinical trial, elements should be formatted as sub headings in any html sent.

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
			<td>Participation in research</td>
			<td>The details of any research studies participated in.</td>
			<td>&nbsp;</td>
			<td>optional</td>
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
			<td>Name of research study</td>
			<td>Name of the research study/trial and/or drug/intervention</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>Record(s) of participation in clinical trial(s). Each record should include information about the trial and the patient's participation, as recorded by the clinician. Text.</td>
		</tr>
	</tbody>
</table>

##  Example Participation in Research Section ##

<script src="https://gist.github.com/IOPS-DEV/9cd8f422a7c1e323ed42ac424a5830db.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK FHIR eDischarge does not currently support coded participation in research information.






