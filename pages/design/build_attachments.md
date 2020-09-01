---
title: Use of Attachments
keywords: design, build
tags: [design]
sidebar: foundations_sidebar
permalink: build_attachments.html
summary: "Use of Attachments in Transfer of Care Documents"
---

{% include important.html content="All information provided below is indicative and subject to on-going review." %}

## Background ##

The Transfer of Care documents allow for attachments to be included within a structured FHIR document.

## Use Cases ##

Senders <b>MAY</b> include attachments within the Transfer of Care documents. For example to include copies of related documents such as patient Advance Statements. 

## Format of Attachments ##

Sender <b>SHOULD</b> send attachments as a PDF, but <b>MAY</b> use other formats by local agreement.
This is the default attachment support format. However, senders can reasonably expect GP IT suppliers to provide support for at least the following additional extensions in the table below.

<table>
	<tr>
		<th>Mime Type</th>
		<th>Extension</th>
	</tr>
	<tr>
		<td>application/pdf</td>
		<td>pdf</td>
	</tr>
	<tr>
		<td>application/msword</td>
		<td>doc</td>
		</tr>
	<tr>
		<td>application/vnd.openxmlformats-officedocument.wordprocessingml.document</td>
		<td>docx</td>
	</tr>
	<tr>
		<td>application/rtf</td>
		<td>rtf</td>
	</tr>
		<tr>
		<td>text/html</td>
		<td>html</td>
	</tr>
	<tr>
		<td>text/plain</td>
		<td>txt</td>
	</tr>
	<tr>
		<td>text/xml</td>
		<td>xml</td>
	</tr>
	<tr>
		<td>image/jpeg or image/jpg</td>
		<td>jpg</td>
	</tr>
		<tr>
		<td>image/png</td>
		<td>png</td>
	</tr>
	<tr>
		<td>image/tiff</td>
		<td>tiff</td>
	</tr>
</table>

## Receivers of Attachments ##

Receivers <b>SHOULD</b> process attachments in-line with the rules stated in the <a href="https://developer.nhs.uk/apis/itk3messagedistribution/explore_s_and_r.html" target="_blank">ITK3 Messaging Distribution Specification</a>. 

## Binary Resource ##

All attachments are carried in the FHIR Binary Resource and <b>MUST</b> be Base64 encoded. The FHIR Binary Resource is profiled as <a href="https://fhir.nhs.uk/STU3/StructureDefinition/ITK-Attachment-Binary-1">ITK-Attachment-Binary-1</a> . 

## Example Attachment ##
<script src="https://gist.github.com/IOPS-DEV/58db5fe49a403172541478f2dadffa8b.js"></script> 





