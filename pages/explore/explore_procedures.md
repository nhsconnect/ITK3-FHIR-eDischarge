---
title: Procedures Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_procedures.html
summary: "Gives information about the Procedures section"
---

{% include custom/section.warnbanner.html %}

## Procedures Section Content##
The Procedures section carries information about the procedures that have been performed on the patient, subheadings should be formatted as such in any html sent:

<table width="100%">
<tr>
<th width="25%">Sub-section</th>
<th width="45%">Description</th>
<th width="15%">Cardinally</th>
<th width="15%">Conformance</th>
</tr>
<tr>
<td>Procedure</td>
<td>The therapeutic procedure performed. This could include site and must include laterality where applicable.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Complications related to procedure</td>
<td>Details of any intra-operative complications encountered during the procedure, arising during the patient’s stay in the recovery unit or directly attributable to the procedure. The intent is to be plain text and/or images but use codes wherever possible.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Specific anaesthesia issues</td>
<td>Details of any adverse reaction to any anaesthetic agents including local
anaesthesia. Problematic intubation, transfusion reaction, etc.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
</table>


##  Example Procedures Sections ##

<script src="https://gist.github.com/IOPS-DEV/9aac8ea1c4e276ff1316608ea53b0c8e.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- Procedures
 
See constructing coded clinical structures - [Procedures](build_procedures.html)











