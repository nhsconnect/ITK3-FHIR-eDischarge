---
title: Use of MESH
keywords: design, build,
tags: [design]
sidebar: foundations_sidebar
permalink: build_mesh.html
summary: "Using MESH withTransfer of Care Documents"
---


## Overview ##

The Transfer of Care documents should be sent using [ITK over MESH](https://developer.nhs.uk/apis/itk3messagedistribution-2-8-0/mesh.html) for further information.

## Use of GP look up on MESH ##

When sending a Transfer of Care document over MESH and the patient's GP practice is not known, then the GP look-up facility supported by MESH **SHOULD** be used. However, some identifier elements with in the document cannot be populated.

In this instance any identifier elements which require the Patient's GP practice ODS code should be populated with "V81999" to indicate "code not known". 

  


 



