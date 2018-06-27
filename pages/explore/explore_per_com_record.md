---
title: Person Completing Record Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_per_com_record.html
summary: "Gives information about the Person completing record section"
---

{% include custom/section.warnbanner.html %}

## Person Completing Record Section Content##
The Person completing record section carries information about the person who completed the record. Elements should be formatted as subheadings in any HTML sent.


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
			<td>Person completing record</td>
			<td>The details of the person who filled out the record.</td>
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
			<td>Name</td>
			<td>The name of the person completing the record, preferably in a structured format.</td>
			<td>1 only</td>
			<td>M</td>
			<td>The person name as held on the source system. Where possible this should be broken down into its constituent parts (prefix, given name, family name, and suffix) within the text and carried in the FHIR element <b>Practitioner.name</b> . An identifier for the person completing the record will be sent in the FHIR element <b>Practitioner.identifier</b>.</td>
		</tr>
		<tr>
			<td>Role</td>
			<td>The role the person is playing within the organisation at the time record was updated.</td>
			<td>1 only</td>
			<td>M</td>
			<td>The role may be held on the source system, be from an authoritative source such as SDS, or use an existing vocabulary such as the job role title (from the national workforce dataset) sent as text and carried in the FHIR element <b>PractitionerRole.code</b>.</td>
		</tr>
		<tr>
			<td>Grade</td>
			<td>The grade of the person completing the record</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>The grade of the person completing the record held on the source system or from an authoritative source<. Sent as text only.</td>
		</tr>
		<tr>
			<td>Specialty</td>
			<td>The main specialty of the person completing the record</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>The main clinical specialty as held on the source system sent as text and the specialty <b>SHOULD</b>  be populated in the <b>PractitionerRole.specialty</b>  FHIR element. The profile is currently bound to the FHIR ValueSet <a href="http://hl7.org/fhir/stu3/valueset-c80-practice-codes.html">c80-practice-codes</a> as preferred. This is proposed to be replaced by NHS Data main specialty code and therfore the current guidance is to not use the preferred ValueSet but to replace it using a code from <a href="https://www.datadictionary.nhs.uk/data_dictionary/attributes/m/main_specialty_code_de.asp?shownav=1">MAIN SPECIALTY CODE</a>. The FHIR CodeSystem element should be populated with "https://www.datadictionary.nhs.uk". As an alternative this element may be populated with a SNOMED CT concept and the FHIR CodeSystem element populated with "http://snomed.info/sct".</td>
		</tr>
		<tr>
			<td>Professional identifier</td>
			<td>Professional identifier for the person completing the record e.g., GMC number, HCPC number etc or the personal identifier used by the local organisation.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>The professional identifier type and the identifier itself of the person completing the record held on the source system. Sent as text and where supported carried in the FHIR element <b>Practitioner.identifier</b> and <b>Practitioner.identifier.type</b>.</td>
		</tr>
		<tr>
			<td>Date and time completed</td>
			<td>The date and time the record was updated.</td>
			<td>1 only</td>
			<td>M</td>
			<td>The date/time the record was updated. This will probably be a system, date taken from electronic device used to update the patient record. Sent as text and will also be carried in the FHIR element <b>Composition.date</b></td>
		</tr>
		<tr>
			<td>Contact details</td>
			<td>Contact details of the person completing the record. For example, a phone number, email address. Contact details are used to resolve queries about the record entry.</td>
			<td>0 to many</td>
			<td>O</td>
			<td>The contact details may be for the individual completing the record, or wider team details (for example a phone number for a hospital department). This will be sent as text and where supported in the FHIR elements <b>PractitionerRole.telecom</b> or <b>Practitioner.telecom</b> or <b>Organization.telecom</b>.</td>
		</tr>
		<tr>
			<td>Organisation</td>
			<td>The organisation the person completing the record works for.</td>
			<td>1 only</td>
			<td>M</td>
			<td>The name of the organisation or site, and a postal address (if available) carried in text and carried in the FHIR elements <b>Organization.name</b> and <b>Organization.address</b>. An ODS identifier for the organisation or site carried in the FHIR element <b>Organization.identifier</b>.</td>
		</tr>
		<tr>
		<td colspan="5"><b>* M=Mandatory R=Required O=Optional</b></td>
		</tr>
	</tbody>
</table>

## Example Person Completing Record Section ##

<script src="https://gist.github.com/IOPS-DEV/4eceababbca389067cde4aefd2d61cde.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK3 FHIR eDischarge does not currently support coded Person completing record information.






