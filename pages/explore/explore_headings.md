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
Note: the examples of section html in this specification show only example html format such as tables. This is a exemplar format. There is no mandated format for the section html. 

<img src="images/explore/section_description.png" style="width:90%;max-width: 90%;"/>
 
## Headings Used By eDischarge ##

- [Admission details](explore_admission_details.html)
- [Allergies and adverse reactions](explore_allergies_and_adverse_reactions.html)
- [Assessment scales](explore_assessment_scales.html)
- [Clinical summary](explore_clinical_summary.html)
- [Diagnoses](explore_diagnosis.html)
- [Discharge details](explore_discharge_details.html)
- [Distribution list](explore_distribution_list.html)
- [GP Practice](explore_gp_practice.html)
- [Individual requirements](explore_individual_reqs.html)
- [Information and advice given](explore_information_given.html)
- [Investigations and procedures requested](explore_invest_and_proc_req.html)
- [Investigation results](explore_invest_results.html)
- [Legal information](explore_legal_info.html)
- [Medications and medical devices](explore_medication.html)
- [Participation in research](explore_part_research.html)
- [Patient demographics](explore_patient_demographics.html)
- [Patient and carer concerns,expectations and wishes](explore_pat_care_concerns.html)
- [Person completing record](explore_per_com_record.html)
- [Plan and requested actions](explore_plan_req_actions.html)
- [Procedures](explore_procedures.html)
- [Referrer details](explore_referrer.html)
- [Safety alerts](explore_safety_alerts.html)
- [Social context](explore_social_context.html)


## Overview of eDischarge Sections and Coded profiles ##
This diagram illustrates the sections used in eDischarge and which sections allow coded representation of the section text. 


<img src="images/explore/eDIS_composition_overview.png" style="height:90%;max-height: 90%;"/>



The text sections are carried in the FHIR composition resource. 
This is profiled as the [ITK-EDIS-Compostion](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-EDIS-Composition-1)


{% include custom/section.warnbanner.html %}


{% include custom/messaging_overview.svg %}