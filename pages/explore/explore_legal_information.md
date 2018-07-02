---
title: Legal Information Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_legal_info.html
summary: "Gives information about the Legal information section"
---

{% include custom/section.warnbanner.html %}

## Legal Information Section Content ##
The Legal information section carries information about legal information relevant to the patient. PRSB Elements should be formatted as subheadings in any HTML sent.

<table style="width:100%;max-width: 100%;">
	<thead>
		<tr>
			<th width="15%">Section</th>
			<th width="35%">Description</th>
			<th width="5%">Card.</th>
			<th width="5%">MRO*</th>
			<th width="40%">FHIR Target and Guidance</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Legal information</td>
			<td>Legal information captured relating to patient care, such as consent to treatment and mental capacity.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>Carried in the CodeableConcept of <b>Composition.section.code</b> FHIR element.</td>
		</tr>
		<tr>
			<th>PRSB Element</th>
			<th>Description</th>
			<th>Card.</th>
			<th>MRO*</th>
			<th>FHIR Target and Guidance</th>		
		</tr>
		<tr>
			<td>Consent for treatment record</td>
			<td>Whether consent has been obtained for the treatment. May include where record of consent is located or record of consent.</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>A statement about the patient's consent to treatment. Text.</td>
		</tr>
		<tr>
			<td>Consent for information sharing</td>
			<td>This is a record of consent for information sharing. Where consent has been not been obtained or sought, the reason why must be provided. Include best interests decision where person lacks capacity.</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>This is a record of the person's consent to information sharing. Text only.</td>
		</tr>
		<tr>
			<td>Consent relating to child</td>
			<td>Consideration of age and competency. Record of person with parental responsibility or appointed guardian where child lacks competency.</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>The consent record relating to a child. Text only.</td>
		</tr>
		<tr>
			<td>Mental capacity assessment</td>
			<td>Whether an assessment of the mental capacity of the (adult) person has been undertaken, if so, what capacity the decision relates to, who carried it out, when and the outcome of the assessment. Also record best interests decision if person lacks capacity.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>The record of the assessment in free text.</td>
		</tr>
		<tr>
			<td>Advance decision to refuse treatment (ADRT)</td>
			<td>A record of an advance decision to refuse one or more specific types of future treatment, made by a person who had capacity at the time of recording the decision. The decision only applies when the person no longer has the capacity to consent to or refuse the specific treatment being considered. An ADRT must be in writing, signed and witnessed. If the ADRT is refusing life-sustaining treatment it must state specifically that the treatment is refused even if the person's life is at risk.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>Text only. Location of ADRT should be recorded as free text. Where available a copy of the ADRT may be appended to the record as a <a href="build_attachments.html">FHIR attachment</a>. Where there has been a change in the ADRT this should be noted in the record in free text.</td>
		</tr>
		<tr>
			<td>Lasting power of attorney  for personal welfare  or court-appointed deputy (or equivalent)</td>
			<td>Record of one or more people who have been given power (LPA) by the person when they had capacity to make decisions about their health and welfare should they lose capacity to make those decisions. To be valid, an LPA must have been registered with the Court of Protection. If life-sustaining treatment is being considered the LPA document must state specifically that the attorney has been given power to consent to or refuse life-sustaining treatment. Details of any person (deputy) appointed by the court to make decisions about the person's health and welfare. A deputy does not have the power to refuse life-sustaining treatment.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>Text to include the name of the LPA and the authority of the LPA. The contact details of the LPA should be recorded under the relevant contacts heading.</td>
		</tr>
		<tr>
			<td>Organ and tissue donation</td>
			<td>Whether the person has given consent for organ and/or tissue donation or opted out of automatic donation where applicable. The location of the relevant information/documents.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>This is information volunteered by the patient and/or relatives. Text only.</td>
		</tr>
		<tr>
			<td>Safeguarding issues</td>
			<td>Any legal matters relating to safeguarding of a vulnerable child or adult, e.g., child protection plan, protection of vulnerable adult.</td>
			<td>0 to 1</td>
			<td>R</td>
			<td>Information obtained locally. Text only.</td>
		</tr>
		<tr>
		<td colspan="5"><b>* M=Mandatory R=Required O=Optional</b></td>
		</tr>
	</tbody>
</table>

## Example Legal Information Section ##

<script src="https://gist.github.com/IOPS-DEV/407d219b7bcc5f70343690974d11e6b5.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK3 FHIR eDischarge does not currently support a coded clinical summary.






