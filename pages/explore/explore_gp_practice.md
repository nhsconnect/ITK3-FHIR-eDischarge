---
title: GP Practice Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_gp_practice.html
summary: "Gives information about the patient's GP Practice"
---
{% include custom/section.warnbanner.html %}


## GP Practice Section Content##

The GP practice section contains details of the patients GP practice. Elements should be formatted as subheadings in any HTML sent.
 
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
			<td>GP practice </td>
			<td>Details of the GP practice where the patient is registered.</td>
			<td>1 only</td>
			<td>mandatory</td>
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
			<td>GP name</td>
			<td>Where the patient or patient's representative offers the name of a GP as their usual GP</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>Patients are registered with GP Practices, so their usual GP name will be something volunteered by the patient or their representative</td>
		</tr>
		<tr>
			<td>GP practice details</td>
			<td>Name and address of the patient's registered GP Practice</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>Registered GP Practice details are available from the Patient Demographics Service (PDS), or volunteered from the patient or their representative or provided by referral contact. Include details of the Practice name and address</td>
		</tr>
		<tr>
			<td>GP practice identifier</td>
			<td>The identifier of the registered GP Practice.</td>
			<td>1 only</td>
			<td>mandatory</td>
			<td>This should be the Organisation Data Services (ODS) identifier for the practice (not displayed in the message). This includes codes to use where there is no registered GP practice.</td>
		</tr>
	</tbody>
</table>


## Example GP Practice Section ##

<script src="https://gist.github.com/IOPS-DEV/0254c9b07fa77cd926dbe0b5a68ff4d8.js"></script>








