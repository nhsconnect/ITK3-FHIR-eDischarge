---
title: Document Profiles 
keywords:  documents
tags: [fhir,messaging,documents]
sidebar: foundations_sidebar
permalink: explore_document_profiles.html
summary: "ITK3 eDischarge FHIR Document profile"
---




## ITK3 eDischarge FHIR Document Bundle ##

The document bundle is a collection of FHIR Resource Profiles combined to support eDischarge (inpatient discharge summary) FHIR Documents.

The Bundle consists of the following FHIR Resource Profiles.

- **[ITK-Document-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-Document-Bundle-1)** - An NHS Digital Bundle Profile to represent a container to collect a combination of the ITK3 FHIR Document resources.
- **[CareConnect-ITK-EDIS-Composition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-EDIS-Composition-1)** - An NHS Digital Profile derived from the CareConnect Profile for eDischarge FHIR Documents. This Profile is aligned to the PRSB standard for headings and subheadings for clinical documents.
- **[CareConnect-ITK-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Encounter-1)** - A NHS Digital Profile derived from the CareConnect Encounter profile. The Encounter Resource represents an Encounter between a care professional and the patient (or patient's record).
- **[CareConnect-ITK-Medication-List-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Medication-List-1)** - An NHS Digital Profile derived from the CareConnect List Profile for recording a snapshot of the list of Medications for the patient.
- **[CareConnect-ITK-MedicationStatement-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-MedicationStatement-1)** - An NHS Digital Profile derived from the CareConnect MedicationStatement profile. The MedicationStatement Resource is a record of a medication that is being consumed by a patient.
- **[CareConnect-ITK-Medication-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Medication-1)** - An NHS Digital Profile derived from the CareConnect Medication profile. The Medication Resource is primarily used for the identification and definition of a medication. 
- **[CareConnect-ITK-MedicationDispense-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-MedicationDispense-1)** - An NHS Digital Profile derived from the CareConnect MedicationDispense Profile. Indicates that a medication product is to be or has been dispensed for a named person/patient. This includes a description of the medication product (supply) provided and the instructions for administering the medication. 
- **[CareConnect-ITK-Allergy-List-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Allergy-List-1)** - An NHS Digital Profile derived from the CareConnect List Profile for recording a snapshot of the list of Allergies for the patient.
- **[CareConnect-ITK-AllergyIntolerance-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-AllergyIntolerance-1)** - An NHS Digital Profile derived from the CareConnect AllergyIntolerance Profile. The AllergyIntolerance Resource records Risk of harmful or undesirable, physiological response which is unique to an individual and associated with exposure to a substance.
- **[CareConnect-ITK-Condition-List-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Condition-List-1)** - An NHS Digital Profile derived from the CareConnect List Profile for recording a snapshot of the list of Conditions for the patient.
- **[CareConnect-ITK-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Condition-1)** -	An NHS Digital Profile derived from the CareConnect List Profile for conditions. The Condition Resource records detailed information about conditions or diagnoses recognised by a clinician.
- **[CareConnect-ITK-Procedure-List-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Procedure-List-1)** - An NHS Digital Profile derived from the CareConnect List Profile for recording a snapshot of the list of procedures for that the patient has had.
- **[CareConnect-ITK-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Procedure-1)** - An NHS Digital Profile derived from the CareConnect procedure profile. The Procedure Resource is used to record an action that is or was performed on a patient.
- **[CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)** - A CareConnect Profile for patient. The Patient Resource represents the patient involved in the provision of healthcare related services.
- **[CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)** - A CareConnect Profile for a practitioner. The Practitioner Resource represents the healthcare professional directly or indirectly involved in the provision of healthcare related services.
- **[CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)** - A CareConnect Profile for a practitioner role.The PractitionerRole Resource represents a specific set of Roles/Locations/specialties/services that a practitioner may perform at an organization for a period of time.
- **[ITK-RelatedPerson-1](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-RelatedPerson-1)** - An NHS Digital Profile which carries information for a person with a relationship with the patient.
- **[CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)** - 	A CareConnect Profile for Organization. The Organization Resource represents the organisation that employs the healthcare professional.
- **[CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)** - A CareConnect Profile for Location. The Location Resource provides information and details on the physical location and the services provided.
- **[ITK-Device-1](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-Device-1)** - An NHS Digital Profile which identifies an instance of a manufactured item that is used in the provision of healthcare without being substantially changed through that activity. The device may be a medical or non-medical device.
- **[ITK-Attachment-Binary-1](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-Attachment-Binary-1)** - An NHS Digital Profile which may be used to carry attachments to be included in the document **See Note 1 below.** 

**Note 1**: This attachment Profile must not be used to send an unstructured Transfer of Care document, its purpose is to allow an attachment to be included within a structured Transfer of Care document.

For a complete definition of the eDischarge document see the section on [message definitions.](explore_defs_overview.html)

## ITK3 eDischarge FHIR Document Profile Referencing ##

The diagram shows the referencing between the profiles in the bundle which make up the ITK3 eDischarge FHIR Document.

When using ITK3 there is an outer bundle structure which is called the <a href="https://developer.nhs.uk/apis/itk3messagedistribution-2-9-0/explore_bundle_type.html" target="_blank">ITK3 Send Payload Bundle Structure</a>. for use with ITK3. 

This diagram only goes to one level due to the complexity and size of the document Profile. Below is the key to the diagram.

<img src="images/explore/Key.png" style="width: 75%;max-width: 75%;"> 

<img src="images/explore/eDischarge_message_bundle.png" style="width:80%;max-width: 80%;"> 

## ITK3 eDischarge Bundle Example ##

<script src="https://gist.github.com/IOPS-DEV/4c7978a769e995660c41c2c8479b9255.js"></script>




