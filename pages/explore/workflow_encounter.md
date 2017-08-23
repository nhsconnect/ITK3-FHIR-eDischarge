---
title: Work flow
keywords: workflow
tags: [development,fhir,profiles]
sidebar: overview_sidebar
permalink: workflow_encounter.html
summary: "Overview of work flow using encounter resource."
---

{% include custom/search.warnbanner.html %}

## Overview ##

The eDischarge does not support any real "workflow" but uses the encounter resource to give context to the information contained in the eDischarge document. The encounter resource represent the inpatient stay and can contain important information such as:
 
- When the patient was admitted
- Why the patient was admitted
- when the patient was discharged
- when the patient was discharged to
- Who was involved in the encounter

The encounter can be referenced by the following resources:

- Composition
- Condition 
- Flag
- List
- MedicationStatement
- Observation
- Procedure

## Example Encounter ##

<script src="https://gist.github.com/IOPS-DEV/66bff9022f16f8341ec1f7b77391ac23.js"></script>




