---
title: Data Mapping
keywords: design, build,
tags: [design]
sidebar: foundations_sidebar
permalink: build_data_mapping.html
summary: "Mapping of system data to ITK Message and Document resources"
---

{% include important.html content="The ITK Messaging Solution data mapping described in this section is not meant to be complete but a starting point to understand some design considerations to consider when implementing ITK Messaging Solutions." %}

## What is ITK 3  Messaging Solution Data Mapping? ##

Any ITK 3 Messaging Solution will require some mapping to the FHIR resources included in the message bundle. For documents the data will also need to be mapped to the sections of the document.

The sender of the ITK 3 Document will need to either create Bundle and MessageHeader data items or source from them from its own data store. When it sources from its own data store then a mapping will need to be done. Some data items such as UUIDs for identifiers for example will always need to be created by sending systems. 




