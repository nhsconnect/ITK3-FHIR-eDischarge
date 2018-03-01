---
title: Patient Demographics Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_patient_demographics.html
summary: "Gives information about the patient"
---
{% include custom/section.warnbanner.html %}


## Patient Demographics Section Content##
The Patient demographics section contains information about the patient, sub headings should be rendered as such in any html sent.

<table>
	<thead>
		<tr>
			<th width="20%">Section</th>
			<th width="28%">Description</th>
			<th width="12%">Cardinality</th>
			<th width="12%">MRO*</th>
			<th width="28%">Values</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Patient demographics</td>
			<td>Patient details and contact information.</td>
			<td>1 only</td>
			<td>mandatory</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<td>Element</td>
			<td>Description</td>
			<td>Cardinality</td>
			<td>MRO*</td>
			<td>Values</td>
		</tr>
		<tr>
			<td>Patient name</td>
			<td>The full name of the patient</td>
			<td>1 only</td>
			<td>mandatory</td>
			<td>The legal name of the patient from the Patient Demographics Service (PDS), or the name volunteered by the patient.</td>
		</tr>
		<tr>
			<td>Patient preferred name</td>
			<td>The name by which a patient wishes to be addressed.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>The preferred name volunteered by the patient and recorded on the Patient Administration System (PAS), or a preferred name given by PDS that the patient has asked to be called by.</td>
		</tr>
		<tr>
			<td>Date of birth</td>
			<td>The date of birth of the patient.</td>
			<td>1 only</td>
			<td>mandatory</td>
			<td>The date of birth of the patient taken from PDS, or the date of birth volunteered by the patient (as recorded on the PAS (Patient Administration System). The date of birth will be as precise as possible, but should at least contain a year</td>
		</tr>
		<tr>
			<td>Gender</td>
			<td>The patient's gender.  As the patient wishes to portray themselves.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>0 Not known1 Male2 Female9 Not specified</td>
		</tr>
		<tr>
			<td>NHS number</td>
			<td>The unique identifier for a patient within the NHS in England and Wales.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>"Sent as per the NHS Data Dictionary NHS number.</td>
		</tr>
		<tr>
			<td>        </td>
		</tr>
		<tr>
			<td>      Traced NHS Numbers only should be used."</td>
		</tr>
		<tr>
			<td>Other identifier</td>
			<td>Country specific or local identifier, e.g., Community Health Index (CHI) in Scotland. Two data items: type of identifier and identifier.</td>
			<td>0 to many</td>
			<td>required</td>
			<td>Recorded as per: NHS Data Dictionary - local identifier.The assigning authority should also be supplied along with the country or local identifier.</td>
		</tr>
		<tr>
			<td>Patient address</td>
			<td>Patient's usual place of residence.</td>
			<td>1 only</td>
			<td>mandatory</td>
			<td>Sent in accordance with the NHS Data Dictionary: patient usual address. May be auto generated from PDS, GP referral record, or from the local PAS.</td>
		</tr>
		<tr>
			<td>Patient email address</td>
			<td>Email address of the patient</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>Set in accordance with the NHS Data Dictionary: contact email address (patient or lead contact). May be auto generated from PDS, GP referral record, or from the local PAS.</td>
		</tr>
		<tr>
			<td>Patient telephone number</td>
			<td>Telephone contact details of the patient. To include, e.g., mobile, work and home number if available.</td>
			<td>0 to many</td>
			<td>optional</td>
			<td>Contact details may come from PDS, or those recorded on the local PAS.Both the actual contact number and its use (work number, home number, mobile number etc.) should be sent.</td>
		</tr>
		<tr>
			<td>Relevant contacts</td>
			<td>Include the most important contacts including:*Personal contacts e.g., next of kin, in case of emergency contact, lasting power of attorney, dependants, informal carers etc.*Health/care professional contacts e.g., social worker, hospital clinician, care coordinator, Independent Mental Capacity Advocate (IMCA) etc.Name, relationship, role (if formal role), contact details and availability, eg out of hours.</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>Details of relevant contacts, such as carers or family members, as recorded on the local system, or volunteered by the patient. This will be a free text list of relevant contacts.</td>
		</tr>
	</tbody>
</table>

## Example Patient Demographics Using Patient Resource ##

<script src="https://gist.github.com/IOPS-DEV/af79cf398178936f11f5eb5c5d45c13c.js"></script>






