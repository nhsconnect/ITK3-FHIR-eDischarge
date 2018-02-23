---
title: Distribution List Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_distribution_list.html
summary: "A list of recipients of the document"
---
{% include custom/non_text_section.warnbanner.html %}


## Distribution List Section Content ##


The Distribution list section carries a list of recipients of the document subheadings should be formatted as such in any html sent:

<table width="100%">
<tr>
<th width="25%">Sub-section</th>
<th width="45%">Description</th>
<th width="15%">Cardinally</th>
<th width="15%">Conformance</th>
</tr>
<tr>
<td>Name</td>
<td>If the document is being sent to a named individual, then this is the name of the recipient, preferably in a structured format. An identifier for the individual, for example GMC code (for a GP), or an SDS identifier, a NHS Number (for a patient) will be sent alongside the name, but may not displayed on rendered document.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Role</td>
<td>If the document is being sent to either a named individual, or to a non-named person with a specific role, then this is the role of the recipient</td>
<td>0..1</td>
<td>Required</td>
</tr>
<tr>
<td>Grade</td>
<td>The recipient’s grade.</td>
<td>0..1</td>
<td>Required</td>
</tr>
<tr>
<td>Organisation name</td>
<td>The name of the organisation the recipient is representing or the organisation named as the receiving organisation. An identifier for the organisation will be sent alongside the name, but may not be displayed on rendered document.</td>
<td>0..1</td>
<td>Required</td>
</tr>
<tr>
<td>Team</td>
<td>Team that the recipient belongs to in the context of receiving this message, or the team acting as the recipient.</td>
<td>0..1</td>
<td>Required</td>
</tr>
<tr>
<td>Relationship to subject</td>
<td>Relationship to subject	The relationship of the receiver to the patient, where the receiver has a personal relationship to the patient, for example, carer or parent</td>
<td>0..1</td>
<td>Required</td>
</tr>
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
			


		
