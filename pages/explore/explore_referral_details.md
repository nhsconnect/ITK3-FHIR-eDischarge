---
title: Referral Details Section
keywords:  messaging, sections
tags: [fhir,messaging,sections]
sidebar: foundations_sidebar
permalink: explore_referral_details.html
summary: "Gives information about the Referral details section"
---

{% include custom/section.warnbanner.html %}

## Referral Details Section Content##
The Referral details section carries a narrative summary of the episode. Where possible, very brief,items in bold are subheadings and should be formatted as such in any html sent:

- **Referrer details** - Name, designation, organisation and contact details of referrer. If not an individual, this could be, eg, GP surgery, department, specialty, subspecialty, educational institution, mental health etc. Also needs to include self-referral.

##  Example Referral Details Section ##

<script src="https://gist.github.com/IOPS-DEV/324006a867ea11a33997dcb6148b289a.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK FHIR eDischarge does not currently support a coded Referral details.






