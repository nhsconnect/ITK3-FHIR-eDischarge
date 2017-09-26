---
title: Medications and Medical Devices Section
keywords:  messaging, sections
tags: [fhir,messaging,sections]
sidebar: foundations_sidebar
permalink: explore_medication.html
summary: "Gives information about the Medications and medical devices section"
---

{% include custom/section.warnbanner.html %}

## Medications and Medical Devices Section Content ##
The Medications and medical devices section carries information about the patient's medication , items in bold are subheadings and should be formatted as such in any html sent:

<ul><li><b>Medication name,</b> - May be generic name or brand name (as appropriate).</li>
<li><b>Medication form</b> - Eg capsule, drops, tablet, lotion etc.</li>
<li><b>Route</b> - Medication administration description (oral, IM, IV, etc): may include method of administration (eg, by infusion, via nebuliser, via NG tube) and/or site of use (eg, ‘to wound’, ‘to left eye’, etc).</li>
<li><b>Dose</b> - This is a record of the total amount of the active ingredient(s) to be given at each administration. It should include, eg, units of measurement, number of tablets, volume/concentration of liquid, number of drops, etc.</li>
<li><b>Medication frequency</b> - Frequency of taking or administration of the therapeutic agent or medication.</li>
<li><b>Additional instructions</b> - Allows for:</li>
<ul><li>requirements for adherence support, eg, compliance aids, prompts and packaging requirements</li>
<li>additional information about specific medicines, eg, where specific brand required</li>
<li>patient requirements, eg, unable to swallow tablets.</li></ul>
<li><b>Do not discontinue warning</b> - To be used on a case-by-case basis if it is vital not to discontinue a medicine in a specific patient scenario.</li>
<li><b>Reason for medication</b> - Reason for medication being prescribed, where known.</li>
<li><b>Medication recommendations</b> - Suggestions about duration and/or review, ongoing monitoring requirements, advice on starting, discontinuing or changing medication.</li>
<li><b>Medication change</b> - Where a change is made to the medication, ie, one drug stopped and another started, or, eg, dose, frequency or route is changed.</li>
<li><b>Reason for medication change</b> - Reason for change in medication, eg, sub-therapeutic dose, patient intolerant.</li>
<li><b>Medical devices</b> - The record of dietary supplements, dressings and equipment that the patient is currently taking or using.</li></ul>


## Example Medications and Medical Devices Section ##

<script src="https://gist.github.com/IOPS-DEV/0a5596bdf4ab2c880eacb409e44c09df.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- List
- MedicationStatement
- MedicationOrder
- Flag
 
See constructing coded clinical structures - [Medication Lists](build_medication_lists.html)


{% include custom/messaging_overview.svg %}








