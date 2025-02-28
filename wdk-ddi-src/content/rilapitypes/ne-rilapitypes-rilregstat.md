---
UID: NE:rilapitypes.RILREGSTAT
title: RILREGSTAT (rilapitypes.h)
description: "Microsoft reserves the RILREGSTAT enumeration for internal use only. Don't use this enumeration in your code."
old-location: netvista\rilregstat_2.htm
tech.root: netvista
ms.date: 02/26/2018
keywords: ["RILREGSTAT enumeration"]
ms.keywords: RILREGSTAT, RILREGSTAT enumeration [Network Drivers Starting with Windows Vista], RIL_REGSTAT_ATTEMPTING, RIL_REGSTAT_DENIED, RIL_REGSTAT_HOME, RIL_REGSTAT_MAX, RIL_REGSTAT_ROAMING, RIL_REGSTAT_ROAMING_DOMESTIC, RIL_REGSTAT_UNREGISTERED, netvista.rilregstat_2, rilapitypes/RILREGSTAT, rilapitypes/RIL_REGSTAT_ATTEMPTING, rilapitypes/RIL_REGSTAT_DENIED, rilapitypes/RIL_REGSTAT_HOME, rilapitypes/RIL_REGSTAT_MAX, rilapitypes/RIL_REGSTAT_ROAMING, rilapitypes/RIL_REGSTAT_ROAMING_DOMESTIC, rilapitypes/RIL_REGSTAT_UNREGISTERED
req.header: rilapitypes.h
req.include-header: 
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
req.lib: NtosKrnl.exe
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RILREGSTAT
req.product: Windows 10 or later.
f1_keywords:
 - RILREGSTAT
 - rilapitypes/RILREGSTAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rilapitypes.h
api_name:
 - RILREGSTAT
---

# RILREGSTAT enumeration (rilapitypes.h)


## -description

This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## -enum-fields

### -field RIL_REGSTAT_UNKNOWN

### -field RIL_REGSTAT_UNREGISTERED

### -field RIL_REGSTAT_HOME

### -field RIL_REGSTAT_ATTEMPTING

### -field RIL_REGSTAT_DENIED

### -field RIL_REGSTAT_ROAMING

### -field RIL_REGSTAT_ROAMING_DOMESTIC

### -field RIL_REGSTAT_MAX

## -syntax

```cpp
typedef enum _RILREGSTAT {
  RIL_REGSTAT_UNREGISTERED,
  RIL_REGSTAT_HOME,
  RIL_REGSTAT_ATTEMPTING,
  RIL_REGSTAT_DENIED,
  RIL_REGSTAT_ROAMING,
  RIL_REGSTAT_ROAMING_DOMESTIC,
  RIL_REGSTAT_MAX
} RILREGSTAT;
```

