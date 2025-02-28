---
UID: NF:ntifs.CcMdlWriteAbort
title: CcMdlWriteAbort function (ntifs.h)
description: The CcMdlWriteAbort routine frees memory descriptor lists (MDL) created by an earlier call to CcPrepareMdlWrite.
old-location: ifsk\ccmdlwriteabort.htm
tech.root: ifsk
ms.date: 04/16/2018
keywords: ["CcMdlWriteAbort function"]
ms.keywords: CcMdlWriteAbort, CcMdlWriteAbort routine [Installable File System Drivers], ccref_517f25ce-d707-4611-af24-c66010b0d89e.xml, ifsk.ccmdlwriteabort, ntifs/CcMdlWriteAbort
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available on Microsoft Windows XP and later.
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
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: PASSIVE_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - CcMdlWriteAbort
 - ntifs/CcMdlWriteAbort
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - CcMdlWriteAbort
---

# CcMdlWriteAbort function


## -description

The <b>CcMdlWriteAbort</b> routine frees memory descriptor lists (MDL) created by an earlier call to <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccpreparemdlwrite">CcPrepareMdlWrite</a>.

## -parameters

### -param FileObject [in]


File object pointer that was passed to <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccpreparemdlwrite">CcPrepareMdlWrite</a>.

### -param MdlChain [in]


Address of the MDL chain returned by <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccpreparemdlwrite">CcPrepareMdlWrite</a>.

## -remarks

File systems call <b>CcMdlWriteAbort</b> to free the memory descriptor lists (MDL) created by an earlier call to <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccpreparemdlwrite">CcPrepareMdlWrite</a> for a cached file. All physical pages that were locked down are unlocked. Any pages that were mapped are unmapped. 

File systems normally call <b>CcMdlWriteAbort</b> only in cases where, after a successful call to <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccpreparemdlwrite">CcPrepareMdlWrite</a>, it is necessary to abort or fail the subsequent MDL write operation. 

Unlike <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccmdlwritecomplete">CcMdlWriteComplete</a>, <b>CcMdlWriteAbort</b> does not cause any data to be written to the cached file.

## -see-also

<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccmdlwritecomplete">CcMdlWriteComplete</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccpreparemdlwrite">CcPrepareMdlWrite</a>
