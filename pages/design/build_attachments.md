---
title: Use of Attachments
keywords: design, build
tags: [design]
sidebar: foundations_sidebar
permalink: build_attachments.html
summary: "Use of Attachments in Transfer of Care Documents"
---

{% include important.html content="All information provided below is indicative and subject to on-going review." %}

## Background ##

The Transfer of Care documents allow for attachments to be included within a structured FHIR document.

## Use Cases ##

Senders <b>MAY</b> include attachments within the Transfer of Care documents. For example to include copies of related documents such as patient Advance Statements. 

## Format of Attachments ##

Sender <b>SHOULD</b> send attachments as a PDF, but <b>MAY</b> use other formats by local agreement.

## Receivers of Attachments ##

Receivers <b>SHOULD</b> process attachments in-line with the rules stated in the <a href="https://nhsconnect.github.io/ITK3-FHIR-Messaging-Distribution/explore_s_and_r.html">ITK3 Messaging Distribution Specification</a>. 

## Binary Resource ##

All attachments are carried in the FHIR Binary Resource. This is profiled as <a href="https://fhir.nhs.uk/STU3/StructureDefinition/ITK-Attachment-Binary-1">ITK-Attachment-Binary-1</a> and <b>MUST</b> be Base64 encoded. 

## Example Attachment ##

 





