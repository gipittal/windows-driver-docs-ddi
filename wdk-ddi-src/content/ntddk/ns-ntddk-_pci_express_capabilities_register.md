---
UID: NS:ntddk._PCI_EXPRESS_CAPABILITIES_REGISTER
title: _PCI_EXPRESS_CAPABILITIES_REGISTER (ntddk.h)
description: The _PCI_EXPRESS_CAPABILITIES_REGISTER structure (ntddk.h) describes a PCI Express (PCIe) capabilities register of a PCIe capability structure.
old-location: pci\pci_express_capabilities_register.htm
tech.root: PCI
ms.date: 02/24/2018
keywords: ["PCI_EXPRESS_CAPABILITIES_REGISTER structure"]
ms.keywords: "*PPCI_EXPRESS_CAPABILITIES_REGISTER, PCI.pci_express_capabilities_register, PCI_EXPRESS_CAPABILITIES_REGISTER, PCI_EXPRESS_CAPABILITIES_REGISTER union [Buses], PPCI_EXPRESS_CAPABILITIES_REGISTER, PPCI_EXPRESS_CAPABILITIES_REGISTER union pointer [Buses], _PCI_EXPRESS_CAPABILITIES_REGISTER, ntddk/PCI_EXPRESS_CAPABILITIES_REGISTER, ntddk/PPCI_EXPRESS_CAPABILITIES_REGISTER, pci_struct_86cc3b70-4de8-4479-b431-5f7f10d4a2f4.xml"
req.header: ntddk.h
req.include-header: Ntddk.h, Miniport.h
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
req.irql: PASSIVE_LEVEL
targetos: Windows
req.typenames: PCI_EXPRESS_CAPABILITIES_REGISTER, *PPCI_EXPRESS_CAPABILITIES_REGISTER
f1_keywords:
 - _PCI_EXPRESS_CAPABILITIES_REGISTER
 - ntddk/_PCI_EXPRESS_CAPABILITIES_REGISTER
 - PPCI_EXPRESS_CAPABILITIES_REGISTER
 - ntddk/PPCI_EXPRESS_CAPABILITIES_REGISTER
 - PCI_EXPRESS_CAPABILITIES_REGISTER
 - ntddk/PCI_EXPRESS_CAPABILITIES_REGISTER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddk.h
api_name:
 - _PCI_EXPRESS_CAPABILITIES_REGISTER
 - PPCI_EXPRESS_CAPABILITIES_REGISTER
 - PCI_EXPRESS_CAPABILITIES_REGISTER
---

# _PCI_EXPRESS_CAPABILITIES_REGISTER structure (ntddk.h)


## -description

The PCI_EXPRESS_CAPABILITIES_REGISTER structure describes a PCI Express (PCIe) capabilities register of a PCIe capability structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field AsUSHORT

A USHORT representation of the contents of the PCI_EXPRESS_CAPABILITIES_REGISTER structure.


### -field CapabilityVersion

The version number of the <a href="/windows-hardware/drivers/ddi/ntddk/ns-ntddk-_pci_express_capability">PCI_EXPRESS_CAPABILITY</a> structure that contains the PCI_EXPRESS_CAPABILITIES_REGISTER structure.


### -field DeviceType

The type of PCIe logical device. Possible values are:





#### PciExpressEndpoint

A PCIe endpoint device.



#### PciExpressLegacyEndpoint

A legacy PCIe endpoint device.



#### PciExpressRootPort

A root port of a PCIe root complex.



#### PciExpressUpstreamSwitchPort

An upstream port of a PCIe switch.



#### PciExpressDownstreamSwitchPort

A downstream port of a PCIe switch.



#### PciExpressToPciXBridge

A PCIe-to-PCI or PCI-X bridge.



#### PciXToExpressBridge

A PCI- or PCI-X-to PCIe bridge.



#### PciExpressRootComplexIntegratedEndpoint

A PCIe endpoint device that is integrated into the root complex.



#### PciExpressRootComplexEventCollector

A PCIe root complex event collector.


### -field InterruptMessageNumber

The MSI or MSI-X vector that is used for interrupt messages that are generated in association with the status bits in either the slot status register or the root status register of the PCIe capability structure.


### -field Rsvd

Reserved.


### -field SlotImplemented

A single bit that indicates that the PCIe link associated with this port is connected to a physical PCIe slot. This member is valid only if the <b>DeviceType</b> member is set to <b>PciExpressRootPort</b> or <b>PciExpressDownstreamSwitchPort</b>.

## -syntax

```cpp
typedef union _PCI_EXPRESS_CAPABILITIES_REGISTER {
  struct {
    USHORT CapabilityVersion  :4;
    USHORT DeviceType  :4;
    USHORT SlotImplemented  :1;
    USHORT InterruptMessageNumber  :5;
    USHORT Rsvd  :2;
  };
  USHORT AsUSHORT;
} PCI_EXPRESS_CAPABILITIES_REGISTER, *PPCI_EXPRESS_CAPABILITIES_REGISTER;
```

## -remarks

The PCI_EXPRESS_CAPABILITIES_REGISTER structure is available in Windows Server 2008 and later versions of Windows.

A PCI_EXPRESS_CAPABILITIES_REGISTER structure is contained in the <a href="/windows-hardware/drivers/ddi/ntddk/ns-ntddk-_pci_express_capability">PCI_EXPRESS_CAPABILITY</a> structure.

## -see-also

<a href="/windows-hardware/drivers/ddi/ntddk/ns-ntddk-_pci_express_capability">PCI_EXPRESS_CAPABILITY</a>

