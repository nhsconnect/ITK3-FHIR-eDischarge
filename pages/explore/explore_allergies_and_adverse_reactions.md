---
title: Allergies and Adverse Reactions Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_allergies_and_adverse_reactions.html
summary: "Gives information about the Allergies and adverse reactions section"
---

{% include custom/section.warnbanner.html %}

## Allergies and Adverse Reactions Section Content##
The Allergies and adverse reactions section carries information about the patient's allergies and adverse reactions. Elements should be formatted as subheadings in any HTML sent.
This table should be used in conjunction with the section on [constructing clinical coded structures](build_allergy_lists.html) for further information on constructing and coding allergy lists. 

<table style="width:100%;max-width: 100%;">
	<thead>
		<tr>
			<th width="15%">Section</th>
			<th width="35%">Description</th>
			<th width="5%">Card.</th>
			<th width="5%">MRO*</th>
			<th width="40%">M=Mandatory R=Required O=Optional</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Allergies and adverse reactions</td>
			<td>The details of any known allergies, intolerances or adverse reactions.</td>
			<td>1 only</td>
			<td>M</td>
			<td>Note: Some information may be text only for example "No known drug allergies or adverse reactions" and "Information not available" for further information see the section on <a href="build_allergy_lists.html">Constructing Medication Lists.</a>. </td>
		</tr>
		<tr>
			<th>PRSB Element</th>
			<th>Description</th>
			<th>Card.</th>
			<th>MRO*</th>
			<th>Guidance</th>		
		</tr>
		<tr>
			<td>Causative agent</td>
			<td>The agent such as food, drug or substances that has caused or may cause an allergy, intolerance or adverse reaction in this patient.</td>
			<td>1 only</td>
			<td>M</td>
			<td>Text and a SNOMED CT concept carried in the CodeableConcept of AllergyIntolerance.code FHIR element. For further information on coding causative agent see <a href="build_allergy_lists.html#causative-agent">Constructing Medication Lists.</a></td>
		</tr>
		<tr>
			<th>Reaction details cluster</th>
			<th>&nbsp;</th>
			<th>&nbsp;</th>
			<th>&nbsp;</th>
			<th>&nbsp;</th>
		</tr>
		<tr>
			<td>Description of reaction</td>
			<td>A description of the manifestation of the allergic or adverse reaction experienced by the patient. For example, skin rash.</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text derived from SNOMED CT</td>
		</tr>
		<tr>
			<td>Date recorded</td>
			<td>The date that the reaction was clinically recorded/asserted. This will often equate to the date of onset of the reaction but this may not be wholly clear from source data.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>The date that the reaction was clinically recorded/asserted. Text and carried in AllergyIntolerance.assertedDate FHIR element.</td>
		</tr>
		<tr>
			<td>Severity</td>
			<td>A description of the severity of the reaction</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>Text derived from SNOMED CT</td>
		</tr>
		<tr>
			<td>Certainty</td>
			<td>A description of the certainty that the stated causative agent caused the allergic or adverse reaction.</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>Text derived from SNOMED CT</td>
		</tr>
		<tr>
			<td>Comment</td>
			<td>Any additional comment or clarification about the adverse reaction.</td>
			<td>0 to 1</td>
			<td>required</td>
			<td>Free text</td>
		</tr>
		<tr>
			<td>Type of reaction</td>
			<td>The type of reaction experienced by the patient (allergic, adverse, intolerance)</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>Text derived from SNOMED CT</td>
		</tr>
		<tr>
			<td>Evidence</td>
			<td>Results of investigations that confirmed the certainty of the diagnosis. Examples might include results of skin prick allergy tests</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>Free text</td>
		</tr>
		<tr>
			<td>Probability of recurrence</td>
			<td>Probability of the reaction (allergic, adverse, intolerant) occurring</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>Free text</td>
		</tr>
		<tr>
			<td>Date first experienced</td>
			<td>When the reaction was first experienced. May be a date or partial date (e.g. year) or text (e.g. during childhood)</td>
			<td>0 to 1</td>
			<td>optional</td>
			<td>Free text</td>
		</tr>
	</tbody>
</table>




##  Example Allergies and Adverse Reactions Sections ##

### Allergy to Penicillin ###

<script src="https://gist.github.com/IOPS-DEV/c02f9626ad71d2230cd51ded6d031bb2.js"></script>

### "No known allergy" ###

<script src="https://gist.github.com/IOPS-DEV/3f77d2ebcfcdf305a640484fb445cc1a.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- List
- AllergyIntolerance
 
See constructing clinical coded structures - [Allergy Lists](build_allergy_lists.html)











