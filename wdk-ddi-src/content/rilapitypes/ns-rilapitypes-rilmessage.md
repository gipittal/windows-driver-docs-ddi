---
UID: NS:rilapitypes.RILMESSAGE
title: RILMESSAGE (rilapitypes.h)
description: "Don't use this structure in your code. Microsoft reserves the RILMESSAGE structure for internal use only."
old-location: netvista\rilmessage.htm
tech.root: netvista
ms.date: 05/02/2018
keywords: ["RILMESSAGE structure"]
ms.keywords: "*LPRILMESSAGE, RILMESSAGE, RILMESSAGE structure [Network Drivers Starting with Windows Vista], netvista.rilmessage, ntddrilapitypes/RILMESSAGE"
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
req.typenames: RILMESSAGE, *LPRILMESSAGE
f1_keywords:
 - RILMESSAGE
 - rilapitypes/RILMESSAGE
 - LPRILMESSAGE
 - rilapitypes/LPRILMESSAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddrilapitypes.h
api_name:
 - RILMESSAGE
 - LPRILMESSAGE
---

# RILMESSAGE structure (rilapitypes.h)


## -description

This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## -struct-fields

### -field cbSize

### -field dwParams

### -field raSvcCtrAddress

### -field dwType

### -field dwFlags

### -field msgUnion

### -field msgUnion.unMsgInDeliver

### -field msgUnion.unMsgInStatus

### -field msgUnion.unMsgOutSubmit

### -field msgUnion.unMsgBcGeneral

### -field msgUnion.unMsgIS637InStatus

### -field msgUnion.unMsgCDMAInDeliver

### -field msgUnion.unMsgCDMAOutSubmit

### -field RILMSGUNION

### -field unMsgBcGeneral


### -field unMsgCDMAInDeliver


### -field unMsgCDMAOutSubmit


### -field unMsgIS637InStatus


### -field unMsgInDeliver


### -field unMsgInStatus


### -field unMsgOutSubmit

