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

<table width="100%">
<tr>
<th width="25%">Sub-section</th>
<th width="45%">Description</th>
<th width="15%">Cardinally</th>
<th width="15%">Conformance</th>
</tr>
<tr>
<td>Patient name</td>
<td>The full name of the patient.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Patient preferred name</td>
<td>The name by which a patient wishes to be addressed.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Date of birth</td>
<td>The date of birth of the patient.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Gender</td>
<td>As the patient wishes to portray themselves.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>NHS number</td>
<td>The unique identifier for a patient within the NHS in England and Wales.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Other identifier</td>
<td>Country specific or local identifier, eg, Community Health Index (CHI) in Scotland.
Two data items:type of identifier and identifier</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Patient address</td>
<td>Patient usual place of residence.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Patient email address</td>
<td>Email address of the patient</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Patient telephone number</td>
<td>Telephone contact details of the person. To include, eg, mobile, work and home number if available.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Relevant contacts</td>
<td>"Include the most important contacts including:<br/>
Personal contacts e.g., next of kin, in case of emergency contact, lasting power of attorney, dependants, informal carers etc.<br/>
Health/care professional contacts e.g., social worker, hospital clinician, care coordinator, key worker, Independent Mental Capacity Advocate (IMCA) etc. Name, relationship, role (if formal role), contact details and availability, e.g. out of hours.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Communication preferences</td>
<td>Preferred contact method, eg, sign language, letter, phone, etc. Also preferred written communication format, eg, large print, braille.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
</table>

## Example Patient Demographics Using Patient Resource ##

<script src="https://gist.github.com/IOPS-DEV/af79cf398178936f11f5eb5c5d45c13c.js"></script>






