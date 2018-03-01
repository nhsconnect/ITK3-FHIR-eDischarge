---
title: Discharge Details Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_discharge_details.html
summary: "Gives information about the Discharge details section"
---

{% include custom/section.warnbanner.html %}

## Discharge Details Section Content##
The Discharge details section carries details of the patient's discharge. Elements should be formatted as sub headings in any html sent.

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
			<td>Discharge details</td>
			<td>The details of the patient's discharge from hospital.</td>
			<td>&nbsp;</td>
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
			<td>Discharging consultant</td>
			<td>The consultant responsible for the patient at time of discharge</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>The name and identifier of the consultant from a recognised source such as the Spine Directory Service, or a local identifier. The identifier would not be displayed in the message.</td>
		</tr>
		<tr>
			<td>Discharging specialty/department</td>
			<td>The specialty or department responsible for the patient at the time of discharge</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>Either the main specialty of the discharging clinician (as held on the Spine Directory Service), or the department from which the patient is discharged.</td>
		</tr>
		<tr>
			<td>Discharge location</td>
			<td>The ward or unit the patient was in immediately prior to discharge</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>The ward name and identifier (if available) prior to discharge as recorded on the hospital discharging system.</td>
		</tr>
		<tr>
			<td>Date/time of discharge</td>
			<td>The actual date of discharge</td>
			<td>1 only</td>
			<td>mandatory</td>
			<td>The date and time of discharge as recorded by the PAS or discharging system.</td>
		</tr>
		<tr>
			<td>Discharge method</td>
			<td>The method of discharge from hospital. National codes: e.g.. patient discharged on clinical advice or with clinical consent; patient discharged him/herself or was discharged by a relative or advocate; patient died; stillbirth</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>A code from the NHS Data Dictionary Discharge Method code</td>
		</tr>
		<tr>
			<th>Discharge destination cluster</th>
			<th>The destination of the patient on discharge. National codes. Eg, High Dependency Unit.</th>
			<th>0 to 1</th>
			<th>required</th>
			<th>&nbsp;</th>
		</tr>
		<tr>
			<td>Discharge type</td>
			<td>The destination of the patient on discharge from hospital. National codes e.g.. NHS-run care home.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>A code from the NHS Data Dictionary Discharge Destination</td>
		</tr>
		<tr>
			<td>Discharge address</td>
			<td>Address to which patient discharged. Only complete where this is not the usual place of residence.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>If the patient is discharged to their normal place of residence, no address is recorded on the discharge summary. Otherwise, an address other than the patient's usual place of residence may be provided by the patient or their representative.</td>
		</tr>
	</tbody>
</table>


##  Example Discharge Section ##

<script src="https://gist.github.com/IOPS-DEV/8af6e4182fad6c0ce91e46e6d17563b5.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- [Encounter](workflow_encounter.html)






