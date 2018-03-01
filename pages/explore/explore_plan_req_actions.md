---
title: Plan and requested actions Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_plan_req_actions.html
summary: "Gives information about the Plan and requested actions section"
---

{% include custom/section.warnbanner.html %}

## Plan and Requested Actions Section Content ##
The Plan and requested actions section carries information about planned and requested actions such as planned investigations, procedures etc, elements should be formatted as sub headings in any html sent.

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
			<td>Plan and requested actions</td>
			<td>The details of planned investigations, procedures and treatment, and whether this plan has been agreed with the patient or their legitimate representative.</td>
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
			<td>Actions for healthcare professionals</td>
			<td>Including planned investigations, procedures and treatment for a patient's identified conditions and priorities. For each action the following should be identified:outcome expectations, including patient's expectations</td>
			<td>0 to many</td>
			<td>required</td>
			<td>A record of the planned and requested actions. May be structured (table), with actions, names, dates, status, location, strategies, or free text</td>
		</tr>
		<tr>
			<td>Actions for patient or their carer</td>
			<td>For each action the following should be identified:outcome expectations, including patient's expectations.</td>
			<td>0 to many</td>
			<td>required</td>
			<td>A record of the planned and requested actions. May be structured (table), with actions, names, dates, status, location, strategies, or free text.</td>
		</tr>
		<tr>
			<td>Agreed with patient or legitimate patient representative</td>
			<td>Indicates whether the patient or legitimate representative has agreed the entire plan or individual aspects of treatment, expected outcomes, risks and alternative treatments.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>A record of the agreement of the decisions made. Text</td>
		</tr>
		<tr>
			<td>Investigations requested</td>
			<td>This includes a name or description of the investigation requested and the date requested.</td>
			<td>0 to many</td>
			<td>optional</td>
			<td>Text. Plus date requested.</td>
		</tr>
		<tr>
			<td>Procedures requested</td>
			<td>These are the diagnostic or therapeutic procedures that have actually been requested (and the date requested).</td>
			<td>0 to many</td>
			<td>optional</td>
			<td>Text. Plus date requested</td>
		</tr>
	</tbody>
</table>

##  Example Plan and Requested Actions Section ##

<script src="https://gist.github.com/IOPS-DEV/1bdcde4481d7de7dfdf7bcc266529e10.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK FHIR eDischarge does not currently support coded Plan and requested actions information.






