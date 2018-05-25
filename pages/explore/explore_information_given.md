---
title: Information and Advice Given Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_information_given.html
summary: "Gives information about the Information and advice given section"
---

{% include custom/section.warnbanner.html %}

## Information and Advice Given Section Content##
The Information and advice given section carries information and advice given. Elements should be formatted as subheadings in any HTML sent.

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
			<td>Information and advice given</td>
			<td>A record of any information or advice given to the patient, carer or relevant third party.</td>
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
			<td>Information and advice given</td>
			<td>This includes:-what information-to whom it was given.</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>Free text description of information and advice given and patient/carer comprehension</td>
		</tr>
	</tbody>
</table>


##  Example Information and Advice Given Section ##


<script src="https://gist.github.com/IOPS-DEV/e71ebe4dbcaf89da92e719307cc56aeb.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK3 FHIR eDischarge does not currently support coded information and advice given.

 








