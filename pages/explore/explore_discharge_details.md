---
title: Discharge Details Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_discharge_details.html
summary: "Gives information about the Discharge details section"
---

{% include custom/section.warnbanner.html %}

## Discharge Details Section content ##
The Discharge details section carries details of the patient's discharge. PRSB Elements should be formatted as subheadings in any HTML sent.

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
			<td>Discharge details</td>
			<td>The details of the patient's discharge from hospital.</td>
			<td></td>
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
			<td>Discharging consultant</td>
			<td>The consultant responsible for the patient at time of discharge</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>The name and identifier of the consultant from a recognised source such as the Spine Directory Service, or a local identifier. Any identifiers <b>MUST NOT</b> be carried as text. The following FHIR Elements <b>SHOULD</b> be populated in the Practitioner and PractitionerRole Resources: 
			<ul>
			<li><b>Encounter.participant.type.code</b> should contain the value "DIS"</li>
			<li><b>Encounter.participant.type.display</b> should contain the value "discharger"</li>
			<li><b>Encounter.participant.individual.<br/>Reference.Practitioner.identifier</b></li>
			<li><b>Encounter.participant.individual.<br/>Reference.Practitioner.name</b></li>
			<li><b>PractitionerRole.code</b></li>
			<li><b>PractitionerRole.identifier</b></li></ul></td>
		</tr>		


<tr>
			<td>Discharging specialty/department</td>
			<td>The specialty or department responsible for the patient at the time of discharge</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>Text for either the main specialty of the discharging clinician (as held on the Spine Directory Service), or the department from which the patient is discharged. The specialty <b>SHOULD</b> be populated in the <b>PractitionerRole.specialty</b> FHIR element. The profile is currently bound to the FHIR ValueSet <a href="http://hl7.org/fhir/stu3/valueset-c80-practice-codes.html">c80-practice-codes</a> as preferred. This is proposed to be replaced by NHS Data main specialty code and therefore the current guidance is to not use the preferred ValueSet but to replace it using a code from <a href="https://www.datadictionary.nhs.uk/attributes/main_specialty_code.html">Main Specialty Code</a>. The FHIR CodeSystem element should be populated with "https://www.datadictionary.nhs.uk". As an alternative this element may be populated with a SNOMED CT concept and the FHIR CodeSystem element populated with "http://snomed.info/sct".

Note further guidance will be issues in a later release of the specification.</td>
		</tr>	


<tr>
			<td>Discharge location</td>
			<td>The ward or unit the patient was in immediately prior to discharge</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>Text to carry the ward name and identifier (if available) prior to discharge as recorded on the hospital discharging system. This information <b>SHOULD</b> also be carried in the FHIR element <b>Encounter.location.Reference.Location.name</b> and <b>Encounter.location.Reference.Location.identifier</b> </td>
		</tr>
		<tr>
			<td>Date/time of discharge</td>
			<td>The actual date of discharge</td>
			<td>1 only</td>
			<td>M</td>
			<td>Text indicating date and time of discharge as recorded by the PAS or discharging system. This <b>SHOULD</b> also be carried in the FHIR element <b>Encounter.period.end</b>.</td>
		</tr>
		<tr>
			<td>Discharge method</td>
			<td>The method of discharge from hospital. National codes: e.g. patient discharged on clinical advice or with clinical consent; patient discharged him/herself or was discharged by a relative or advocate; patient died; stillbirth</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>Text - Currently not to be coded for Transfer of Care Documents</td>
		</tr>
		<tr>
			<td>Discharge destination cluster</td>
			<td>The destination of the patient on discharge. National codes. E.g., High Dependency Unit.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td></td>
		</tr>
		<tr>
			<td>Discharge type</td>
			<td>The destination of the patient on discharge from hospital. National codes e.g.. NHS-run care home.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>Text and a code from the NHS Data Dictionary Discharge Destination carried in the CodeableConcept of the FHIR element <b>Encounter.hospitalization.dischargeDisposition</b></td>
		</tr>
		<tr>
			<td>Discharge address</td>
			<td>Address to which patient discharged. Only complete where this is not the usual place of residence.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>If the patient is discharged to their normal place of residence, no address is recorded on the discharge summary. Otherwise, an address other than the patient's usual place of residence may be provided by the patient or their representative. Text and an address carried in the FHIR element <b>Encounter.location.Reference.Location.address</b></td>
		</tr>
	
		<tr>
		<td colspan="5"><b>* M=Mandatory R=Required O=Optional</b></td>
		</tr>
	</tbody>
</table>


##  Example Discharge Section ##

<script src="https://gist.github.com/IOPS-DEV/1bfa7a1c00147c6bc5b1fc98aaa51029.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- [Encounter](workflow_encounter.html)






