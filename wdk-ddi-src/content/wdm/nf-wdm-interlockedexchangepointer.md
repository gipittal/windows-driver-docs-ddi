---
UID: NF:wdm.InterlockedExchangePointer
title: InterlockedExchangePointer function (wdm.h)
description: The InterlockedExchangePointer function (wdm.h) performs an atomic operation that sets a pointer to a new value.
old-location: kernel\interlockedexchangepointer.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["InterlockedExchangePointer function"]
ms.keywords: InterlockedExchangePointer, InterlockedExchangePointer routine [Kernel-Mode Driver Architecture], k102_4959af35-65d8-4768-94f7-a2dad0a2db46.xml, kernel.interlockedexchangepointer, wdm/InterlockedExchangePointer
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h, Miniport.h
req.target-type: Desktop
req.target-min-winverclnt: Available starting with Windows 2000.
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
req.irql: Any level
targetos: Windows
req.typenames: 
f1_keywords:
 - InterlockedExchangePointer
 - wdm/InterlockedExchangePointer
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wdm.h
api_name:
 - InterlockedExchangePointer
---

# InterlockedExchangePointer function (wdm.h)


## -description

The <b>InterlockedExchangePointer</b> routine performs an atomic operation that sets a pointer to a new value.

## -parameters

### -param Target [in, out]


A pointer to a PVOID value. The routine sets (*<i>Target</i>) to <i>Value</i>.

### -param Value [in, optional]


Specifies the PVOID value to set (*<i>Target</i>) to.

## -returns

<b>InterlockedExchangePointer</b> returns the original value of the pointer at *<i>Target</i> (that is, the value of this pointer at entry to the routine).

## -remarks

<b>InterlockedExchangePointer</b> provides a fast, atomic way to synchronize updating a pointer variable that is shared by multiple threads.

<b>InterlockedExchangePointer</b> is designed for speed and, typically, is implemented inline by a compiler. <b>InterlockedExchangePointer</b> is atomic only with respect to other <b>Interlocked<i>Xxx</i></b> calls. It does not use a spin lock and can be safely used on pageable data. 

The <i>Target</i> parameter should be aligned on either a 32-bit or 64-bit boundary, depending on the system type, for better performance.

A call to <b>InterlockedExchangePointer</b> is atomic only with respect to other <b>Interlocked<i>Xxx</i></b> calls.

Interlocked operations cannot be used on non-cached memory.

## -see-also

<a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-interlockedcompareexchange">InterlockedCompareExchange</a>



<a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-interlockedcompareexchangepointer">InterlockedCompareExchangePointer</a>



<a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-interlockedexchange">InterlockedExchange</a>
