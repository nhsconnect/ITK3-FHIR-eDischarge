---
title: Investigation Results Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_invest_results.html
summary: "Gives information about Investigation Results section"
---

{% include custom/section.warnbanner.html %}

## Investigation Results Section Content ##
The Investigation results section carries information about investigation results for the patient, subheadings should be formatted as such in any html sent:

<table width="100%">
<tr>
<th width="25%">Sub-section</th>
<th width="45%">Description</th>
<th width="15%">Cardinally</th>
<th width="15%">Conformance</th>
</tr>
<tr>
<td>Investigation results</td>
<td>The result of the investigation (this includes the result value, with unit of observation and reference interval where applicable and date), and plans for acting upon investigation results.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<table>

## Example Investigation Results Section ##


<script src="https://gist.github.com/IOPS-DEV/72e6cca3707440c2299d7655b60a7b23.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK FHIR eDischarge does not currently support coded investigation results.








