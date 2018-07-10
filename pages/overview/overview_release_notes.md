---
title: Release Notes
keywords: development, versioning
tags: [development]
sidebar: overview_sidebar
permalink: overview_release_notes.html
summary: Summary release notes of the versions released in ITK3 eDischarge Implementation Guide
---


## 2.4.0-beta ##

**Profiles**

- New CareConnect-ITK-MedicationResponse-1 Profile added to support TTOs (To take outs)
- Updated CareConnect-ITK-MedicationStatement-1 to support reference to CareConnect-ITK-MedicationResponse-1.

**Specification Pages**

- Updated Profile page to include the new Profile
- Updated Message Definitions
- Added new MedicationDispense referencing diagram
- Updated MedicationStatement referencing diagram to include MedicationDispense Resource
- Update "Build medication list" pages 

## 2.3.0-beta ##

**PRSB section tables** 

These have been updated to include mappings of the PRSB elements to the FHIR elements (where there are mappings). 

**Examples**

Examples have been updated and corrected following further validation.

All Coded entries are now done as lists. Medication is now two lists one for "Active" and one for "Discontinued". 

**Constructing clinical coded structures section**

Updated with new guidance derived from INTEROPen curation.

## 2.2.0-alpha ##

**Profiles**

All profiles have been updated to align with CareConnect profiles following INTEROPen curation.

**Examples**
All examples have been updated to align with CareConnect profiles following INTEROPen curation.

**Section**

The section Design & Build/Constructing Clinical Coded Structures has been updated to reflect the change to the approach following 
INTEROPen curation process.

## 2.1.0-alpha ##

**Infrastructure Changes**

Changed to align with the ITK3 Messaging Distribution specification version 2.1.0-beta.  

**Messaging Architecture Changes**

Interactions have been replaced by message definitions and new ITK3 Handling keys.

**Value sets / Code Systems**

The url for ValueSet-CareSettingType-1, has changed to <https://fhir.nhs.uk/STU3/ValueSet/CareSettingType-1> so that it can be used across programs, also the internal version has changed to 1.0.0.

**Composition Sections**

The structure used for the Patient demographics , GP practice and Distribution list sections has been changed to have specific slices in the composition to align with all other PRSB sections. Descriptions and examples have been updated to suit.

**Section Guidance**

All PRSB headings and subheadings have been updated following release of the version 1.0 Final PRSB documentation. Descriptions and examples have been updated to suit. 

**New Profiles**

Added Binary Resource Profile to allow support for attachments.

**Specification Structure**

Added new sub menus under Design and build section for "Use of Attachments" and "Rendering of Documents" these are place-holders for guidance to be issued in a later release.

## 2.0.0-alpha.1 ##
First version published using Jekyll

