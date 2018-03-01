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
The Procedures section carries information about the procedures that have been performed on the patient, subheadings should be formatted as such in any html sent:

<table>
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
			<td>Procedures </td>
			<td>The details of any procedures performed.</td>
			<td>0 to 1</td>
			<td>optional</td>
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
			<td> Procedure name</td>
			<td>The therapeutic or diagnostic procedure performed.</td>
			<td>1 only</td>
			<td>mandatory</td>
			<td>Choice of free or text derived from SNOMED CT concepts.</td>
		</tr>
		<tr>
			<td>Anatomical site</td>
			<td>The body site of the procedure</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>Choice of free or text derived from SNOMED CT concepts.</td>
		</tr>
		<tr>
			<td>Laterality</td>
			<td>Laterality of the procedure</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>Choice of free or text derived from SNOMED CT concepts.</td>
		</tr>
		<tr>
			<td>Complications related to procedure</td>
			<td>Details of any intra-operative complications encountered during the procedure, arising during the patient's stay in the recovery unit or directly attributable to the procedure.</td>
			<td>0 to many</td>
			<td>optional</td>
			<td>Choice of free or text derived from SNOMED CT concepts.</td>
		</tr>
		<tr>
			<td>Specific anaesthesia issues</td>
			<td>Details of any adverse reaction to any anaesthetic agents including local anaesthesia.  Problematic intubation, transfusion reaction, etc.</td>
			<td>0 to many</td>
			<td>optional</td>
			<td>Choice of free or text derived from SNOMED CT concepts.</td>
		</tr>
		<tr>
			<td>Comment</td>
			<td>Any further textual comment to clarify such as statement that information is partial or incomplete.</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>Text</td>
		</tr>
	</tbody>
</table>


##  Example Procedures Sections ##

<script src="https://gist.github.com/IOPS-DEV/9aac8ea1c4e276ff1316608ea53b0c8e.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- Procedures
 
See constructing coded clinical structures - [Procedures](build_procedures.html)











