---
title: Admission Details Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_admission_details.html
summary: "Gives information about the Admission details section"
---

{% include custom/section.warnbanner.html %}

## Admission Details Section Content##
The Admission details section carries information about the patient's admission. Elements should be formatted as subheadings in any HTML sent.

<table style="width:100%;max-width: 100%;">
	<thead>
		<tr>
			<th width="15%">Section</th>
			<th width="30%">Description</th>
			<th width="5%">Card.</th>
			<th width="5%">MRO*</th>
			<th width="25%">M=Mandatory R=Required O=Optional</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Admission details</td>
			<td>Details of the patient's admission and reason for admission</td>
			<td>0..1</td>
			<td>R</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<th>Element</th>
			<th>Description</th>
			<th>Card.</th>
			<th>MRO*</th>
			<th>Guidance</th>		
		</tr>
		<tr>
			<td>Reason for admission</td>
			<td>The health problems and issues experienced by the patient that prompted the decision to admit to hospital e.g. chest pain, mental health crisis, blackout, fall,  a specific procedure, intervention, investigation or treatment, non compliance with treatment.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>Text and where supported a SNOMED CT concept carried in the CodeableConcept of the <b>Encounter.reason</b> element to indicate the reason the patient was admitted.</td>
		</tr>
		<tr>
			<td>Admission method</td>
			<td>How the patient was admitted to hospital. For example: elective, emergency, maternity, transfer etc.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>Text and where supported a code and description from the ValueSet <a href="https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-SourceOfAdmission-1">CareConnect-SourceOfAdmission-1</a> carried in the FHIR CodeableConcept of  the <b>Encounter.hospitalization.Extension-CareConnect-AdmissionMethod-1</b> element</td>
		</tr>
		<tr>
			<td>Source of admission</td>
			<td>Where the patient was immediately prior to admission, e.g. usual place of residence, temporary place of residence, penal establishment. National code.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>Text and where supported a code and description from the ValueSet <a href="https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-SourceOfAdmission-1">CareConnect-SourceOfAdmission-1</a> carried in the CodeableConcept of the <b>Encounter.hospitalization.admitSource</b> element</td>
		</tr>
		<tr>
			<td>Date/time of admission</td>
			<td>Date and time patient admitted to hospital.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>The date and time of admission as recorded on the Patient Administration System (PAS) as text and carried in the <b>Encounter.period.start element</b> </td>
		</tr>
	</tbody>
</table>


##  Example Admission Details Section ##

<script src="https://gist.github.com/IOPS-DEV/063615bfb87522015e0c37ef7f06d4fd.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- [Encounter](workflow_encounter.html)






