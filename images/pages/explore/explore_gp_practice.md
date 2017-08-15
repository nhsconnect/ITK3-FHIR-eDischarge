---
title: GP Practice Section
keywords:  messaging, sections
tags: [fhir,messaging,sections]
sidebar: foundations_sidebar
permalink: explore_gp_practice.html
summary: "Gives information about the patient's GP Practice"
---
{% include custom/non_text_section.warnbanner.html %}


## GP Practice Section Content##

The GP Practice section is rendered from the careProvider reference in the patient resource which uses Practitioner and Organization resources to the carry information about the patient's GP practice and GP. Items in bold are subheadings and should be formatted as such when rendered: 

<ul>
<li><b>GP name</b></li>
This is rendered from the practitioner resource 
<li><b>GP practice details</b></li>
<li><b>GP practice identifier</b></li>
These are rendered from the organization resource
</ul>


## Example GP Practice Using Organization Resource ##

<script src="https://gist.github.com/unicorn150161/93469cbeb6220339a745f9706cecc004.js"></script>

## Example GP Name Using Practitioner Resource ##

Note: The GP is linked to the GP Practice by the Practitioner resource referencing the organization resource using the managingOrganization element.

<script src="https://gist.github.com/unicorn150161/1d719278e4f08e06d595ac228c00f677.js"></script>




