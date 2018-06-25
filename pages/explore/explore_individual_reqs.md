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
			<th width="15%">Section</th>
			<th width="35%">Description</th>
			<th width="5%">Card.</th>
			<th width="5%">MRO*</th>
			<th width="40%">FHIR Target and Guidance</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Individual requirements </td>
			<td>Individual requirements that a person has, e.g. communication, cultural, cognitive or mobility needs. </td>
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
			<td>Individual requirements</td>
			<td>Individual requirements that a person has. These may be communication, cultural, cognitive or mobility needs.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>Information volunteered by the person or their representative or known about locally. Text only constrained as specified in SCCI1605 Accessible Information standard (accessible information - communications support, accessible information - requires communications professional, accessible information - requires specific contact method, accessible information - requires specific information format).</td>
		</tr>
		<tr>
		<td colspan="5"><b>* M=Mandatory R=Required O=Optional</b></td>
		</tr>
	</tbody>
</table>


##  Example Individual Requirements Section ##

<script src="https://gist.github.com/IOPS-DEV/497e71d591b9041c318dc4c88517287b.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK3 FHIR eDischarge does not currently support coded individual requirements information.






