---
UID: NS:rilapitypes.RILCALLDISCONNECTDETAILS
title: RILCALLDISCONNECTDETAILS (rilapitypes.h)
description: "Don't use this structure in your code. Microsoft reserves the RILCALLDISCONNECTDETAILS structure for internal use only. "
old-location: netvista\rilcalldisconnectdetails.htm
tech.root: netvista
ms.date: 05/02/2018
keywords: ["RILCALLDISCONNECTDETAILS structure"]
ms.keywords: "*LPRILCALLDISCONNECTDETAILS, RILCALLDISCONNECTDETAILS, RILCALLDISCONNECTDETAILS structure [Network Drivers Starting with Windows Vista], netvista.rilcalldisconnectdetails, ntddrilapitypes/RILCALLDISCONNECTDETAILS"
req.header: rilapitypes.h
req.include-header: Rilapitypes.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RILCALLDISCONNECTDETAILS, *LPRILCALLDISCONNECTDETAILS
f1_keywords:
 - RILCALLDISCONNECTDETAILS
 - rilapitypes/RILCALLDISCONNECTDETAILS
 - LPRILCALLDISCONNECTDETAILS
 - rilapitypes/LPRILCALLDISCONNECTDETAILS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddrilapitypes.h
api_name:
 - RILCALLDISCONNECTDETAILS
 - LPRILCALLDISCONNECTDETAILS
---

# RILCALLDISCONNECTDETAILS structure (rilapitypes.h)


## -description

This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## -struct-fields

### -field dwDisconnectGroup

### -field causeUnion

### -field causeUnion.unGPPCause

### -field causeUnion.unGPPRejectCause

### -field causeUnion.unGPP2Cause

### -field causeUnion.unIMSSIPCause

### -field causeUnion.dwASCode

### -field causeUnion.dwOtherCode

### -field RILCAUSEUNION

### -field dwASCode


### -field dwOtherCode


### -field unGPP2Cause


### -field unGPPCause


### -field unGPPRejectCause


### -field unIMSSIPCause

