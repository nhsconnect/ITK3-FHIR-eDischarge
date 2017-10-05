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

- **[ITK-Document-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-Document-Bundle-1)** - An NHS Digital Bundle Profile to represent a container to collect a combination of the ITK FHIR Document resources.
- **[ITK-EDIS-Composition-1](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-EDIS-Composition-1)** - An NHS Digital Profile for eDischarge FHIR Documents. 
- **[CareConnect-ITK-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Encounter-1)** - A CareConnect derived NHS Digital Profile for encounter. The encounter resource represents an encounter between a care professional and the patient (or patient's record).
- **[ITK-Medication-List-1](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-Medication-List-1)** - An NHS Digital Profile for recording a snapshot of the list of Medications for the patient.
- **[CareConnect-MedicationStatement-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-MedicationStatement-1)** - A CareConnect Profile for medication statements. The MedicationStatement Resource is a record of a medication that is being consumed by a patient.
- **[CareConnect-Medication-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Medication-1)** - A CareConnect Profile for medication. The Medication Resource is primarily used for the identification and definition of a medication.
- **[CareConnect-ITK-Medication-Flag-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Medication-Flag-1)** - An NHS Digital Profile for medication flags. The Flag Resource carries prospective warnings of potential issues related to the patient's medications.
- **[ITK-Allergies-List-1](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-Allergies-List-1)** - An NHS Digital profile for recording a snapshot of the list of Allergies for the patient.
- **[CareConnect-AllergyIntolerance-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-AllergyIntolerance-1)** - A careConnect Profile for Allergies and adverse reactions. The AllergyIntolerance Resource records Risk of harmful or undesirable, physiological response which is unique to an individual and associated with exposure to a substance.
- **[ITK-Allergy-Flag-1](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-Allergy-Flag-1)** - An NHS Digital profile used to record prospective warnings of potential issues related to the patient's allergies.
- **[CareConnect-ITK-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Condition-1)** -	A CareConnect derived NHS Digital Profile for conditions. The Condition resource records detailed information about conditions or diagnoses recognised by a clinician.
- **[CareConnect-ITK-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Procedure)** - A CareConnect derived NHS Digital Profile for procedures. The Procedure resource is used to record an action that is or was performed on a patient.
- **[CareConnect-ITK-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Observation-1 )** - A CareConnect dervived NHS Digital Profile for observation. The Observation resource is used for tracking the current and historical observations that have been made for a patient.
- **[CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)** - A CareConnect Profile for patient. The Patient resource represents the patient involved in the provision of healthcare related services.
- **[CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)** - A CareConnect Profile for a practitioner. The Practitioner resource represents the healthcare professional directly or indirectly involved in the provision of healthcare related services.
- **[CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)** - A CareConnect Profile for a practitioner role.The PractitionerRole resource represents a specific set of Roles/Locations/specialties/services that a practitioner may perform at an organization for a period of time.
- **[ITK-RelatedPerson-1](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-RelatedPerson-1)** - An NHS Digital profile which carries information for a person with a relationship with the patient.
- **[CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)** - 	A CareConnect Profile for Organization. The Organization resource represents the organisation that employs the healthcare professional.
- **[CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)** - A CareConnect Profile for Location. The Location resource provides information and details on the physical location and the services provided.
- **[ITK-Device-1](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-Device-1)** - An NHS Digital profile which identifies an instance of a manufactured item that is used in the provision of healthcare without being substantially changed through that activity. The device may be a medical or non-medical device.

## Profile Extensions ##

- **[Extension-ITK-Authorization-1](https://fhir.nhs.uk/STU3/StructureDefinition/Extension-ITK-Authorization-1)** - An NHS Digital extension to Composition resource to allow the details of the person who authorised the document.
- **[Extension-ITK-CareSettingType-1](https://fhir.nhs.uk/STU3/StructureDefinition/Extension-ITK-CareSettingType-1)** - An NHS Digital extension to Composition resource to allow the details care setting type that the document was sent from.
- **[Extension-ITK-DataEnterer-1](https://fhir.nhs.uk/STU3/StructureDefinition/Extension-ITK-DataEnterer-1)** An NHS Digital extension to Composition resource to allow the details of a person who entered the information contained in the document.
- **[Extension-ITK-Informant-1](https://fhir.nhs.uk/STU3/StructureDefinition/Extension-ITK-Informant-1)** - An NHS Digital extension to Composition resource to allow the details of the person who informed the author about information contained in the document.
- **[Extension-ITK-InformationRecipient-1](https://fhir.nhs.uk/STU3/StructureDefinition/Extension-ITK-InformationRecipient-1)** - An NHS Digital extension to Composition resource to allow the details of the person or organization who/which is a recipient of the document.
- **[Extension-ITK-Participant-1](https://fhir.nhs.uk/STU3/StructureDefinition/Extension-ITK-Participant-1)** - An NHS Digital extension to Composition resource to allow the details of the person who participated in the document where this is not explicitly modelled.
- **[Extension-ITK-Performer-1](https://fhir.nhs.uk/STU3/StructureDefinition/Extension-ITK-Performer-1)** - An NHS Digital extension to Composition resource to allow the details of the person who performed items within the document.
- **[Extension-CareConnect-NHSCommunication-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-NHSCommunication-1)** - A CareConnect extension to Patient and Practitioner resources to carry language information suitable for NHS use.
- **[Extension-CareConnect-MainLocation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-MainLocation-1)** - A CareConnect extension to the Location resource to allow the main location to be carried/indicated.
- **[organization-period](http://hl7.org/fhir/StructureDefinition/organization-period)** - An HL7 common extension to the Organization resource allow the periods of time to be associated with the organization.
- **[Extension-CareConnect-EncounterTransport-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-EncounterTransport-1)** - A CareConnect extension to the Encounter resource to allow transportation information to be carried. 
- **[Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid)** -  A CareConnect extension used in resources that use SNOMED CT to allow the SNOMED description identifier to be carried.
- **[Extension-CareConnect-MedicationStatementReasonEnded-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-MedicationStatementReasonEnded-1)** - A CareConnect extension to the MedicationStatement resource allow information about why the medication was ended to be carried.
- **[Extension-CareConnect-MedicationStatementQuantity-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-MedicationStatementQuantity-1)** - A CareConnect extension to the MedicationStatement resource to allow indication of the amount of medication to supply per dispense.
- **[Extension-CareConnect-MedicationStatementLastIssueDate-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-MedicationStatementLastIssueDate-1)** - A CareConnect extension to the MedicationStatement resource to allow the last issue date of the medication to be carried.
- **[Extension-CareConnect-MedicationRepeatInformation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-MedicationRepeatInformation-1)** - A CareConnect extension to the MedicationStatement resource to allow the specific repeat information of a medication item.
- **[Extension-CareConnect-MedicationFlag-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-MedicationFlag-1)** - A CareConnect extension to the MedicationStatement resource to specify the flags related to the patient's medications.
- **[Extension-CareConnect-RegistrationDetails-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-RegistrationDetails-1)** - A CareConnect extension to the Patient resource to carry the additional registration information for a patient.
- **[Extension-CareConnect-EthnicCategory-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-EthnicCategory-1)** - A CareConnect extension to the Patient resource to carry the ethnic category for a patient.
- **[Extension-CareConnect-ReligiousAffiliation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ReligiousAffiliation-1)** - A CareConnect extension to the Patient resource to carry the religious affiliation for a patient.
- **[Extension-CareConnect-ResidentialStatus-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ResidentialStatus-1)** - A CareConnect extension to the Patient resource to carry the residential status for a patient.
- **[Extension-CareConnect-TreatmentCategory-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-TreatmentCategory-1)** - A CareConnect extension to the Patient resource to carry the treatment category for a patient.
- **[Extension-CareConnect-NHSNumberVerificationStatus-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-NHSNumberVerificationStatus-1)** - A CareConnect extension to the Patient resource to carry the verification status of the patient NHS number.
- **[patient-cadavericDonor](http://hl7.org/fhir/StructureDefinition/patient-cadavericDonor)** - A HL7 common extension to the Patient resource which uses a Flag indicating whether the patient authorized the donation of body parts after death. 
- **[patient-birthTime](http://hl7.org/fhir/StructureDefinition/patient-birthTime)** - A HL7 common extension to the patient resource which allows the time of day that the Patient was born. This includes the date to ensure that the timezone information can be communicated effectively.
- **[Extension-CareConnect-ConditionEpisode-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ConditionEpisode-1)** - A CareConnect extension to the Condition resource for the episodicity status of a condition. 
- **[Extension-CareConnect-ConditionRelationship-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ConditionRelationship-1)** -  A CareConnect extension to the Condition resource for a reference to another related condition (target) whose relationship is defined by the relationship type code.
- **[Extension-CareConnect-ReasonCondition-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ReasonCondition-1)** -  A CareConnect extension to the Procedure resource for the reason why a procedure was added/performed/given. This may be due to a Condition, may be coded entity of some type, or may simply be present as text. 
- **[Extension-CareConnect-DateRecorded-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-DateRecorded-1)** - A CareConnect extension to the Procedure resource for the date that the Procedure was recorded.
- **[Extension-ITK-MedicationFlagAssociation-1](https://fhir.nhs.uk/STU3/StructureDefinition/Extension-ITK-MedicationFlagAssociation-1)** - An NHS Digital extension to the Flag Resource to allow a relationship to the associated Medication.  
- **[Extension-ITK-AllergyFlagAssociation-1](https://fhir.nhs.uk/STU3/StructureDefinition/Extension-ITK-AllergyFlagAssociation-1)** - An NHS Digital extension to the Flag Resource to allow a relationship to the associated Allergy.   
- **[encounter-associatedEncounter](http://hl7.org/fhir/StructureDefinition/encounter-associatedEncounter)** - A CareConnect extension to the AllergyIntolerance resource to the encounter associated with the allergy.
- **[Extension-CareConnect-AllergyIntoleranceEndDate-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-AllergyIntoleranceEndDate-1)** - A CareConnect extension to the allergyIntolerance resource for the date that the allergy was no longer valid.
- **[Extension-CareConnect-Evidence-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-Evidence-1)** - A CareConnect extension to the allergyIntolerance resource to support a reference to results of investigations that confirmed the certainty of the diagnosis. Examples might include results of skin prick allergy tests.
- **[Extension-CareConnect-ProbabilityOfRecurrence-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ProbabilityOfRecurrence-1)** - A CareConnect extension to the allergyIntolerance resource to constrained to support representation of the probability of the reaction (allergic, adverse, intolerant) occurring.
- **[Extension-CareConnect-AllergyCertainty-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-AllergyCertainty-1)** - A CareConnect extension to the allergyIntolerance resource to support a coded certainty of the allergy/intolerance.
- **[Extension-CareConnect-AllergySeverity-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-AllergySeverity-1)** - A CareConnect extension to the allergyIntolerance resource

## ITK eDischarge FHIR Document Profile Referencing ##

The diagram shows the referencing between the profiles in the bundle which make up the ITK eDischarge FHIR Document.

When using ITK3 there is an outer bundle structure which is called the [ITK3 send payload bundle structure](https://nhsconnect.github.io/ITK3-FHIR-Messaging-Distribution/explore_messages.html#itk-send-payload-bundle-diagram) for use with ITK3. 

This diagram only goes to one level due to the complexity and size of the document profile.Below is the key to the diagram.

<img src="images/explore/Key.png" style="width: 75%;max-width: 75%;"> 

<img src="images/explore/eDischarge_message_bundle.png" style="width:80%;max-width: 80%;"> 

## ITK eDischarge Bundle Example ##

<script src="https://gist.github.com/IOPS-DEV/4c7978a769e995660c41c2c8479b9255.js"></script>

{% include custom/messaging_overview.svg %}


