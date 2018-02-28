---
title: Plan and requested actions Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_plan_req_actions.html
summary: "Gives information about the Plan and requested actions section"
---

{% include custom/section.warnbanner.html %}

## Plan and Requested Actions Content ##
The Plan and requested actions section carries information about planned and requested actions such as planned investigations, procedures etc, subheadings should be formatted as such in any html sent:

<table width="100%">
<tr>
<th width="25%">Sub-section</th>
<th width="45%">Description</th>
<th width="15%">Cardinally</th>
<th width="15%">Conformance</th>
</tr>
<tr>
<td>Actions for healthcare professionals
</td>
<td>Including planned investigations, procedures, interventions and treatment for a patient’s identified conditions and priorities. For each action the following should be identified: 
<ol><li>Person responsible - name and designation / department / hospital / patient etc or role (eg GP) responsible for carrying out the proposed action, and where action should take place.</li>
<li>Status - requested, planned or completed.</li> 
<li>When action requested for - requested date, time, or period - as relevant.</li>                                                       <li>Suggested strategies - suggested strategies for potential problems.</li>
<li>Outcome expectations, including patient’s expectations.</li>
</ol>
</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Actions for patient or their carer</td>
<td>"For each action the following should be identified:                                                    a) person responsible - name and designation eg patient or carer responsible for carrying out the proposed action, and where action should take place.
b) status - requested, planned or completed.                                              c)  When action requested for - requested date, time, or period - as relevant.                                                       d) suggested strategies - suggested strategies for potential problems, eg telephone contact for advice.
e) outcome expectations, including patient’s expectations. "
</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Agreed with patient or legitimate patient representative
</td>
<td>Indicates whether the patient or legitimate representative has agreed the entire plan or individual aspects of treatment, expected outcomes, risks and alternative treatments.
</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Investigations requested
</td>
<td>This includes a name or description of the investigation requested and the date requested. </td>  
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Procedures requested
</td>
<td>These are the diagnostic or therapeutic procedures that have actually been requested (and the date requested).
</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
</table>

##  Example Plan and Requested Actions Section ##

<script src="https://gist.github.com/IOPS-DEV/1bdcde4481d7de7dfdf7bcc266529e10.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK FHIR eDischarge does not currently support coded Plan and requested actions information.






