---
title: Social Context Section
keywords:  messaging, sections
tags: [fhir,messaging,sections]
sidebar: foundations_sidebar
permalink: explore_social_context.html
summary: "Gives information about the Social context section"
---

{% include custom/section.warnbanner.html %}

## Social Context Section Content##
The Social context section carries information about the social context of the patient,items in bold are subheadings and should be formatted as such in any html sent:

- **Household composition** - Eg: lives alone, lives with family, lives with partner, etc. This may be plain text.
- **Lives alone** - Yes/no/don’t know (Y/N/DK).
- **Occupational history** - The current and/or previous relevant occupation(s) of the patient/individual. This may include educational history.

##  Example Social Context Section ##

<script src="https://gist.github.com/IOPS-DEV/73932c1d2ee99e5fd832bcbfa1922092.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK FHIR eDischarge does not currently support coded Social context information.






