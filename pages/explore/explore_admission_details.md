---
title: Admission Details Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_admission_details.html
summary: "Gives information about the Admission details section"
---

{% include custom/section.warnbanner.html %}

## Admission Details Section Content##
The Admission details section carries information about the patient's admission, subheadings should be formatted as such in any html sent:

<table width="100%">
<tr>
<th width="25%">Sub-section</th>
<th width="45%">Description</th>
<th width="15%">Cardinally</th>
<th width="15%">Conformance</th>
</tr>
<tr>
<td>Reason for admission</td>
<td>The health problems and issues experienced by the patient that prompted the decision to admit to hospital e.g. chest pain, mental health crisis, blackout, fall,  a specific procedure, intervention, investigation or treatment, non compliance with treatment.</td>
<td>1..1</td>
<td>M</td>
</tr>
<tr>
<td>Admission method</td>
<td>How the patient was admitted to hospital. Eg: elective, emergency, maternity, transfer, etc.</td>
<td>1..1</td>
<td>M</td>
</tr>
<tr>
<td>Source of admission</td>
<td>Where the patient was immediately prior to admission, eg, usual place of residence, temporary place of residence, penal establishment. National code.</td>
<td>1..1</td>
<td>M</td>
</tr>
<tr>
<td>Date/Time of admission</td> 
<td>Date and time patient admitted to hospital.</td>
<td>1.1</td>
<td>M</td>
</tr>
</table>

##  Example Admission Details Section ##

<script src="https://gist.github.com/IOPS-DEV/063615bfb87522015e0c37ef7f06d4fd.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- [Encounter](workflow_encounter.html)






