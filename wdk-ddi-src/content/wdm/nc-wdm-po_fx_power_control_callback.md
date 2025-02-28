---
UID: NC:wdm.PO_FX_POWER_CONTROL_CALLBACK
title: PO_FX_POWER_CONTROL_CALLBACK (wdm.h)
description: The PowerControlCallback callback routine performs a power control operation that is requested by the power management framework (PoFx).
old-location: kernel\powercontrolcallback.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["PO_FX_POWER_CONTROL_CALLBACK callback function"]
ms.keywords: PO_FX_POWER_CONTROL_CALLBACK, PowerControlCallback, PowerControlCallback routine [Kernel-Mode Driver Architecture], kernel.powercontrolcallback, wdm/PowerControlCallback
req.header: wdm.h
req.include-header: Wudfwdm.h
req.target-type: Desktop
req.target-min-winverclnt: Supported starting with Windows 8.
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
req.irql: Called at IRQL <= DISPATCH_LEVEL.
targetos: Windows
req.typenames: 
f1_keywords:
 - PO_FX_POWER_CONTROL_CALLBACK
 - wdm/PO_FX_POWER_CONTROL_CALLBACK
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wdm.h
api_name:
 - PO_FX_POWER_CONTROL_CALLBACK
---

# PO_FX_POWER_CONTROL_CALLBACK callback function


## -description

The <i>PowerControlCallback</i> callback routine performs a power control operation that is requested by the power management framework (PoFx).

## -parameters

### -param DeviceContext

### -param PowerControlCode [in]


A pointer to the power control code. This code is a GUID value that specifies the requested operation.

### -param InBuffer [in, optional]


A pointer to the buffer that contains the input data for the operation. The format for the data in this buffer depends on the power control code specified by the <i>PowerControlCode</i> parameter. The <i>InBuffer</i> parameter is optional and can be specified as NULL if the specified operation requires no input data.

### -param InBufferSize [in]


The size, in bytes, of the input buffer that is pointed to by the <i>InBuffer</i> parameter. If <i>InBuffer</i> is NULL, this parameter is zero.

### -param OutBuffer [out, optional]


A pointer to the buffer to which the callback routine writes the output data from the operation. The format for the data in this buffer depends on the power control code specified by the <i>PowerControlCode</i> parameter.  The <i>OutBuffer</i> parameter is optional and can be specified as NULL if the specified operation produces no output data.

### -param OutBufferSize [in]


The size, in bytes, of the output buffer that is pointed to by the <i>OutBuffer</i> parameter. If <i>OutBuffer</i> is NULL, this parameter is zero.

### -param BytesReturned [out, optional]


A pointer to a location into which the routine writes the number of bytes of data that were written to the buffer that is pointed to by <i>OutBuffer</i>. The number of bytes written must be less than or equal to <i>OutBufferSize</i>. This parameter is optional and can be specified as NULL if the caller does not need to know how many bytes were written to the output buffer.


### -param Context [in]

A pointer to the device context. The device driver uses this context to store information about the current power state of the device. The device driver specified this pointer in the <b>DeviceContext</b> member of the <a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_po_fx_device_v1">PO_FX_DEVICE</a> structure that the driver used to register the device with PoFx. This context is opaque to PoFx.

## -returns

The <i>PowerControlCallback</i> routine returns STATUS_SUCCESS if the call is successful. Otherwise, it returns an appropriate error code.

## -remarks

PoFx calls this routine to send a power control request directly to the device driver. A power control request is similar to an I/O control request (IOCTL). Unlike an IOCTL, however, a power control request is sent directly to the driver and is not observed by other device drivers in the device stack. During a <i>PowerControlCallback</i> call, the driver synchronously performs the requested operation.

This routine is optional. A device driver that does not support power control operations is not required to implement a <i>PowerControlCallback</i> routine.

The device driver can call the <a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-pofxpowercontrol">PoFxPowerControl</a> routine to send a power control request to PoFx.

For more information about power control requests, see <a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-pofxpowercontrol">PoFxPowerControl</a>.


#### Examples

To define a <i>PowerControlCallback</i> callback routine, you must first provide a function declaration that identifies the type of callback routine you're defining. Windows provides a set of callback function types for drivers. Declaring a function using the callback function types helps <a href="/windows-hardware/drivers/devtest/code-analysis-for-drivers">Code Analysis for Drivers</a>, <a href="/windows-hardware/drivers/devtest/static-driver-verifier">Static Driver Verifier</a> (SDV), and other verification tools find errors, and it's a requirement for writing drivers for the Windows operating system.

For example, to define a <i>PowerControlCallback</i> callback routine that is named <code>MyPowerControlCallback</code>, use the PO_FX_POWER_CONTROL_CALLBACK type as shown in this code example:


```
PO_FX_POWER_CONTROL_CALLBACK MyPowerControlCallback;
```

Then, implement your callback routine as follows:


```
_Use_decl_annotations_
NTSTATUS
  MyPowerControlCallback(
    PVOID Context,
    LPCGUID PowerControlCode,
    PVOID InBuffer,
    SIZE_T InBufferSize,
    PVOID OutBuffer,
    SIZE_T OutBufferSize,
    PSIZE_T BytesReturned
    )
  {
      // Function body
  }
```

The PO_FX_POWER_CONTROL_CALLBACK function type is defined in the Wdm.h header file. To more accurately identify errors when you run the code analysis tools, be sure to add the _Use_decl_annotations_ annotation to your function definition. The _Use_decl_annotations_ annotation ensures that the annotations that are applied to the PO_FX_POWER_CONTROL_CALLBACK function type in the header file are used. For more information about the requirements for function declarations, see <a href="/windows-hardware/drivers/devtest/declaring-functions-using-function-role-types-for-wdm-drivers">Declaring Functions by Using Function Role Types for WDM Drivers</a>. For information about _Use_decl_annotations_, see <a href="/visualstudio/code-quality/annotating-function-behavior">Annotating Function Behavior</a>.

<div class="code"></div>

## -see-also

<a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_po_fx_device_v1">PO_FX_DEVICE</a>



<a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-pofxpowercontrol">PoFxPowerControl</a>

