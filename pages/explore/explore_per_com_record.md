---
title: Person Completing Record Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_per_com_record.html
summary: "Gives information about the Person completing record section"
---

{% include custom/section.warnbanner.html %}

## Person Completing Record Section Content##
The Person completing record section carries information about the person who completed the record.Elements should be formatted as sub headings in any html sent.


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
			<td>Person completing record</td>
			<td>The details of the person who filled out the record.</td>
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
			<td>Name</td>
			<td>The name of the person completing the record, preferably in a structured format.</td>
			<td>1 only</td>
			<td>mandatory</td>
			<td>The person name as held on the source system. Where possible this should be broken down into its constituent parts (prefix, given name, family name, and suffix). An identifier for the person completing the record will be sent (but may not be displayed in the rendered message).</td>
		</tr>
		<tr>
			<td>Role</td>
			<td>The role the person is playing within the organisation at the time record was updated.</td>
			<td>1 only</td>
			<td>mandatory</td>
			<td>The role may be held on the source system, be from an authoritative source such as SDS, or use an existing vocabulary such as the job role title (from the national workforce dataset).</td>
		</tr>
		<tr>
			<td>Grade</td>
			<td>The grade of the person completing the record</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>The grade of the person completing the record held on the source system or from an authoritative source</td>
		</tr>
		<tr>
			<td>Specialty</td>
			<td>The main specialty of the person completing the record</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>The main clinical specialty as held on the source system.</td>
		</tr>
		<tr>
			<td>Professional identifier</td>
			<td>Professional identifier for the person completing the record e.g., GMC number, HCPC number etc or the personal identifier used by the local organisation.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>The professional identifier type and the identifier itself of the person completing the record held on the source system.</td>
		</tr>
		<tr>
			<td>Date and time completed</td>
			<td>The date and time the record was updated.</td>
			<td>1 only</td>
			<td>mandatory</td>
			<td>The date/time the record was updated. This will probably be a system, date taken from electronic device used to update the patient record.</td>
		</tr>
		<tr>
			<td>Contact details</td>
			<td>Contact details of the person completing the record. For example a phone number, email address. Contact details are used to resolve queries about the record entry.</td>
			<td>0 to many</td>
			<td>optional</td>
			<td>The contact details may be for the individual completing the record, or wider team details (for example a phone number for a hospital department).</td>
		</tr>
		<tr>
			<td>Organisation</td>
			<td>The organisation the person completing the record works for.</td>
			<td>1 only</td>
			<td>mandatory</td>
			<td>An ODS identifier for the organisation or site, the name of the organisation or site, and a postal address (if available).</td>
		</tr>
	</tbody>
</table>

## Example Person Completing Record Section ##

<script src="https://gist.github.com/IOPS-DEV/4eceababbca389067cde4aefd2d61cde.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK FHIR eDischarge does not currently support coded Person completing record information.






