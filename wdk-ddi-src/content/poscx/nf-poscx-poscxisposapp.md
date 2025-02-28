---
UID: NF:poscx.PosCxIsPosApp
title: PosCxIsPosApp function (poscx.h)
description: PosCxIsPosApp checks if the open instance is associated with a point-of-service application.
old-location: pos\poscxisposapp.htm
tech.root: pos
ms.date: 02/23/2018
keywords: ["PosCxIsPosApp function"]
ms.keywords: PosCxIsPosApp, PosCxIsPosApp function, pos.poscxisposapp, poscx/PosCxIsPosApp
req.header: poscx.h
req.include-header: Poscx.h
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
req.typenames: 
req.product: Windows 10 or later.
f1_keywords:
 - PosCxIsPosApp
 - poscx/PosCxIsPosApp
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - poscx.h
api_name:
 - PosCxIsPosApp
---

# PosCxIsPosApp function


## -description

PosCxIsPosApp checks if the open instance is associated with a point-of-service application.

## -parameters

### -param device [in]


A handle to a framework device object that represents the device.

### -param fileObject [in]


A handle to a framework file object that identifies the caller, usually acquired with <a href="/windows-hardware/drivers/ddi/wdfrequest/nf-wdfrequest-wdfrequestgetfileobject">WdfRequestGetFileObject</a>.

## -returns

Returns TRUE if <i>fileObject</i> is associated with a point-of-service application. Otherwise, returns FALSE.
