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
The Patient and carer concerns, expectations and wishes section carries information about the concerns of the patient or their representative. Elements should be formatted as subheadings in any HTML sent.

<table style="width:100%;max-width: 100%;">
	<thead>
		<tr>
			<th width="15%">Section</th>
			<th width="35%">Description</th>
			<th width="5%">Card.</th>
			<th width="5%">MRO*</th>
			<th width="40%">FHIR Target and Guidance</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Patient and carer concerns, expectations and wishes</td>
			<td>A description of the concerns, expectations or wishes of the patient.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>Carried in the CodeableConcept of <b>Composition.section.code</b> FHIR element.</td>
		</tr>
		<tr>
			<th>PRSB Element</th>
			<th>Description</th>
			<th>Card.</th>
			<th>MRO*</th>
			<th>FHIR Target and Guidance</th>		
		</tr>
		<tr>
			<td>Patient and carer concerns, expectations and wishes</td>
			<td>Description of the concerns, wishes or goals of the person in relation to their care, as expressed by the person, their representative or carer. Record who has expressed these (patient or carer/ representative on behalf of the patient).Where the person lacks capacity this may include their representative's concerns, expectations or wishes.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>A record of statements expressed by the person or their carer or representative. Text only.</td>
		</tr>
		<tr>
			<td>Advance statement</td>
			<td>Written requests and preferences made by a person with capacity conveying their wishes, beliefs and values for their future care should they lose capacity. Include the location of the document if known.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>A record of the presence of an advance statement in text. The content of the advance statement should also be included as text or attached as a document where available see section on <a href="build_attachments.html">FHIR attachments</a>.</td>
		</tr>
		<tr>
		<td colspan="5"><b>* M=Mandatory R=Required O=Optional</b></td>
		</tr>
	</tbody>
</table>


## Example Patient and Carer Concerns, Expectations and Wishes Section ##

<script src="https://gist.github.com/IOPS-DEV/cd418195a1684f2148936dec94a40842.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK3 FHIR eDischarge does not currently support coded patient and carer concerns, expectations and wishes information.






