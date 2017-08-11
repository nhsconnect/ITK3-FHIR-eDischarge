---
title: Allergies and Adverse Reactions Section
keywords:  messaging, sections
tags: [fhir,messaging,sections]
sidebar: foundations_sidebar
permalink: explore_allergies_and_adverse_reactions.html
summary: "Gives information about the Allergies and adverse reactions section"
---

{% include custom/section.warnbanner.html %}

## Allergies and Adverse Reactions Content##
The Allergies and adverse reactions section carries information about the patient's allergies and adverse reactions such as:

<ul>
<li><b>Causative agent</b> - The agent such as food, drug or substances that has caused or may cause an allergy, intolerance or adverse reaction in this patient.</li>
<li><b>Description of the reaction</b> - A description of the manifestation of the allergic or adverse reaction experienced by the patient. This may include:</li>
<ul>
<li>manifestation, eg, skin rash</li>
<li>type of reaction (allergic, adverse, intolerance)</li>
<li>severity of the reaction</li>
<li>certainty</li>
<li>evidence (eg, results of investigations).</li>
</ul>
<li><b>Probability of recurrence</b> - Probability of the reaction (allergic, adverse, intolerant) occurring.</li>
<li><b>Date first experienced</b> - When the reaction was first experienced. May be a date or partial date (eg, year) or free text (eg, during childhood).</li>
</ul>


##  Example Allergies and Adverse Reactions Sections ##

### Allergy to Penicillin ###

<script src="https://gist.github.com/unicorn150161/23480eebe86e002e82aa5df412cdb2ae.js"></script>

## Coded Resources ##

This text section should be linked to the following FHIR Resources to provide the textual information in a coded format.

- List
- AllergyIntolerance
- Flag
 
See constructing coded clinical structures - [Allergy Lists](design_allergy_lists.html)


{% include custom/messaging_overview.svg %}








