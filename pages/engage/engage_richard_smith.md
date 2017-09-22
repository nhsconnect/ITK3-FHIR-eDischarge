---
title: Richard Smith Discharge Summary Scenario
keywords: workflow
tags: [development,fhir,profiles]
sidebar: overview_sidebar
permalink: engage_richard_smith.html
summary: "Example scenario - Richard Smith Discharge Summary"
---

{% include custom/search.warnbanner.html %}

## Background ##

Richard Smith aged 60, is at home and has been feeling unwell with chest pain. His wife speaks to Peter, a neighbour, who offers to take them to the local A & E department. On arrival at A & E Richard, with the aid of his wife checks in with the receptionist. The receptionist asks for his name, address and Date of Birth and does a PDS look-up to get his details. She confirms these are correct and checks Richard in on the A & E system. She then asks him to take a seat in the waiting area.

After a short wait, Richard starts to feel worse and his wife goes to speak to the receptionist, who asks a passing nurse to speak to Richard. Richard's wife explains that she is concerned about the possibility of Richard suffering from a heart attack,as his symptoms are similar to Richard's mother when she had a heart attack. The nurse feels that Richard needs to be seen urgently and asks him and his wife to follow her to the examination cubicle. After taking Richard's vital signs, the nurse explains that she will go and get a doctor to examine Richard, leaves the cubicle and returns with Doctor Amanda Smith. She also takes Richard's vital signs and does an ECG that shows inferior ischaemic changes. She explains that they are going to admit Richard onto a ward for further tests.

## The Inpatient Stay ##

The Inpatient stay is carried in the [Encounter Resource](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-ITK-Encounter-1)

**Named Participants**

- Patient - **Richard Smith** - [Patient Resource](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)
- Patient's wife - **Joy Smith** - [RelatedPerson Resource](https://fhir.nhs.uk/STU3/StructureDefinition/ITK-RelatedPerson-1)
- Consultant - **Mr Abacus** - [Practitioner Resource](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- Discharging clinician (Document Author) - **Dr Paul Rastall** - [Practitioner Resource](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- Patient's GP (Document recipient) - **Dr John Lorenzo** - [Practitioner Resource](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- Community Nurse (Document recipient) - **Mrs Angela Jones** - [Practitioner Resource](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)

**Named Organisations**

- Patient's GP Practice - **MGP Medical Centre** - [Organization Resource](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- Discharging Hospital - **Leeds Teaching Hospitals NHS Trust** - [Practitioner Resource](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)

Richard is admitted to the ward on the 12th Feb where, during triage, the nurse asks if he has any allergies and what medication he is on. Richard's wife has brought his medication with her so is able to show the nurse the medication. Richard tells the nurse he has an allergy to Penicillin which causes a rash. The nurse asks if he gets any swelling, to which Richard replies "no". Richard's Summary Care Record confirms what he told the nurse. Richard is given a TIMI assessment and a full blood test.

During the course of his stay in hospital Richard is given another ECG. The coronary angiogram indicates a diseased RCA. Following consultation with Mr Abacus, the heart specialist, Richard consents to having an angioplasty procedure to place a drug eluting stent. The is done the next day and the procedure is successful.

When Richard's wife visits him on the 15th he tells her that the consultant Mr Abacus says he can go home the following day once he has spoken to someone from the Cardiac Rehabilitation Team. The following day Richard has a Cardiac Rehabilitation consultation with Dr Paul Rastall during which he is given information regarding the diagnosis and possible life style changes when he is discharged. Richard is concerned about whether he can drive and asks about this as he is a self employed electrician. Dr Paul Rastall advises him that he should not to drive for at least a week, but reassures him that he should be able to drive once recovered and says he will arrange for a community follow-up.

In the afternoon Dr Paul Rastall discharges Richard and completes and sends an eDischarge to Richard's GP and the community nurse at the practice where Richard is registered.

Richard's wife arrives with their neighbour Peter, who has kindly agreed to pick him up from the hospital and take him home.

