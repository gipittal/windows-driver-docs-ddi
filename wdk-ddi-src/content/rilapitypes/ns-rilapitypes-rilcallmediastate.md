---
UID: NS:rilapitypes.RILCALLMEDIASTATE
title: RILCALLMEDIASTATE (rilapitypes.h)
description: "Don't use this structure in your code. Microsoft reserves the RILCALLMEDIASTATE structure for internal use only."
old-location: netvista\rilcallmediastate.htm
tech.root: netvista
ms.date: 05/02/2018
keywords: ["RILCALLMEDIASTATE structure"]
ms.keywords: "*LPRILCALLMEDIASTATE, RILCALLMEDIASTATE, RILCALLMEDIASTATE structure [Network Drivers Starting with Windows Vista], netvista.rilcallmediastate, ntddrilapitypes/RILCALLMEDIASTATE"
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
req.typenames: RILCALLMEDIASTATE, *LPRILCALLMEDIASTATE
f1_keywords:
 - RILCALLMEDIASTATE
 - rilapitypes/RILCALLMEDIASTATE
 - LPRILCALLMEDIASTATE
 - rilapitypes/LPRILCALLMEDIASTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddrilapitypes.h
api_name:
 - RILCALLMEDIASTATE
 - LPRILCALLMEDIASTATE
---

# RILCALLMEDIASTATE structure (rilapitypes.h)


## -description

This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## -struct-fields

### -field dwDirection

### -field dwCallMediaType

### -field mediaStateUnion

### -field mediaStateUnion.stAudioState

### -field mediaStateUnion.stVideoState

### -field mediaStateUnion.dwCustomStateSpecific

### -field mediaStateUnion.pad

### -field RILCALLMEDIASTATEUNION

### -field dwCustomStateSpecific


### -field pad


### -field stAudioState


### -field stVideoState

