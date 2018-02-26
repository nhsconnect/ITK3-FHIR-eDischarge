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
<li><b>Date of birth</b></li>
The date of birth of the patient.
<li><b>Patient sex</b></li>
Sex at birth. Determines how the individual will be treated clinically.
<li><b>Gender</b></li>
As the patient wishes to portray themselves.
<li><b>Ethnicity</b></li>
The ethnicity of a person as specified by the person.
<li><b>NHS number</b></li>
The unique identifier for a patient within the NHS in England and Wales.
<li><b>Other identifier</b></li>
Country specific or local identifier, eg, Community Health Index (CHI) in Scotland.
Two data items:
<ol>
<li>type of identifier</li>
<li>identifier</li>
</ol>
<li><b>Patient address</b></li>
Patient usual place of residence.
<li><b>Patient telephone number</b></li>
Telephone contact details of the person. To include, eg, mobile, work and home number if available.
Two data items:
<ol><li>type</li>
<li>number</li>
</ol>
<li><b>Patient email address</b></li>
Email address of the patient.</ul>


## Example Patient Demographics Using Patient Resource ##

<script src="https://gist.github.com/IOPS-DEV/af79cf398178936f11f5eb5c5d45c13c.js"></script>






