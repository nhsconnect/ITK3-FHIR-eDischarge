---
title: Discharge Details Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_discharge_details.html
summary: "Gives information about the Discharge details section"
---

{% include custom/section.warnbanner.html %}

## Discharge Details Section Content##
The Discharge details section carries details of the patient's discharge, items in bold are subheadings and should be formatted as such in any html sent:


- **Discharging consultant** - The consultant responsible for the patient at time of discharge.
- **Discharging specialty/department** - The specialty/department responsible for the patient at the time of discharge.
- **Expected date of discharge** -  The date the patient is currently expected to be discharged from hospital.
- **Date of discharge** - Time of discharge Electronic environment only.
- **Discharge method** - The method of discharge from hospital. National codes:
eg, patient discharged on clinical advice or with clinical consent; patient discharged
him/herself or was discharged by a relative or advocate, patient died, stillbirth.
- **Discharge destination** -  The destination of the patient on discharge from hospital. National codes.
Eg NHS-run care home.
- **Discharge address Address** - to which patient discharged. Only completed where this is not the usual
place of residence.

##  Example Discharge Section ##

<script src="https://gist.github.com/IOPS-DEV/8af6e4182fad6c0ce91e46e6d17563b5.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- [Encounter](workflow_encounter.html)






