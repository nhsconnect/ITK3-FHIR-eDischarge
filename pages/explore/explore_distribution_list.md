---
title: Distribution List Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_distribution_list.html
summary: "A list of recipients of the document"
---
{% include custom/section.warnbanner.html %}


## Distribution List Section Content ##


The Distribution list section carries a list of recipients of the document. Elements should be formatted as subheadings in any html sent.

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
			<td>Distribution list</td>
			<td>A list of other individuals to receive a copy of this communication.</td>
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
			<td>Name</td>
			<td>If the comunication is being sent to a named individual, then this is the name of the recipient, preferably in a structured format. An identifier for the individual, for example GMC code (for a GP), or an SDS identifier, a NHS Number (for a patient) will be sent alongside the name, but may not displayed on rendered document.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>Names may be entered as the communication is being created, or sourced from the hospital system.Patient names may be from the Patient Demographic Service.</td>
		</tr>
		<tr>
			<td>Role</td>
			<td>If the communication is being sent to either a named individual, or to a non-named person with a specific role, then this is the role of the recipient.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>Role may be entered as the communication is being created, or sourced from the hospital system. This may be a role defined in the National Workforce data set (see the NHS Data Dictionary Job Role Code).</td>
		</tr>
		<tr>
			<td>Grade</td>
			<td>The recipient's grade.</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>The grade of the recipient, if known by the sending institution, otherwise omitted.</td>
		</tr>
		<tr>
			<td>Organisation name</td>
			<td>The name of the organisation the recipient is representing or the organisation named as the receiving organisation.An identifier for the organisation will be sent alongside the name, but may not be displayed on rendered document.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>Organisation name, and identifier, taken from the Organisation Data Service (ODS).</td>
		</tr>
		<tr>
			<td>Team</td>
			<td>Team that the recipient belongs to in the context of receiving this message, or the team acting as the recipient.</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>There are no national codes for teams, so this value would have to be agreed locally, and entered as free text.</td>
		</tr>
		<tr>
			<td>Relationship to subject</td>
			<td>The relationship of the receiver to the patient, where the receiver has a personal relationship to the patient, for example, carer or parent</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>Personal relationships as documented in the NHS Data Dictionary Person Relationship Type.</td>
		</tr>
	</tbody>
</table>

## Example Distribution List Entry Using Organization Resource ##

This example shows a recipient organization entry.

<script src="https://gist.github.com/IOPS-DEV/f5c1fab997a9d0ef2a586e73728ac2a7.js"></script>


## Example Distribution List Entry Using Practitioner Resource ##

This example shows a recipient practitioner entry.

<script src="https://gist.github.com/IOPS-DEV/dd3378a4b7b62deaa48117449efbd7b8.js"></script>


## Example Distribution List Entry Using Patient Resource ##

This example shows a recipient patient entry.

<script src="https://gist.github.com/IOPS-DEV/af79cf398178936f11f5eb5c5d45c13c.js"></script>

## Example Distribution List Entry Using RelatedPerson Resource ##

This example shows a recipient related person (such as a carer) entry.

<script src="https://gist.github.com/IOPS-DEV/0b8035163391ff6a5de011412c079338.js"></script>

## Example Rendered Distribution List ##

This example shows a Distribution list section when rendered using the NHS Digital exemplar renderer.


**Distribution list**
		
<table width="100%">
<tr>
<th>Recipient name</th>
<th>Job role</th>
<th>Phone</th>
<tr>
<tr>
<td>Morris, Angela (Mrs)</td>
<td>Physiotherapist</td>
<td>01136323200</td>
<tr>
<tr>
<th>Recipient name</th>
<th>Relationship</th>
<th>Phone</th>
<tr>
<tr>
<td>Smith, Sarah</td>
<td>Wife</td>
<td>071234567811</td>
<tr>		
<tr>
<th>Recipient name</th>
<th>Type</th>
<th>Phone</th>
<tr>
<tr>
<td>Whitehouse Practice</td>
<td>GP Practice</td>
<td>071234567811</td>
<tr>
			


		
