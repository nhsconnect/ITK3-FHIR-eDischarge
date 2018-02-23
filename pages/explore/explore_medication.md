---
title: Medications and Medical Devices Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_medication.html
summary: "Gives information about the Medications and medical devices section"
---

{% include custom/section.warnbanner.html %}

## Medications and Medical Devices Section Content ##
The Medications and medical devices section carries information about the patient's medication , subheadings should be formatted as such in any html sent:

<table width="100%">
<tr>
<th width="25%">Sub-section</th>
<th width="45%">Description</th>
<th width="15%">Cardinally</th>
<th width="15%">Conformance</th>
</tr>

<tr>
<td>Medication name</td>
<td>May be generic name or brand name (as appropriate).</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>

<tr>
<td>Medication form</td>
<td>Eg capsule, drops, tablet, lotion etc.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>

<tr>
<td>Route</td>
<td>Medication administration description (oral, IM, IV, etc): may include method of administration (eg, by infusion, via nebuliser, via NG tube) and/or site of use (eg, ‘to wound’, ‘to left eye’, etc).</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>

<tr>
<td>Dose</td>
<td>This is a record of the total amount of the active ingredient(s) to be given at each administration. It should include, eg, units of measurement, number of tablets, volume/concentration of liquid, number of drops, etc.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>

<tr>
<td>Medication frequency</td>
<td>Frequency of taking or administration of the therapeutic agent or medication.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>

<tr>
<td>Additional instructions</td>
<td>Allows for: requirements for adherence support, eg, compliance aids, prompts and packaging requirements</td>
<td>0..1</td>
<td>required</td>
</tr>

<tr>
<td>Do not discontinue warning</td>
<td>To be used on a case-by-case basis if it is vital not to discontinue a medicine in a specific patient scenario.</td>
<td>0..1</td>
<td>Required</td>
</tr>

<tr>
<td>Reason for medication</td>
<td>Reason for medication being prescribed, where known.</td>
<td>0..1</td>
<td>Required</td>
</tr>

<tr>
<td>Medication recommendations</td>
<td>Suggestions about duration and/or review, ongoing monitoring requirements, advice on starting, discontinuing or changing medication.</td>
<td>0..1</td>
<td>Required</td>
</tr>

<tr>
<td>Medication change</td>
<td>Where a change is made to the medication, ie, one drug stopped and another started, or, eg, dose, frequency or route is changed.</td>
<td>0..1</td>
<td>Required</td>
</tr>

<tr>
<td>Reason for medication change</td>
<td>Reason for change in medication, eg, sub-therapeutic dose, patient intolerant.</td>
<td>0..1</td>
<td>Required</td>
</tr>

<tr>
<td>Medical devices</td>
<td>The record of dietary supplements, dressings and equipment that the patient is currently taking or using.</td>
<td>0..1</td>
<td>Required</td>
</tr>

</table>


## Example Medications and Medical Devices Section ##

<script src="https://gist.github.com/IOPS-DEV/0a5596bdf4ab2c880eacb409e44c09df.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- List
- MedicationStatement
- Flag
 
See constructing coded clinical structures - [Medication Lists](build_medication_lists.html)











