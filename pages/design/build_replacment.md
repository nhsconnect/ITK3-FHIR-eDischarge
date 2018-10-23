---
title: Document Replacement
keywords: design, build
tags: [design]
sidebar: foundations_sidebar
permalink: build_replacement.html
summary: "Replacement Semantics for Transfer of Care Documents"
---

## Background ##

The Transfer of Care documents allow for replacement of a previously sent document. This replacement is at a whole document level in that, the original document is replaced by a new one and the old document is only kept for audit purposes. 
A sender may choose to send a new replacement document for a number of reasons, for example:

- The original document contained an error - identified after the document sent
- The sender has more up to date  or complete information - the original is correct but further information is now available to make the document more complete or detailed 

Receivers of replacement documents **MUST** process the replacement document and archive the replaced document.

When the new document cannot be processed then:

- The receiver of the new document **SHOULD** mark the original and replacement document as null and void and report a error to the sender using the ITK Response message and appropriate code see [ITK3 response codes](https://developer.nhs.uk/apis/itk3messagedistribution/explore_response_codes.html) for further information. 
- The sender of the new document **SHOULD** mark the original and replacement document as null and void once it receives the ITK3 Response indicating that the replacement document could not be processed.


## FHIR Elements Used for Replacement ##

- Composition.identifier@value on old document - UUID of original document
- Composition.identifier@value on new document - UUID of new document
- Composition.relatesTo.code@value fixed value of "replaces"
- Composition.relatesTo.targetIdentifier@value = UUID of original document


## Example of Use of relatesTo Element ##

<img src="images/build/ReplacementDiagram.png" style="width: 75%;max-width: 100%;"> 






