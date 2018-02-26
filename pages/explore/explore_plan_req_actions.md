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
<td>Actions</td>
<td>Including planned investigations, procedures, Interventions and treatment for a patient’s identified conditions and priorities. For each action the following should be identified: 
<ol><li>person responsible - name and designation / department / hospital / patient etc or role (eg GP) responsible for carrying out the proposed action, and where action should take place.</li>
<li>status - requested, planned or completed.</li> 
<li>When action requested for - requested date, time, or period - as relevant.</li>                                                       <li>suggested strategies - suggested strategies for potential problems.</li>
<li>outcome expectations, including patient’s expectations.</li>
</td>
</tr>
</table>

##  Example Plan and Requested Actions Section ##

<script src="https://gist.github.com/IOPS-DEV/1bdcde4481d7de7dfdf7bcc266529e10.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK FHIR eDischarge does not currently support coded Plan and requested actions information.






