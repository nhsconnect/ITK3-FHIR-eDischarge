---
title: GP Practice Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_gp_practice.html
summary: "Gives information about the patient's GP Practice"
---
{% include custom/non_text_section.warnbanner.html %}


## GP Practice Section Content##

The GP Practice section is rendered from the careProvider reference in the patient resource. The resources used are: 

- **[CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)** - A CareConnect Profile for a practitioner. The Practitioner resource represents the healthcare professional directly or indirectly involved in the provision of healthcare related services.
- **[CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)** - A CareConnect Profile for a practitioner role.The PractitionerRole resource represents a specific set of Roles/Locations/specialties/services that a practitioner may perform at an organization for a period of time.
- **[CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)** - 	A CareConnect Profile for Organization. The Organization resource represents the organisation that employs the healthcare professional.

The GP Practice section must be rendered in a similar format to other sections. The following is a suggested format for rendering. Items in bold are suggested subheadings and should be formatted as such when rendered:
 
<ul>
<li><b>GP name</b></li>
<li><b>GP practice details</b></li>
<li><b>GP practice identifier</b></li>
</ul>

The PractitionerRole resource is included to allow identification of the practitioner in the role of GP. 

## Example GP Practice Using Organization Resource ##

<script src="https://gist.github.com/IOPS-DEV/96ebbfe2e8f8f58ca820c7fb0a278bd5.js"></script>

## Example GP Name Using Practitioner Resource ##

Note: The GP is linked to the GP Practice by the Practitioner resource referencing the organization resource using the managingOrganization element. The PractitionerRole resource identifies the practitioner in the role of GP.

<script src="https://gist.github.com/IOPS-DEV/3f5d3d112a125a0d28f449964e0a26c5.js"></script>




