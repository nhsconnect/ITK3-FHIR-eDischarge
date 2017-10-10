---
title: Introduction to ITK eDischarge
keywords: homepage
tags: [overview]
sidebar: overview_sidebar
permalink: index.html
toc: false
summary: A brief introduction to getting started with the ITK eDischarge.
---

{% include important.html content="This site is under active development by NHS Digital and is intended to provide all the technical resources you need to successfully develop the ITK eDischarge components of FHIR messaging. This project is being developed using an agile methodology so iterative updates to content will be added on a regular basis." %}

{% include warning.html content="This site is provided for information only and is intended for those engaged with NHS Digital in the development of FHIR Messaging. It is advised not to develop against these specifications until a formal announcement has been made." %}

{% include warning.html content="The examples provided are for illustrative purposes only. They have had no clinical validation. Whilst every effort has been taken to ensure that the examples are consistent with the FHIR profiles and this specification , where there are conflicts the written message specification or FHIR profile shall be considered to take precedence." %}

## Introduction ##

The Transfer Of Care eDischarge  Specification supports the following care communications:

**eDischarge (inpatient discharge summary) Document** – An ITK FHIR Document containing Transfer of Care information supporting an inpatient discharge typically between an acute hospital and GP practice.
   
FHIR Messaging components specified within this site have been developed by NHS Digital and use some of the CareConnect profiles created in collaboration with the INTEROPen community. 

The INTEROPen vision is to create a library of nationally defined HL7® FHIR® resources and interaction patterns that implementers can adopt to simplify integration and interoperability within UK health and social care.

Find out more on the [INTEROPen website](http://interopen.org/).

This documentation provides a FHIR document implmentation of the work done by the Academy of Medical Royal Colleges (AoMRC) in defining headings for clinical documents.
 
{% include custom/section.warnbanner.html %}

# Using this guide #

This guide has been created to support the adoption of NHS Digital defined FHIR Messages. As such the site is structured around stakeholders involved in building FHIR ITK Messaging Solutions including  ITK Messaging Solution users, developers and architects.  

{% include custom/messaging_overview.svg %}

The above steps outline a complete journey from imagination and exploring to developing local ITK Messaging Solutions using NHS Digital Messages, all the way to deploying a live ITK Messaging Solution.

# ITK FHIR eDischarge Focus #

The current site focuses on a typical FHIR ITK Messaging Solution Developer's Journey as highlighted by the green boxes below in the developer journey:

<img src="images/roadmap/guide-focus.png" style="width:100%;max-width: 100%;">


# Resource Roadmap #

The [ITK eDischarge journey](overview_message_journey.html) outlines the development roadmap for FHIR Messaging using the ITK eDischarge outlined messaging within this site. Note: This roadmap would include components from other NHS Digital specifications for example ITK eDischarge message components, CareConnect profiles etc.

<img src="images/roadmap/messaging_roadmap-online.png" style="width:100%;max-width: 100%;">

The above roadmap illustrates the steps necessary to create, test and verify the messaging components as well as some of the supporting tooling which might be necessary to build to provide viable ITK Messaging Solutions. The roadmap is not intended to be complete but to promote discussion, extension and engagement from interested parties.

