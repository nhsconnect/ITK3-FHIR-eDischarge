---
title: Document Profiles 
keywords:  documents
tags: [fhir,messaging,documents]
sidebar: foundations_sidebar
permalink: explore_document_profiles.html
summary: "ITK3 eDischarge FHIR Document profile"
---

{% include custom/search.warnbanner.html %}


## ITK3 eDischarge FHIR Document Bundle ##

FHIR resource profiles combined to support eDischarge (inpatient discharge summary) FHIR Documents.

The Bundle consists of the following FHIR Resource Profiles.

- **ITK3-Document-Bundle-1** - An NHS Digital Bundle Profile to represent a container to collect a combination of the ITK3 FHIR Document resources.
- **ITK3-EDIS-Composition-1** - An NHS Digital Profile for eDischarge FHIR Documents. 
- **CareConnect-Encounter-1** - A CareConnect profile for encounter. The encounter resource represents an encounter between a care professional and the patient (or patient's record).
- **ITK3-Medication-List-1** - An NHS Digital profile for recording a snapshot of the list of Medications for the patient.
- **CareConnect-MedicationStatement-1** - A CareConnect Profile for medication statements. The MedicationStatement Resource is a record of a medication that is being consumed by a patient.
- **CareConnect-Medication-1** - A CareConnect Profile for medication. The Medication Resource is primarily used for the identification and definition of a medication.
- **CareConnect-MedicationOrder-1** - A CareConnect Profile for medication orders. The MedicationOrder Resource represents an order for both supply of the medication and the instructions for administration of the medication to a patient.
- **CareConnect-Medication-Flag-1** - A CareConnect Profile for medication flags. The Flag Resource carries prospective warnings of potential issues related to the patient's medications.
- **ITK3-Allergies-List-1** - An NHS Digital profile for recording a snapshot of the list of Allergies for the patient.
- **CareConnect-AllergyIntolerance-1** - A careConnect Profile for Allergies and adverse reactions. The AllergyIntolerance Resource records Risk of harmful or undesirable, physiological response which is unique to an individual and associated with exposure to a substance.
- **ITK3-Allergy-Flag-1** - An NHS Digital profile used to record prospective warnings of potential issues related to the patient's allergies.
- **CareConnect-Condition-1** -	A Connect Profile for conditions. The Condition resource records detailed information about conditions or diagnoses recognised by a clinician.
- **CareConnect-Procedure-1** - A careConnect Profile for procedures. The Procedure resource is used to record an action that is or was performed on a patient.
- **CareConnect-Observation-1** - The Observation resource is used for tracking the current and historical observations that have been made for a patient.
- **CareConnect-Patient-1** - A CareConnect Profile for patient. The Patient resource represents the patient involved in the provision of healthcare related services.
- **CareConnect-Practitioner-1** - A CareConnect Profile for a practitioner. The Practitioner resource represents the healthcare professional directly or indirectly involved in the provision of healthcare related services.
- **ITK3-RelatedPerson-1** - An NHS Digital profile which carries information for a person with a relationship with the patient.
- **CareConnect-Organization-1** - 	A CareConnect Profile for Organization. The Organization resource represents the organisation that employs the healthcare professional.
- **CareConnect-Location-1** - A CareConnect Profile for Location. The Location resource provides information and details on the physical location and the services provided.
- **ITK3-Device-1** - An NHS Digital profile which identifies an instance of a manufactured item that is used in the provision of healthcare without being substantially changed through that activity. The device may be a medical or non-medical device.

## ITK3 eDischarge FHIR Document Profile Referencing ##

The diagram shows the referencing between the profiles in the bundle which make up the ITK3 eDischarge FHIR Document.


<img src="images/explore/eDischarge_message_bundles.png" style="width:60%;max-width: 80%;"> 

## ITK3 eDischarge Bundle Example ##

<script src="https://gist.github.com/unicorn150161/4cc76d52e3a93ce529efdffcaa487396.js"></script>

{% include custom/messaging_overview.svg %}





