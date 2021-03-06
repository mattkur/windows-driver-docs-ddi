---
UID: NE:wditypes._WDI_EXEMPTION_PACKET_TYPE
title: _WDI_EXEMPTION_PACKET_TYPE
author: windows-driver-content
description: The WDI_EXEMPTION_PACKET_TYPE enumeration defines the types of packet exemptions.
old-location: netvista\wdi_exemption_packet_type.htm
old-project: netvista
ms.assetid: 7F584EBE-9ACB-4AC7-9472-34322F24EF74
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: WDI_EXEMPT_PACKET_TYPE_UNICAST, WDI_EXEMPTION_PACKET_TYPE, WDI_EXEMPTION_PACKET_TYPE enumeration [Device and Driver Installation], wditypes/WDI_EXEMPTION_PACKET_TYPE, netvista.wdi_exemption_packet_type, WDI_EXEMPT_PACKET_TYPE_MULTICAST, wditypes/WDI_EXEMPT_PACKET_TYPE_UNICAST, wditypes/WDI_EXEMPT_PACKET_TYPE_MULTICAST, netvista.wifi_exemption_packet_type, WDI_EXEMPT_PACKET_TYPE_BOTH, wditypes/WDI_EXEMPT_PACKET_TYPE_BOTH, _WDI_EXEMPTION_PACKET_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wditypes.hpp
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	wditypes.hpp
apiname: 
-	WDI_EXEMPTION_PACKET_TYPE
product: Windows
targetos: Windows
req.typenames: WDI_EXEMPTION_PACKET_TYPE
req.product: Windows 10 or later.
---

# _WDI_EXEMPTION_PACKET_TYPE enumeration


## -description


The WDI_EXEMPTION_PACKET_TYPE enumeration defines the types of packet exemptions.


## -syntax


````
typedef enum _WDI_EXEMPTION_PACKET_TYPE { 
  WDI_EXEMPT_PACKET_TYPE_UNICAST    = 1,
  WDI_EXEMPT_PACKET_TYPE_MULTICAST  = 2,
  WDI_EXEMPT_PACKET_TYPE_BOTH       = 3
} WDI_EXEMPTION_PACKET_TYPE;
````


## -enum-fields




### -field WDI_EXEMPT_PACKET_TYPE_UNICAST

Exempt unicast packets only.


### -field WDI_EXEMPT_PACKET_TYPE_MULTICAST

Exempt multicast and broadcast packets only.


### -field WDI_EXEMPT_PACKET_TYPE_BOTH

Exempt all packet types.

