---
title: Admission Details Section
keywords:  messaging, sections
tags: [fhir,messaging,sections]
sidebar: foundations_sidebar
permalink: explore_admission_details.html
summary: "Gives information about the Admission details section"
---

{% include custom/section.warnbanner.html %}

## Admission Details Section Content##
The Admission details section carries information about the patient's admission, items in bold are subheadings and should be formatted as such in any html sent:

- **Admission method** How the patient was admitted to hospital. Eg: elective,
emergency, maternity, transfer, etc.
- **Source of admission** Where the patient was immediately prior to admission, eg, usual place of residence, temporary place of residence, penal establishment. National code.
- **Patient location** This is the physical location of the patient. For inpatient, eg, hospital ward, bed, theatre. For ambulatory care, eg, health centre, clinic, resource centre, patient’s home.
- **Date of admission** Date patient admitted to hospital.
- **Time of admission** Time patient admitted to hospital.

##  Example Admission Details Section ##

<script src="https://gist.github.com/IOPS-DEV/063615bfb87522015e0c37ef7f06d4fd.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- [Encounter](workflow_encounter.html)






