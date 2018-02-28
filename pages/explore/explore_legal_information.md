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
The Legal information section carries information about about legal information relevant to the patient, subheadings should be formatted as such in any html sent:

<table width="100%">
<tr>
<th width="25%">Sub-section</th>
<th width="45%">Description</th>
<th width="15%">Cardinally</th>
<th width="15%">Conformance</th>
</tr>
<tr>
<td>Consent for treatment record</td>
<td>Whether consent has been obtained for the treatment. May include where record of consent is located or record of consent.
</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Consent for information sharing</td>
<td>This is a record of consent for information sharing. Where consent has been not been obtained or sought, the reason why must be provided. Include best interests decision where person lacks capacity.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Consent relating to child</td>
<td>"Consideration of age and competency, applying Gillick competency or Fraser guidelines.
Record of person with parental responsibility or appointed guardian where child lacks competency. Record if there is disagreement between patient and parent. 
</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr>
<td>Mental capacity assessment</td>
<td>Whether an assessment of the mental capacity of the (adult) person has been undertaken, if so, what capacity the decision relates to, who carried it out, when and the outcome of the assessment. Also record best interests decision if person lacks capacity.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr> 
<td>Lasting power of attorney for personal welfare  or court-appointed deputy (or equivalent)</td>
<td>Record of one or more people who have been given power (LPA) by the person when they had capacity to make decisions about their health and welfare should they lose capacity to make those decisions. To be valid, an LPA must have been registered with the Court of Protection. If life-sustaining treatment is being considered the LPA document must state specifically that the attorney has been given power to consent to or refuse life-sustaining treatment. Details of any person (deputy) appointed by the court to make decisions about the person’s health and welfare. A deputy does not have the power to refuse life-sustaining treatment.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr> 
<td>Advance decision to refuse treatment (ADRT)</td>
<td>A record of an advance decision to refuse one or more specific types of future treatment, made by a person who had capacity at the time of recording the decision. The decision only applies when the person no longer has the capacity to consent to or refuse the specific treatment being considered. An ADRT must be in writing, signed and witnessed. If the ADRT is refusing life-sustaining treatment it must state specifically that the treatment is refused even if the person’s life is at risk.
</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr> 
<td>Safeguarding issues</td>
<td>Any legal matters relating to safeguarding of a vulnerable child or adult, e.g., child protection plan, protection of vulnerable adult.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
<tr> 
<td>Organ and tissue donation</td> 
<td>Whether the person has given consent for organ and/or tissue donation or opted out of automatic donation where applicable. The location of the relevant information/documents.</td>
<td>1..1</td>
<td>Mandatory</td>
</tr>
</table>

 




## Example Legal Information Section ##

<script src="https://gist.github.com/IOPS-DEV/407d219b7bcc5f70343690974d11e6b5.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- The ITK FHIR eDischarge does not currently support a coded clinical summary.






