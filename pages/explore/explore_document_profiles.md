---
title: Document Profiles 
keywords:  documents
tags: [fhir,messaging,documents]
sidebar: foundations_sidebar
permalink: explore_document_profiles.html
summary: "ITK eDischarge FHIR Document profile"
---

{% include custom/search.warnbanner.html %}


## ITK eDischarge FHIR Document Bundle ##

FHIR resource profiles combined to support eDischarge (inpatient discharge summary) FHIR Documents.

The Bundle consists of the following FHIR Resource Profiles.

- **ITK-Document-Bundle-1** - An NHS Digital Bundle Profile to represent a container to collect a combination of the ITK FHIR Document resources.
- **ITK-EDIS-Composition-1** - An NHS Digital Profile for eDischarge FHIR Documents. 
- **CareConnect-Encounter-1** - A CareConnect profile for encounter. The encounter resource represents an encounter between a care professional and the patient (or patient's record).
- **ITK-Medication-List-1** - An NHS Digital profile for recording a snapshot of the list of Medications for the patient.
- **CareConnect-MedicationStatement-1** - A CareConnect Profile for medication statements. The MedicationStatement Resource is a record of a medication that is being consumed by a patient.
- **CareConnect-Medication-1** - A CareConnect Profile for medication. The Medication Resource is primarily used for the identification and definition of a medication.
- **CareConnect-Medication-Flag-1** - A CareConnect Profile for medication flags. The Flag Resource carries prospective warnings of potential issues related to the patient's medications.
- **ITK-Allergies-List-1** - An NHS Digital profile for recording a snapshot of the list of Allergies for the patient.
- **CareConnect-AllergyIntolerance-1** - A careConnect Profile for Allergies and adverse reactions. The AllergyIntolerance Resource records Risk of harmful or undesirable, physiological response which is unique to an individual and associated with exposure to a substance.
- **ITK-Allergy-Flag-1** - An NHS Digital profile used to record prospective warnings of potential issues related to the patient's allergies.
- **CareConnect-Condition-1** -	A Connect Profile for conditions. The Condition resource records detailed information about conditions or diagnoses recognised by a clinician.
- **CareConnect-Procedure-1** - A careConnect Profile for procedures. The Procedure resource is used to record an action that is or was performed on a patient.
- **CareConnect-Observation-1** - The Observation resource is used for tracking the current and historical observations that have been made for a patient.
- **CareConnect-Patient-1** - A CareConnect Profile for patient. The Patient resource represents the patient involved in the provision of healthcare related services.
- **CareConnect-Practitioner-1** - A CareConnect Profile for a practitioner. The Practitioner resource represents the healthcare professional directly or indirectly involved in the provision of healthcare related services.
- **ITK-RelatedPerson-1** - An NHS Digital profile which carries information for a person with a relationship with the patient.
- **CareConnect-Organization-1** - 	A CareConnect Profile for Organization. The Organization resource represents the organisation that employs the healthcare professional.
- **CareConnect-Location-1** - A CareConnect Profile for Location. The Location resource provides information and details on the physical location and the services provided.
- **ITK-Device-1** - An NHS Digital profile which identifies an instance of a manufactured item that is used in the provision of healthcare without being substantially changed through that activity. The device may be a medical or non-medical device.

## ITK eDischarge FHIR Document Profile Referencing ##

The diagram shows the referencing between the profiles in the bundle which make up the ITK eDischarge FHIR Document.

When using ITK3 there is an outer bundle structure which is called the [ITK3 send payload bundle structure](https://nhsconnect.github.io/ITK3-FHIR-Messaging-Distribution/explore_messages.html#itk-send-payload-bundle-diagram) for use with ITK3. 

<img src="images/explore/eDischarge_message_bundle.png" style="width:80%;max-width: 80%;"> 

## ITK eDischarge Bundle Example ##

<script src="https://gist.github.com/IOPS-DEV/4c7978a769e995660c41c2c8479b9255.js"></script>

{% include custom/messaging_overview.svg %}


