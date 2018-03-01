---
title: Patient and Carer Concerns, Expectations and Wishes Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_pat_care_concerns.html
summary: "Gives information about the Patient and carer concerns, expectations and wishes section"
---

{% include custom/section.warnbanner.html %}

## Patient and Carer Concerns, Expectations and Wishes Section Content##
The Patient and carer concerns, expectations and wishes section carries information about the concerns of the patient or their representative. Elements should be formatted as subheadings in any html sent.

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
			<td>Patient and carer concerns, expectations and wishes</td>
			<td>A description of the concerns, expectations or wishes of the patient.</td>
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
			<td>Patient and carer concerns, expectations and wishes</td>
			<td>Description of the concerns, wishes or goals of the person in relation to their care, as expressed by the person, their representative or carer. Record who has expressed these (patient or carer/ representative on behalf of the patient).Where the person lacks capacity this may include their representative's concerns, expectations or wishes.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>A record of statements expressed by the person or their carer or representative. Text</td>
		</tr>
		<tr>
			<td>Advance statement</td>
			<td>Written requests and preferences made by a person with capacity conveying their wishes, beliefs and values for their future care should they lose capacity. Include the location of the document if known.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>A record of the presence of an advance statement using the following SNOMED CT concept from the National Information Standard (SCCI1580):SNOMED CT: 816281000000101. Has advance statement (Mental Capacity Act 2005)The content of the advance statement should also be included as text or attached as a document where available.</td>
		</tr>
	</tbody>
</table>


## Example Patient and Carer Concerns, Expectations and Wishes Section ##

<script src="https://gist.github.com/IOPS-DEV/cd418195a1684f2148936dec94a40842.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK FHIR eDischarge does not currently support coded patient and carer concerns, expectations and wishes information.






