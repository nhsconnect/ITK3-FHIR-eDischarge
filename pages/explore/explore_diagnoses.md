---
title: Diagnoses Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_diagnoses.html
summary: "Gives information about the Diagnoses section"
---

{% include custom/section.warnbanner.html %}

## Diagnoses Section Content##
The Diagnoses section carries information about Diagnoses. Elements should be formatted as subheadings in any HTML sent.

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
			<td>Diagnoses</td>
			<td>A list of the patient's diagnoses.</td>
			<td>1 only</td>
			<td>M</td>
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
			<td>Diagnosis name</td>
			<td>Confirmed diagnosis (or symptom); active diagnosis being treated.</td>
			<td>1 only</td>
			<td>M</td>
			<td>Text and if available a SNOMED CT concept carried in the CodeableConcept of the <b>Condition.code</b> FHIR element. See <a href="build_conditions.html#diagnosis-code">Constructing Diagnosis Lists (Diagnosis code)</a> for further guidance.</td>
		</tr>
		<tr>
			<td>Stage</td>
			<td>Stage of the disease, where relevant</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text and if available a SNOMED CT concept carried in the CodeableConcept of the <b>Condition.stage.summary (using the CodeableContext text to hold the stage of disease text)</b></td>
		</tr>
		<tr>
			<td>Comment</td>
			<td>Supporting text may be given covering diagnosis confirmation, active diagnosis being treated.</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Free text.  Supporting text may be given covering diagnosis confirmation, active diagnosis being treated.  The section text should be repeated in the text of the <b>Condition.note </b>FHIR element to record Free differential and excluded diagnosis.</td>
		</tr>
		<tr>
		<td colspan="5"><b>* M=Mandatory R=Required O=Optional</b></td>
		</tr>
	</tbody>
</table>



##  Example Diagnoses Section ##

This section example includes a reference to a coded diagnosis.

<script src="https://gist.github.com/IOPS-DEV/6903725738cefc330a8964316f0a5e9d.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- Condition
 
See constructing clinical coded structures - [Condition](build_conditions.html)






