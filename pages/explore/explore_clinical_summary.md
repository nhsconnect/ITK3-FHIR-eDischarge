---
title: Clinical Summary Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_clinical_summary.html
summary: "Gives information about the Clinical summary section"
---

{% include custom/section.warnbanner.html %}

## Clinical Summary Section Content##
The Clinical summary section carries a narrative summary of the episode. Where possible, very brief, subheadings should be formatted as such in any html sent:

<table width="100%">
<tr>
<th width="25%">Sub-section</th>
<th width="45%">Description</th>
<th width="15%">Cardinally</th>
<th width="15%">Conformance</th>
</tr>
<tr>
<td>Clincal summary</td>
<td>This may include interpretation of findings and results; differential diagnoses, opinion and specific action(s). Planned actions will be recorded under ‘plan’.</td>
<td>x</td>
<td>x</td>
</tr>
</table>

##  Example Clinical Summary Section ##

<script src="https://gist.github.com/IOPS-DEV/77620f7d132b195c42b5f2fee5f39172.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK FHIR eDischarge does not currently support a coded clinical summary.






