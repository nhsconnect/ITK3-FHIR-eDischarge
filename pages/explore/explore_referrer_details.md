---
title: Referrer Details Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_referrer_details.html
summary: "Gives information about the Referrer details section"
---

{% include custom/section.warnbanner.html %}

## Referrer Details Section Content##
The Referrer details section carries a narrative summary of the episode. Where possible, very brief. Elements should be formatted as sub headings in any html sent.

<table style="width:100%;max-width: 100%;">
	<thead>
		<tr>
			<th width="15%">Section</th>
			<th width="30%">Description</th>
			<th width="14%">Cardinality</th>
			<th width="11%">MRO*</th>
			<th width="30%">Values</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Referrer details</td>
			<td>Details of the individual or team who referred the patient.</td>
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
			<td>Referrer details</td>
			<td>Name, role, grade, organisation and contact details of referrer. If not an individual, this could be e.g. GP surgery, department, specialty, sub-specialty, educational institution, mental health team etc. Also needs to include self-referral.</td>
			<td>0 to 1 referrer name<br/>0 to 1 referrer role<br/>0 to 1 referrer grade<br/>0 to 1 referrer department or team name<br/>0 to 1 referrer speciality<br/>0 to 1 referrer organisation<br/>0 to many contact details</td>
			<td>required</td>
			<td>The referrer details will normally be copied forward from the referral or handover of care, document.Where the referral or handover of care document stated individual, team, department or organisation names and identifies, these should form part of the Referrer details.Where the referral is a self-referral, coded text - self referral.</td>
		</tr>
	</tbody>
</table>


##  Example Referrer Details Section ##

<script src="https://gist.github.com/IOPS-DEV/324006a867ea11a33997dcb6148b289a.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK FHIR eDischarge does not currently support coded referrer details.






