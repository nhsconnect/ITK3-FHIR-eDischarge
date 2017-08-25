---
title: Clinical Summary Section
keywords:  messaging, sections
tags: [fhir,messaging,sections]
sidebar: foundations_sidebar
permalink: explore_clinical_summary.html
summary: "Gives information about the Clinical summary section"
---

{% include custom/section.warnbanner.html %}

## Clinical Summary Section Content##
The Clinical summary section carries a narrative summary of the episode. Where possible, very brief,items in bold are subheadings and should be formatted as such in any html sent:
**Clincal summary**
This may include interpretation of findings and results; differential diagnoses, opinion and specific action(s). Planned actions will be recorded under ‘plan’.

##  Example Clinical Summary Section ##

<script src="https://gist.github.com/IOPS-DEV/77620f7d132b195c42b5f2fee5f39172.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK FHIR eDischarge does not currently support a coded clinical summary.






