---
UID: NS:bthioctl._BTH_SDP_CONNECT
title: _BTH_SDP_CONNECT (bthioctl.h)
description: The BTH_SDP_CONNECT structure contains input and output information about a connection between the local Bluetooth system and a remote SDP server. This structure is passed as the input buffer and output buffer of IOCTL_BTH_SDP_CONNECT.
old-location: bltooth\bth_sdp_connect.htm
tech.root: bltooth
ms.date: 11/30/2021
keywords: ["BTH_SDP_CONNECT structure"]
ms.keywords: "*PBTH_SDP_CONNECT, BTH_SDP_CONNECT, BTH_SDP_CONNECT structure [Bluetooth Devices], PBTH_SDP_CONNECT, PBTH_SDP_CONNECT structure pointer [Bluetooth Devices], _BTH_SDP_CONNECT, bltooth.bth_sdp_connect, bth_structs_5502fd7e-54f1-46dd-a441-68103d439c27.xml, bthioctl/BTH_SDP_CONNECT, bthioctl/PBTH_SDP_CONNECT"
req.header: bthioctl.h
req.include-header: Bthioctl.h
req.target-type: Windows
req.target-min-winverclnt: Versions:\_Supported in Windows Vista, and later.
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
req.typenames: BTH_SDP_CONNECT, *PBTH_SDP_CONNECT
f1_keywords:
 - _BTH_SDP_CONNECT
 - bthioctl/_BTH_SDP_CONNECT
 - PBTH_SDP_CONNECT
 - bthioctl/PBTH_SDP_CONNECT
 - BTH_SDP_CONNECT
 - bthioctl/BTH_SDP_CONNECT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - bthioctl.h
api_name:
 - _BTH_SDP_CONNECT
 - PBTH_SDP_CONNECT
 - BTH_SDP_CONNECT
---

# _BTH_SDP_CONNECT structure

## -description

The BTH_SDP_CONNECT structure contains input and output information about a connection between the local Bluetooth system and a remote SDP server. This structure is passed as the input buffer and output buffer of [IOCTL_BTH_SDP_CONNECT](/windows-hardware/drivers/ddi/bthioctl/ni-bthioctl-ioctl_bth_sdp_connect).

## -struct-fields

### -field bthAddress

The address of the remote SDP server that the local system connects to. This address cannot be to the local radio.

### -field fSdpConnect

A flag or combination of flags that determines how to handle the connection request. Valid flag values are listed in the following table.

| Flag                  | Description                                                     |
|-----------------------|-----------------------------------------------------------------|
| SDP_CONNECT_ALLOW_PIN | If requested, perform a pin exchange with the remote device.    |
| SDP_CONNECT_CACHE     | Requests are serviced out of the local cache of the SDP record. |

### -field HANDLE_SDP_FIELD_NAME

When the connect request returns, this specifies the handle to the SDP connection to the remote server.

### -field requestTimeout

Timeout, in seconds, for the requests on this SDP channel. If the request times out, the SDP connection represented by the HANDLE_SDP must be closed. The values for this field are bound by SDP_REQUEST_TO_MIN and SDP_REQUEST_MAX. If SDP_REQUEST_TO_DEFAULT is specified, the timeout is 30 seconds.

## -see-also

- [IOCTL_BTH_SDP_CONNECT](/windows-hardware/drivers/ddi/bthioctl/ni-bthioctl-ioctl_bth_sdp_connect)
