---
UID: NI:sidebandaudio.IOCTL_SBAUD_GET_SIDETONE_STATUS_UPDATE
title: IOCTL_SBAUD_GET_SIDETONE_STATUS_UPDATE (sidebandaudio.h)
description: "Learn more about: IOCTL_SBAUD_GET_SIDETONE_STATUS_UPDATE IOCTL"
ms.date: 10/05/2018
keywords: ["IOCTL_SBAUD_GET_SIDETONE_STATUS_UPDATE IOCTL"]
req.header: sidebandaudio.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: 
req.ddi-compliance: 
req.max-support: 
targetos: Windows
tech.root: audio
ms.custom: RS5
f1_keywords:
 - IOCTL_SBAUD_GET_SIDETONE_STATUS_UPDATE
 - sidebandaudio/IOCTL_SBAUD_GET_SIDETONE_STATUS_UPDATE
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sidebandaudio.h
api_name:
 - IOCTL_SBAUD_GET_SIDETONE_STATUS_UPDATE
---

# IOCTL_SBAUD_GET_SIDETONE_STATUS_UPDATE IOCTL

### Major Code:  [IRP_MJ_DEVICE_CONTROL](/windows-hardware/drivers/kernel/irp-mj-device-control)


## -description

This control codes used by an audio driver when cooperating with the Audio class drivers to operate a Sideband connection.

## -ioctlparameters

### -input-buffer


### -input-buffer-length 


### -output-buffer


### -output-buffer-length 


### -in-out-buffer


### -inout-buffer-length 


### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.
Otherwise, Status to the appropriate error condition as a NTSTATUS code. 
For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

## -see-also
