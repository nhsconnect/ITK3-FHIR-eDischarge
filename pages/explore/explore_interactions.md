---
title: Messaging Interactions
keywords:  messaging, interactions
tags: [fhir,messaging,interactions]
sidebar: foundations_sidebar
permalink: explore_interactions.html
summary: "ITK eDischarge Interactions"
---

{% include custom/search.warnbanner.html %}

{% include custom/messaging_overview.svg %}

## ITK eDischarge Interactions Overview ##
This section provides ITK eDischarge implementers with the information required to utilise the ITK eDischarge Interactions.

**Note 1:** When using MESH, additional MESH acknowledgements and responses will be available.  The MESH acknowledgements and responses are not defined in this specification

**Note 2:** Messages are structured in eXtensible Markup Language (XML) only.

The ITK eDischarge is based on the [HL7 FHIR STU3 Messaging Implementation](http://hl7.org/fhir/messaging.html) and supports multiple interactions. 

---------
## DOC-ToC-Primary-Recipient-eDischarge-1 Interaction ##

The sending hospital system will construct an eDischarge (inpatient discharge summary) FHIR Document and send it to the primary recipient's receiving system.

- Sender: Hospital sending system
- Receiver: eDischarge Recipient system
- Message: Wire Format: TOC-eDischarge-1

## DOC-ToC-Copy-Recipient-eDischarge-1 Interaction ##

The sending hospital system will construct an eDischarge (inpatient discharge summary) FHIR Document and send it to the copy recipient's receiving system. 

- Sender: Hospital sending system
- Receiver: eDischarge Recipient system
- Message: Wire Format: TOC-eDischarge-1

## Acknowledgements Interactions ##

Dependent on system set up the following interactions may be utilised.


- <a href="https://nhsconnect.github.io/ITK3-FHIR-Messaging-Distribution/explore_interactions.html#rsp-itk-infrastructure-acknowledgement-response-1-interaction" target="_blank">RSP-ITK-Infrastructure-Acknowledgement-Response-1</a>
- <a href="https://nhsconnect.github.io/ITK3-FHIR-Messaging-Distribution/explore_interactions.html#rsp-itk-business-acknowledgement-response-1-interactions" target="_blank">RSP-ITK-Business-Acknowledgement-Response-1</a>

## eDischarge (inpatient discharge summary) ITK FHIR Document Interactions Diagram  ##

The diagram shows the eDischarge (inpatient discharge summary) Document Interactions: Note: The use of the ITK infrastructure interactions are dependant on system configuration.  


<img src="images/explore/ITK-eDischarge-FHIRInteractions.png" style="width:75%;max-width: 75%;">












