---
UID: NS:windot11._DOT11_WFD_CHANNEL
title: _DOT11_WFD_CHANNEL
author: windows-driver-content
description: The DOT11_WFD_CHANNEL structure contains the channel information for a Peer-to-Pear (P2P) group.
old-location: netvista\dot11_wfd_channel.htm
old-project: netvista
ms.assetid: FE05F3D9-B1F0-4DC3-9265-22A76209A3E1
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: DOT11_WFD_CHANNEL structure [Network Drivers Starting with Windows Vista], netvista.dot11_wfd_channel, DOT11_WFD_CHANNEL, windot11/DOT11_WFD_CHANNEL, _DOT11_WFD_CHANNEL, PDOT11_WFD_CHANNEL structure pointer [Network Drivers Starting with Windows Vista], windot11/PDOT11_WFD_CHANNEL, *PDOT11_WFD_CHANNEL, PDOT11_WFD_CHANNEL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: windot11.h
req.include-header: Windot11.h
req.target-type: Windows
req.target-min-winverclnt: Supported starting with   Windows 8.
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
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	Windot11.h
apiname: 
-	DOT11_WFD_CHANNEL
product: Windows
targetos: Windows
req.typenames: DOT11_WFD_CHANNEL, *PDOT11_WFD_CHANNEL
req.product: Windows 10 or later.
---

# _DOT11_WFD_CHANNEL structure


## -description


<div class="alert"><b>Important</b>  The <a href="https://msdn.microsoft.com/library/windows/hardware/ff560689">Native 802.11 Wireless LAN</a> interface is deprecated in Windows 10 and later. Please use the WLAN Device Driver Interface (WDI) instead. For more information about WDI, see <a href="https://msdn.microsoft.com/6EF92E34-7BC9-465E-B05D-2BCB29165A18">WLAN Universal Windows driver model</a>.</div><div> </div>The <b>DOT11_WFD_CHANNEL</b> structure contains the channel information for a Peer-to-Pear (P2P) group.


## -syntax


````
typedef struct _DOT11_WFD_CHANNEL {
  DOT11_COUNTRY_OR_REGION_STRING CountryRegionString;
  UCHAR                          OperatingClass;
  UCHAR                          ChannelNumber;
} DOT11_WFD_CHANNEL, *PDOT11_WFD_CHANNEL;
````


## -struct-fields




### -field CountryRegionString

The country or region code where <b>OperatingClass</b> and <b>ChannelNumber</b> are valid.


### -field OperatingClass

The frequency band for <b>ChannelNumber</b>.


### -field ChannelNumber

The channel number for the P2P group.

