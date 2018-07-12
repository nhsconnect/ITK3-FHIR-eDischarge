---
title: Medications and Medical Devices Section
keywords:  messaging, sections
tags: [fhir,messaging,section]
sidebar: foundations_sidebar
permalink: explore_medication.html
summary: "Gives information about the Medications and medical devices section"
---

{% include custom/section.warnbanner.html %}

## Medications and Medical Devices Section Content ##
The Medications and medical devices section carries information about the patient's medication. PRSB Elements should be formatted as subheadings in any HTML sent. For more information on constructing medication lists see [constructing clinical coded structures](build_medication_lists.html). 

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
			<td>Medications and Medical Devices </td>
			<td>The details of and instructions for medications and medical equipment the patient is using.</td>
			<td>0 to 1</td>
			<td>O</td>
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
			<th>Medication item cluster</th>
			<th>&nbsp;</th>
			<th>&nbsp;</th>
			<th>&nbsp;</th>
			<th>&nbsp;</th>
		</tr>
		<tr>
			<td>Medication name</td>
			<td>May be generic name or brand name (as appropriate). Mandatory medication name coded using a SNOMED CT/dm+d term where possible, allowing plain text for historical/patient reported items , extemporaneous preparations or those not registered in dm+d. Comment: e.g. "Citalopram tab 20mg", "Trimethoprim".</td>
			<td>1 only</td>
			<td>M</td>
			<td>Text and a SNOMED CT concept carried in the CodeableConcept of the FHIR element <b>MedicationStatement.medication[x].<br/>medicationReference.Medication.Name</b>. See <a href="build_medication_lists.html#medicationcode">medication.code</a> for further guidance.</td>
		</tr>
		<tr>
			<td>Form</td>
			<td>Form of the medicinal substance e.g. capsules, tablets, liquid. Not normally required unless a specific form has been requested by the prescriber.  Comment: e.g. "Modified Release Capsules".</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text and a SNOMED CT concept carried in the CodeableConcept of the FHIR element <b>MedicationStatement.medication[x].<br/>medicationReference.Medication.form</b>. See <a href="build_medication_lists.html#medicationform">medication.form</a> for further guidance.</td>
		</tr>
		<tr>
			<td>Route</td>
			<td>Medication administration description (oral, IM, IV, etc.): may include method of administration, (e.g., by infusion, via nebuliser, via NG tube). Optional medication route, using SNOMED CT terms where possible. Not generally applicable to product-based medication. Should not be used to specify a specific administration site, for which a separate archetype is used e.g. The Route is 'intraocular' the Site may be 'Left eye'.   Comment: e.g. "Oral", "Intraocular". Note that this element supports multiple Routes to allow a choice to be specified by the prescriber.</td>
			<td>0 to many</td>
			<td>O</td>
			<td>Text and a SNOMED CT concept carried in the CodeableConcept of the FHIR element <b>MedicationStatement.dosage.route</b>. See <a  href="build_medication_lists.html#medicationstatementdosageroute">medicationStatement.dosage.route</a> for further guidance.</td>
		</tr>
		<tr>
			<td>Site</td>
			<td>The anatomical site at which the medication is to be administered.  Comment: e.g. "Left eye".</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text and a SNOMED CT concept carried in the CodeableConcept of the FHIR element <b>MedicationStatement.dosage.site</b>. See <a href="build_medication_lists.html#medicationstatementdosagesite">medicationStatement.dosage.site</a> for further guidance.</td>
		</tr>
		<tr>
			<td>Method</td>
			<td>The technique or method by which the medication is to be administered.</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text Only.</td>
		</tr>
		<tr>
			<td>Dose directions description</td>
			<td>A single plain text phrase describing the entire medication dosage and administration directions, including dose quantity and medication frequency.  Comment: e.g. "I tablet at night" or "20mg at 10pm" This is the form of dosage direction text normally available from UK GP systems.</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text within the <b>section.narrative.text</b> and text repeated in the FHIR element <b>MedicationStatement.dosage.text</b>.</td>
		</tr>
		<tr>
			<td>Dose amount description </td>
			<td>A plain text description of medication single dose amount, as described in the AoMRC medication headings.  Comment: e.g. "30 mg" or "2 tabs". UK Secondary care clinicians and systems normally minimally structure their dose directions, separating Dose amount and Dose timing (often referred to as Dose and Frequency). This format is not normally used in GP systems, which will always import Dose and Frequency descriptions concatenated into the single Dose directions description.</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text should be part of Dose directions description PRSB element and will be included as part of the FHIR element <b>MedicationStatement.dosage.text</b>.</td>
		</tr>
		<tr>
			<td>Dose timing description</td>
			<td>A plain text description of medication dose frequency, as described in the PRSB medication headings.  Comment: e.g. "Twice a day", "At 8am 2pm and 10pm". UK Secondary care clinicians and systems normally minimally structure their dose directions, separating Dose amount and Dose timing (often referred to as Dose and Frequency). This format is not normally used in GP systems, which will always import Dose and Frequency descriptions concatenated into the single Dose directions description.</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text should be part of Dose directions description PRSB element and will be included as part of the FHIR element <b>MedicationStatement.dosage.text</b>.</td>
		</tr>
		<tr>
			<td> <font color="red">Text Parsable dose directions</font></td>
			<td> <font color="red">A parsable 'dose syntax' which carries dose strength, dose timing, dose duration and maximum dose information.  Comment: e.g. "20-30mg ^4/6h prn [180mg /24h]" = 20 to 30 mgs, up to 4-6 hourly as required. Maximum 180mg in 24 hours. The 'as required reason' e.g. 'for pain' should be carried in the Additional Instruction element. Note that this is generally a symptom and is not the same as the Indication which will usually describe a diagnosis or condition. Where supported, this would generally be used to exchange dosage information between systems, while Structured dose directions are likely to be used only within openEHR-based systems.</font></td>
			<td> <font color="red">0 to 1</font></td>
			<td> <font color="red">O</font></td>
			<td> <font color="red"><b>DO NOT USE</b> Data items acting as placeholders for future 'advanced' structured dose syntax solution. Insufficient information to detail these further at present.</font></td>
		</tr>
		<tr>
			<td>Structured dose direction cluster</td>
			<td>A structural representation of the elements carried by the dose syntax in 'Parsable doseStrength / timing' i.e. dose strength, dose timing, dose duration and maximum dose.</td>
			<td>0 to many</td>
			<td>O</td>
			<td>Where supported (these values)
