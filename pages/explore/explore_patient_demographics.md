---
title: Patient Demographics Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_patient_demographics.html
summary: "Gives information about the patient"
---
{% include custom/non_text_section.warnbanner.html %}


## Patient Demographics Section Content##

The Patient demographics section is rendered from the patient resource.The resource used is:
 
- **[CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)** - A CareConnect Profile for patient. The Patient resource represents the patient involved in the provision of healthcare related services.

Items in bold are subheadings and should be formatted as such when rendered: 

<ul>
<li><b>Patient name</b></li>
The full name of the patient.
Also patient preferred name: the name by which a patient wishes to be addressed.
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






