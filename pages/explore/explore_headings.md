---
title: eDischarge Headings
keywords:  messaging
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_headings.html
summary: "Overview of the eDischarge headings"
---


{% include custom/section.warnbanner.html %}

## Overview ##

This section provides a list of the PRSB headings used for text sections in the ITK3 FHIR eDischarge based on the "Standards for the clinical structure and content of patient records" documentation. 

This section lists the following

- The headings used
- An overview of the type of information carried within the text section
- An example of a text section instance
- A list of the coded resources which may be used to give the text carried in the section in a coded format. 
 
## Typical Text Section Content ##
This diagram shows the elements of a typical text section which is found in the FHIR Composition Resource.
Note: the examples of section HTML in this specification show only example HTML format such as tables. This is an exemplar format. There is no mandated format for the section HTML. 

<img src="images/explore/section_description.png" style="width: 100%;max-width: 100%;">

## Must Support Property ##
Some elements in the Composition Resource used within ITK3 Transfer of Care documents have the must support property set to "true".  
These are :
- Composition.extension(careSettingTypeExtension)
- Composition.identifier
- Composition.status
- Composition.type
- Composition.subject
- Composition.encounter
- Composition.date
- Composition.author
- Composition.title
- Composition.custodian
- Composition.relatesTo
- Composition.section(slice) Where slice=The PRSB headings for the ITK3 Transfer of Care document type.

The “must support” property has been added to all the elements that must be supported regardless of cardinality.  Whether the conformance of the element is mandatory or optional has no relevance for the “must support” property. This means that for sending or receiving systems to claim conformance to any ITK3 Transfer of Care Composition Profile the following MUST be true:

- The sending system MUST support the creation and sending of all the elements in the list above.
- The sending system MUST support the creation and sending of all Composition.section slices with the specified sub-elements and narrative.* See Note 1. 
- The receiving system MUST support the processing of all the elements in the list above.  
- The receiving system MUST support the display of all Composition.section slices with the specified sub-elements and narrative.

**Note 1** - There are rules around when sections are sent or not sent in a document. These are specified in the document headings sections.


## Headings Used By eDischarge ##

<table>
	<tr>
		<th width="40%">Section Name</th>
		<th width="20%">SNOMED Concept</th>
		<th width="13%">Cardinality</th>
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
			<a href="explore_diagnoses.html">Diagnoses</a>
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
		<td>1078911000000106</td>
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
			<a href="explore_pat_care_concerns.html">Patient and carer concerns, expectations and wishes</a>
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
			<a href="explore_referrer_details.html">Referrer details</a>
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

<a href="images/explore/eDIS_composition_overview.png" target="_blank" style="width: 100%;max-width: 100%;"><b>Click to open in a new window</b></a>

<img src="images/explore/eDIS_composition_overview.png" style="width:auto;height: auto;"/>


The text sections are carried in the FHIR Composition Resource. 

This is profiled as the [ITK-EDIS-Composition](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-EDIS-Composition-1)