<ul>
<li>Continue indefinitely [The medication should be continued indefinitely.] </li>
<li>Do not discontinue [The medication should be continued indefinitely and the prescriber highly recommends that it should never be discontinued. This is an AoMRC Clinical Headings recommendation.]</li>
<li>Stop when course complete. [The medication should be stopped when the currently prescribed course has been completed.]</li>
<li>Duration:  Allowed values: years, months, weeks, days, hours >=0 days</li>
</ul> 
For coded information use the FHIR element <b>MedicationStatement.dosage.additionalInstruction</b>.<br/>If no codes exist use the FHIR element <b>MedicationStatement.dosage.additionalInstruction CodeableConcept.text</b><br/>
Duration goes in the FHIR element <b>MedicationStatement.effective[x].effectivePeriod</b><br/>
Implementation guidance: FHIR element <b>MedicationStatement.additionalInstruction</b> to be used as a string element for "Continue Indefinitely"; "Do not discontinue" and "Stop when course complete".<br/> 
Any Duration instructions in the FHIR element <b>MedicationStatement.effective[x].effectivePeriod</b> or in FHIR element <b>MedicationStatement.note</b> as a degrade to text.

</td>
		</tr>
		<tr>
			<td> <font color="red">Structured dose amount cluster</font></td>
			<td> <font color="red">A structural representation of dose amount.  Comment: e.g. 20mg or 2 tablets This element will generally only be used when persisting data within systems with 'Parsable dose directions' being used to exchange the same information between systems.</font></td>
			<td> <font color="red">&nbsp;</font></td>
			<td> <font color="red">O</font></td>
				<td> <font color="red"><b>DO NOT USE</b> - Data items acting as placeholders for future 'advanced' structured dose syntax solution. Insufficient information to detail these further at present.</font></td>
		</tr>
		<tr>
			<td> <font color="red">Structured dose timing cluster</font></td>
			<td> <font color="red">A slot containing a structural, computable representation of dose timing and maximum dose.  Comment: This element will generally only be used when persisting data within systems with 'Parsable dose directions' being used to exchange the same information between systems.</font></td>
			<td> <font color="red">&nbsp;</font></td>
			<td> <font color="red">O</font></td>
				<td> <font color="red"><b>DO NOT USE</b> - Data items acting as placeholders for future 'advanced' structured dose syntax solution. Insufficient information to detail these further at present.</font></td>
		</tr>
		<tr>
			<td>Dose direction duration</td>
			<td>Recommendation of the time period for which the medication should be continued, including direction not to discontinue.</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text in the <b>section.narrative.text</b> - Continue indefinitely [The medication should be continued indefinitely.]<br/>Do not discontinue [The medication should be continued indefinitely and the prescriber highly recommends that it should never be discontinued. This is an AoMRC Clinical Headings recommendation.]<br/>Stop when course complete. [The medication should be stopped when the currently prescribed course has been completed.]<br/>Duration: Allowed values: years, months, weeks, days, hours 	&gt;=0 days". Duration goes in the FHIR element MedicationStatement.effective[x].effectivePeriod and should be repeated in the FHIR element <b>MedicationStatement.dosage.additionalInstruction</b>.</td>
		</tr>
		<tr>
			<td>Additional instruction </td>
			<td>Additional multiple dosage or administration instructions as plain text. This may include guidance to the prescriber, patient or person administering the medication. In some settings, specific Administration Instructions may be re-labelled as "Patient advice' or 'Dispensing Instruction' to capture these flavours of instruction.  Comment: e.g. "Omit morning dose on day of procedure", "for pain or fever", "Dispense weekly".</td>
			<td>0 to many</td>
			<td>O</td>
			<td>Additional instruction [Additional multiple dosage or administration instructions as plain text. This may include guidance to the prescriber, patient or person administering the medication. In some settings, specific Administration Instructions may be re-labelled as "Patient advice' or 'Dispensing Instruction' to capture these flavours of instruction.]<br/>Dispensing instruction [Multiple plain text to record complex dispensing arrangements, particularly for Controlled Drug instalment dispensing. 'Dispensing instructions' may be used as a specific label to overwrite 'Additional instructions' to align with legacy GP system behaviour.]<br/>Patient advice [Multiple plain text instructions intended for patient or carer. 'Patient advice' may be used as a specific label to overwrite 'Additional instructions' to align with legacy GP system behaviour.]<br/>Monitoring [Special instructions related to monitoring of medication, such as lab tests.]. This information is carried as text in <b>section.narrative.text</b> and repeated in the FHIR elements <b>MedicationStatement.dosage.patientInstruction</b> for specific patient instruction use and <b>MedicationStatement.note</b> For narrative instructions (e.g. monitoring, pain, prevention).</td>
		</tr>
<tr>
<th colspan="5">Medication item cluster end</th>
</tr>
		<tr>
			<td><font color="red">Course details cluster</font></td>
			<td><font color="red">Details of the overall course of medication.</font></td>
			<td><font color="red">0 to 1</font></td>
			<td><font color="red">O</font></td>
			<td><font color="red"><b>Not to be used for Hospital to GP discharge summary.</b></font></td>
		</tr>
		<tr>
			<td><font color="red">Course status</font></td>
			<td><font color="red">The status of this prescription in an ambulatory (outpatient/GP/community) context.</font></td>
			<td><font color="red">0 to 1</font></td>
			<td><font color="red">O</font></td>
			<td><font color="red">Choice of Coded text:<br/>Active [This is an active medication.]<br/>Discontinued [This is a medication that has been issued. dispensed or administered but has now been discontinued.]<br/> Never active [A medication which was ordered or authorised but has been cancelled prior to being issued, dispensed or administered.]<br/> Completed [The medication course has been completed.]<br/> Obsolete [This medication order has been superseded by another.] Data items not relevant to Hospital to GP discharge summary and <b>SHOULD NOT be used</b>.</font></td>
		</tr>
		<tr>
			<td><font color="red">Start date/time</font></td>
			<td><font color="red">The date and/or time that the medication course should begin.</font></td>
			<td><font color="red">0 to 1</font></td>
			<td><font color="red">O</font></td>
			<td><font color="red">Date/time - Data items not relevant to Hospital to GP discharge summary and <b>SHOULD NOT be used</b>.</font></td>
		</tr>
		<tr>
			<td><font color="red">End date/time</font></td>
			<td><font color="red">The date and/or time that the medication course should finish.</font></td>
			<td><font color="red">0 to 1</font></td>
			<td><font color="red">O</font></td>
			<td><font color="red">Date/time. Data items not relevant to Hospital to GP discharge summary and <b>SHOULD NOT</b> be used.</font></td>
		</tr>
		<tr>
			<td><font color="red">Indication</font></td>
			<td><font color="red">Reason for medication being prescribed, where known.</font></td>
			<td><font color="red">0 to 1</font></td>
			<td><font color="red">O</font></td>
			<td><font color="red">A free text or code derived text term giving the clinical indication or reason for ordering the medication. Coded terms are preferable.<br/>Comment: e.g. "Angina". The Indication generally describes a condition or diagnosis. Data items not relevant to Hospital to GP discharge summary and <b>SHOULD NOT</b> be used.</font></td>
		</tr>
		<tr>
			<td><font color="red">Link to indication record</font></td>
			<td><font color="red">A link to the record which contains the Indication for this medication order.</font></td>
			<td><font color="red">0 to 1</font></td>
			<td><font color="red">O</font></td>
			<td><font color="red">URL. Data items not relevant to Hospital to GP discharge summary and <b>SHOULD NOT</b> be used.</font></td>
		</tr>
		<tr>
			<td><font color="red">Comment/recommendation</font></td>
			<td><font color="red">Suggestions about duration and/or review, ongoing monitoring requirements, advice on starting, discontinuing or changing medication.</font></td>
			<td><font color="red">0 to 1</font></td>
			<td><font color="red">O</font></td>
			<td><font color="red">Free text. Additional comment or recommendation about the medication course e.g. 'Patient named supply', 'unlicensed medication', 'Foreign brand' or monitoring recommendations. Data items not relevant to Hospital to GP discharge summary and <b>SHOULD NOT</b> be used.</font></td>
		</tr>
<tr ><td colspan="5"><font color="red">End of course details cluster</font></td></tr>
		<tr>
			<th>Medication change summary cluster</th>
			<th>Records the changes made to medication since admission</th>
			<th>0 to 1</th>
			<th>O</th>
			<th>&nbsp;</th>
		</tr>
		<tr>
			<td>Status</td>
			<td>The nature of any change made to the medication since admission.</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text containing the strings associated with the codes as below<br/>Continued [Medicine present on both admission and discharge with no amendments.]<br/>Added [Medicine present on discharge but not on admission]<br/>Amended [Medicine present on both admission and discharge but with amendment(s) since admission.] and coded using the FHIR elements in <b>MedicationStatement.Extension<br/>-CareConnect-MedicationChangeSummary</b>, These will use the <b>status</b> element.</td>
		</tr>
		<tr>
			<td>Indication</td>
			<td>Reason for change in medication, e.g. sub-therapeutic dose, patient intolerant.</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text is carried using the FHIR elements in <b>MedicationStatement.Extension<br/>-CareConnect-MedicationChangeSummary</b>, this will use the <b>indicationForChange</b> element.</td>
		</tr>
		<tr>
			<td>Date of latest change</td>
			<td>The date of the latest change - addition, or amendment</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text and carried using the FHIR elements in <b>MedicationStatement.Extension<br/>-CareConnect-MedicationChangeSummary</b>, this will use the <b>dateChanged</b> element.</td>
		</tr>
		<tr>
			<td>Description of amendment</td>
			<td>Where a change is made to the medication i.e. one drug stopped and another started or e.g. dose, frequency or route is changed.</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text and carried using the FHIR elements in <b>MedicationStatement.Extension<br/>-CareConnect-MedicationChangeSummary</b>, this will use the <b>detailsOfAmendment</b> element.</td>
		</tr>
		<tr>
			<td>Comment</td>
			<td>Any additional comment about the medication change</td>
			<td>0 to 1</td>
			<td>O</td>
			<td><b>This heading is no longer used  and comments should be included in the Description of amendment heading.</b></td>
		</tr>
		<tr>
			<td> <font color="red">Total dose daily quantity cluster</font></td>
			<td><font color="red">The total daily dose of this medication. This is helpful for estimating optimal adherence to dosing guidance. It may be computed from product/dose strength and frequency or entered manually.</font></td>
			<td><font color="red">0 to 1</font></td>
			<td><font color="red">O</font></td>
			<td><font color="red">Data item not relevant to Hospital to GP discharge summary and <b>MUST NOT</b> be used.</font></td>
		</tr>
		<tr>
			<td>Medical devices entry</td>
			<td>Any therapeutic medical device of relevance that does not have representation in the NHS dictionary of medicines and medical devices (dm+d).</td>
			<td>0 to many</td>
			<td>O</td>
			<td>Text only.</td>
		</tr>
		<tr>
			<th>Medication discontinued entry</th>
			<th>&nbsp;</th>
			<th>&nbsp;</th>
			<th>&nbsp;</th>
			<th>&nbsp;</th>
		</tr>
		<tr>
			<td>Name of discontinued medication</td>
			<td>May be generic name or brand name (as appropriate).Mandatory medication name coded using a SNOMED CT/dm+d term where possible, allowing plain text for historical/patient reported items , extemporaneous preparations or those not registered in dm+d. Comment: e.g."Citalopram tab 20mg", "Trimethoprim"</td>
			<td>1 only</td>
			<td>M</td>
			<td>Text and a SNOMED CT concept carried in the CodeableConcept of the FHIR element <b>MedicationStatement.medication[x].<br/>medicationReference.Medication.Name</b>. See <a href="build_medication_lists.html#medicationcode">medication.code</a> for further guidance.</td>
		</tr>
		<tr>
			<td>Status</td>
			<td>The nature of any change made to the medication since admission.</td>
			<td>1</td>
			<td>M</td>
			<td>Text and carried in the FHIR element <b>MedicationStatement.status</b> which <b>MUST</b> contain the value of "stopped"</td>
		</tr>
		<tr>
			<td>Indication</td>
			<td>The clinical indication for any changes in medication status</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text and carried in the FHIR element <b>MedicationStatement.reasonCode</b>.</td>
		</tr>
		<tr>
			<td>Date of latest change</td>
			<td>The date of the discontinuation</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text and carried in the FHIR element <b>MedicationStatement.effectiveDateTime</b>.</td>
		</tr>
		<tr>
			<td>Description of amendment</td>
			<td>A description of any amendment</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text and carried in the FHIR element <b>MedicationStatement.note</b>.</td>
		</tr>
		<tr>
			<td>Comment</td>
			<td>Any additional comment about the medication change.</td>
			<td>0 to 1</td>
			<td>O</td>
			<td>Text and may also be carried in the FHIR element <b>"MedicationStatement.note</b>.</td>
		</tr>
		<tr>
		<td colspan="5"><b>* M=Mandatory R=Required O=Optional</b></td>
		</tr>
	</tbody>
</table>


## Example Medications and Medical Devices Section ##

<script src="https://gist.github.com/IOPS-DEV/0a5596bdf4ab2c880eacb409e44c09df.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- List
- MedicationStatement
- Medication
- MedicationDispense
 
See constructing clinical coded structures - [Medication Lists](build_medication_lists.html)











