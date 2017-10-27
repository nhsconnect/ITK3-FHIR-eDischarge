---
title: Distribution List Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_distribution_list.html
summary: "A list of recipients of the document"
---
{% include custom/non_text_section.warnbanner.html %}


## Distribution List Section Content ##
The Distribution list section is rendered from the Information Recipient Extension which references a number of resources for document recipients. The resources used are:

- **[CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)** - A CareConnect Profile for a practitioner. The Practitioner resource represents the healthcare professional directly or indirectly involved in the provision of healthcare related services.
- **[CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)** - 	A CareConnect Profile for Organization. The Organization resource represents the organisation that employs the healthcare professional.
- **[ITK-RelatedPerson-1](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-RelatedPerson-1)** - An NHS Digital profile which carries information for a person with a relationship with the patient.
- **[CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)** - A CareConnect Profile for patient. The Patient resource represents the patient involved in the provision of healthcare related services.

This is a standard extension for all ITK FHIR documents and therefore not all recipient types may be applicable to all document types. However receiving systems should be capable of rendering information from all the above resource types.

The Recipient list section must be rendered in a similar format to other sections. The following is a suggested format for rendering. Items in bold are suggested subheadings and should be formatted as such when rendered: 

- **Recipient name** 
- **Job role**
- **Phone**
- **Email**

## Example Distribution List Entry Using Organization Resource ##

This example shows a recipient organization entry.

<script src="https://gist.github.com/IOPS-DEV/f5c1fab997a9d0ef2a586e73728ac2a7.js"></script>


## Example Distribution List Entry Using Practitioner Resource ##

This example shows a recipient practitioner entry.

<script src="https://gist.github.com/IOPS-DEV/dd3378a4b7b62deaa48117449efbd7b8.js"></script>


## Example Distribution List Entry Using Patient Resource ##

This example shows a recipient patient entry.

<script src="https://gist.github.com/IOPS-DEV/af79cf398178936f11f5eb5c5d45c13c.js"></script>

## Example Distribution List Entry Using RelatedPerson Resource ##

This example shows a recipient related person (such as a carer) entry.

<script src="https://gist.github.com/IOPS-DEV/0b8035163391ff6a5de011412c079338.js"></script>

## Example Rendered Distribution List ##

This example shows a Distribution list section when rendered using the NHS Digital exemplar renderer.


**Distribution list**
		
<table width="100%">
<tr>
<th>Recipient name</th>
<th>Job role</th>
<th>Phone</th>
<tr>
<tr>
<td>Morris, Angela (Mrs)</td>
<td>Physiotherapist</td>
<td>01136323200</td>
<tr>
<tr>
<th>Recipient name</th>
<th>Relationship</th>
<th>Phone</th>
<tr>
<tr>
<td>Smith, Sarah</td>
<td>Wife</td>
<td>071234567811</td>
<tr>		
<tr>
<th>Recipient name</th>
<th>Type</th>
<th>Phone</th>
<tr>
<tr>
<td>Whitehouse Practice</td>
<td>GP Practice</td>
<td>071234567811</td>
<tr>
			


		
