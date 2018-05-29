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
The Investigation results section carries information about investigation results for the patient. Elements should be formatted as subheadings in any HTML sent.

<table style="width:100%;max-width: 100%;">
	<thead>
		<tr>
			<th width="18%">Section</th>
			<th width="30%">Description</th>
			<th width="11%">Cardinality</th>
			<th width="11%">MRO*</th>
			<th width="30%">Values</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Investigation results</td>
			<td>A record of investigations and procedures requested, results and plans.</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>&nbsp;</td>
		</tr>
		<tr>
			<th>Element</th>
			<th>Description</th>
			<th>Cardinality</th>
			<th>MRO*</th>
			<th>Values</th>
		</tr>
		<tr>
			<td>Investigation result</td>
			<td>For each investigation, the result of the investigation (this includes the result value, with unit of observation and reference interval where applicable and date, and plans for acting upon investigation results.</td>
			<td>0 to many</td>
			<td>optional</td>
			<td>If possible, this should include only results which are important or relevant to communicate to the GP. Hence health professional may need to select them. Text. (Note that work is underway to standardise recording of pathology investigation results, which will inform content under this heading.)</td>
		</tr>
	</tbody>
</table>


## Example Investigation Results Section ##

<script src="https://gist.github.com/IOPS-DEV/72e6cca3707440c2299d7655b60a7b23.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK3 FHIR eDischarge does not currently support coded investigation results.








