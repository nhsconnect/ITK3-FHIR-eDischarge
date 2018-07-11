---
title: Procedures Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_procedures.html
summary: "Gives information about the Procedures section"
---

{% include custom/section.warnbanner.html %}

## Procedures Section Content##
The Procedures section carries information about the procedures that have been performed on the patient. PRSB Elements should be formatted as subheadings in any HTML sent.

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
			<td>Procedures </td>
			<td>The details of any procedures performed.</td>
			<td>0 to 1</td>
			<td>O</td>
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
			<td> Procedure name</td>
			<td>The therapeutic or diagnostic procedure performed.</td>
			<td>1 only</td>
			<td>M</td>
			<td>The procedure name in text and where supported a SNOMED CT concept from 71388002 Procedure (procedure) hierarchy or Procedure with explicit context (situation)129125009. Carried in the FHIR element <b>Procedure.code</b> See <a href="build_procedures#procedurecode.html">Constructing Procedure Lists (Procedure name)</a></td>
		</tr>
		<tr>
			<td>Anatomical site</td>
			<td>The body site of the procedure</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text and where supported a SNOMED CT concept to represent the anatomical site carried in <b>Procedure.bodySite</b>.</td>
		</tr>
		<tr>
			<td>Laterality</td>
			<td>Laterality of the procedure</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text and where supported a SNOMED CT concept to represent the laterality carried in <b>Procedure.bodySite</b> (if part of the pre-coordinated term).</td>
		</tr>
		<tr>
			<td>Complications related to procedure</td>
			<td>Details of any intra-operative complications encountered during the procedure, arising during the patient's stay in the recovery unit or directly attributable to the procedure.</td>
			<td>0 to many</td>
			<td>O</td>
			<td>Text and where supported a SNOMED CT concept to represent the complication carried in the FHIR element <b>Procedure.complication</b> and <b>Procedure.complicationDetail</b>.</td>
		</tr>
		<tr>
			<td>Specific anaesthesia issues</td>
			<td>Details of any adverse reaction to any anaesthetic agents including local anaesthesia.  Problematic intubation, transfusion reaction, etc.</td>
			<td>0 to many</td>
			<td>O</td>
			<td>Text and where supported either a SNOMED CT concept or a reference to the Condition Resource to represent the anaesthesia issues carried using the extension <b>Extension-CareConnect-AnaestheticIssues-1</b>.</td>
		</tr>
		<tr>
			<td>Comment</td>
			<td>Any further textual comment to clarify such as statement that information is partial or incomplete.</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Free text</td>
		</tr>
		<tr>
		<td colspan="5"><b>* M=Mandatory R=Required O=Optional</b></td>
		</tr>
	</tbody>
</table>


##  Example Procedures Sections ##

<script src="https://gist.github.com/IOPS-DEV/9aac8ea1c4e276ff1316608ea53b0c8e.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- Procedure
 
See constructing clinical coded structures - [Procedures](build_procedures.html)











