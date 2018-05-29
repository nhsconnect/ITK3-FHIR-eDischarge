---
title:  Individual Requirements Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_individual_reqs.html
summary: "Gives information about the Individual requirements section"
---

{% include custom/section.warnbanner.html %}

## Individual Requirements Section Content ##
The Individual requirements section carries information about the individual requirements of the patient. Elements should be formatted as subheadings in any HTML sent.

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
			<td>Individual requirements </td>
			<td>Individual requirements that a person has, e.g. communication, cultural, cognitive or mobility needs. </td>
			<td>0 to 1</td>
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
			<td>Individual requirements</td>
			<td>Individual requirements that a person has. These may be communication, cultural, cognitive or mobility needs.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>Information volunteered by the person or their representative or known about locally. Text or coded text (SNOMED CT), constrained as specified in SCCI1605 Accessible Information standard (accessible information - communications support, accessible information - requires communications professional, accessible information - requires specific contact method, accessible information - requires specific information format).</td>
		</tr>
	</tbody>
</table>


##  Example Individual Requirements Section ##

<script src="https://gist.github.com/IOPS-DEV/497e71d591b9041c318dc4c88517287b.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK3 FHIR eDischarge does not currently support coded individual requirements information.






