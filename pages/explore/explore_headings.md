---
title: eDischarge Headings
keywords:  messaging
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_headings.html
summary: "Overview of the eDischarge headings"
---

{% include custom/search.warnbanner.html %}

## Overview ##

This section provides a list of the AMoRC headings used for text sections in the ITK FHIR eDischarge based on the "Standards for the clinical structure and content of patient records" documentation. 

This section lists the following

- The headings used
- An overview of the type of information carried within the text section
- An example of a text section instance
- A list of the coded resources which may be used to give the text carried in the section in a coded format. 
 
## Typical Text Section Content ##
This diagram shows a typical text section.
Note: the examples of section HTML in this specification show only example html format such as tables. This is an exemplar format. There is no mandated format for the section HTML. 

<img src="images/explore/section_description.png" style="width:90%;max-width: 90%;"/>
 
## Headings Used By eDischarge ##

<table>
	<tr>
		<th width="40%">Section Name</th>
		<th width="20%">SNOMED Concept</th>
		<th width="13%">Cardinally</th>
		<th width="13%">Conformance</th>
		<th width="13%">Associated Coded Profiles</th>
	</tr>
	<tr>
		<td>
			<a href="explore_admission_details.html">Admission details</a>
		</td>
		<td>886781000000108</td>
	    <td>0..1</td>
		<td>Required</td>	
		<td>1</td>
	</tr>
	<tr>
		<td>
			<a href="explore_allergies_and_adverse_reactions.html">Allergies and adverse reactions</a>
		</td>
		<td>886921000000105</td>
		<td>1..1</td>
		<td>Mandatory</td>
		<td>2</td>
	</tr>
	<tr>
		<td>
			<a href="explore_assessment_scales.html">Assessment scales</a>
		</td>
		<td>887141000000103</td>
    	<td>0..1</td>
		<td>Optional</td>
		<td>0</td>
	</tr>
	<tr>
		<td>
			<a href="explore_clinical_summary.html">Clinical summary</a>
		</td>
		<td>887181000000106</td>
    	<td>1..1</td>
		<td>Mandatory</td>
		<td>0</td>
	</tr>
	<tr>
		<td>
			<a href="explore_diagnosis.html">Diagnoses</a>
		</td>
		<td>887161000000102</td>
    	<td>1..1</td>
		<td>Mandatory</td>
		<td>2</td>
	</tr>
	<tr>
		<td>
			<a href="explore_discharge_details.html">Discharge details</a>
		</td>
		<td>886811000000106</td>
    	<td>0..1</td>
		<td>Required</td>
		<td>1</td>
	</tr>
	<tr>
		<td>
			<a href="explore_distribution_list.html">Distribution list</a>
		</td>
		<td>887261000000109</td>
    	<td>0..1</td>
		<td>Required</td>
		<td>4</td>
	</tr>
	<tr>
		<td>
			<a href="explore_gp_practice.html">GP practice</a>
		</td>
		<td>886711000000101</td>
    	<td>1..1</td>
		<td>Mandatory</td>
		<td>2</td>
	</tr>
	<tr>
		<td>
			<a href="explore_individual_reqs.html">Individual requirements</a>
		</td>
		<td>1052901000000109</td>
    	<td>0..1</td>
		<td>Required</td>
		<td>0</td>
	</tr>
	<tr>
		<td>
			<a href="explore_information_given.html">Information and advice given</a>
		</td>
		<td>1052951000000105</td>
    	<td>0..1</td>
		<td>Required</td>
		<td>0</td>
	</tr>
	<tr>
		<td>
			<a href="explore_invest_results.html">Investigation results</a>
		</td>
		<td>1082101000000102</td>
    	<td>0..1</td>
		<td>Optional</td>
		<td>0</td>
	</tr>
	<tr>
		<td>
			<a href="explore_legal_info.html">Legal information</a>
		</td>
		<td>886961000000102</td>
    	<td>0..1</td>
		<td>Required</td>
		<td>0</td>
	</tr>
	<tr>
		<td>
			<a href="explore_medication.html">Medications and Medical Devices</a>
		</td>
		<td>933361000000108</td>
    	<td>0..1</td>
		<td>Optional</td>
		<td>2</td>
	</tr>
	<tr>
		<td>
			<a href="explore_part_research.html">Participation in research</a>
		</td>
		<td>886751000000102</td>
    	<td>0..1</td>
		<td>Optional</td>
		<td>0</td>
	</tr>
	<tr>
		<td>
			<a href="explore_patient_demographics.html">Patient demographics</a>
		</td>
		<td>886731000000109</td>
    	<td>1..1</td>
		<td>Mandatory</td>
		<td>1</td>
	</tr>
	<tr>
		<td>
			<a href="explore_pat_care_concerns.html">Patient and carer concerns,expectations and wishes</a>
		</td>
		<td>1052941000000107</td>
    	<td>0..1</td>
		<td>Required</td>
		<td>0</td>
	</tr>
	<tr>
		<td>
			<a href="explore_per_com_record.html">Person completing record</a>
		</td>
		<td>887231000000104</td>
    	<td>1..1</td>
		<td>Mandatory</td>
		<td>0</td>
	</tr>
	<tr>
		<td>
			<a href="explore_plan_req_actions.html">Plan and requested actions</a>
		</td>
		<td>887201000000105</td>
    	<td>0..1</td>
		<td>Required</td>
		<td>0</td>
	</tr>
	<tr>
		<td>
			<a href="explore_procedures.html">Procedures</a>
		</td>
		<td>887171000000109</td>
    	<td>0..1</td>
		<td>Optional</td>
		<td>1</td>
	</tr>
	<tr>
		<td>
			<a href="explore_referrer.html">Referrer details</a>
		</td>
		<td>1052891000000108</td>
    	<td>0..1</td>
		<td>Required</td>
		<td>0</td>
	</tr>
	<tr>
		<td>
			<a href="explore_safety_alerts.html">Safety alerts</a>
		</td>
		<td>886931000000107</td>
    	<td>0..1</td>
		<td>Required</td>
		<td>0</td>
	</tr>
	<tr>
		<td>
			<a href="explore_social_context.html">Social context</a>
		</td>
		<td>887051000000101</td>
    	<td>0..1</td>
		<td>Optional</td>
		<td>0</td>
	</tr>
</table>


## Overview of eDischarge Sections and Coded profiles ##
This diagram illustrates the sections used in eDischarge and which sections allow coded representation of the section text. 


<img src="images/explore/eDIS_composition_overview.png" style="width:100%;height: auto;"/>



The text sections are carried in the FHIR composition resource. 
This is profiled as the [ITK-EDIS-Composition](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-EDIS-Composition-1)


{% include custom/section.warnbanner.html %}


