---
UID: NC:wlanihv.DOT11EXT_SEND_PACKET
title: DOT11EXT_SEND_PACKET
author: windows-driver-content
description: Important  The Native 802.11 Wireless LAN interface is deprecated in Windows 10 and later.
old-location: netvista\dot11extsendpacket.htm
old-project: netvista
ms.assetid: 0672eed0-4824-464b-9f4e-93862f27d586
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: netvista.dot11extsendpacket, Dot11ExtSendPacket callback function [Network Drivers Starting with Windows Vista], Dot11ExtSendPacket, DOT11EXT_SEND_PACKET, DOT11EXT_SEND_PACKET, wlanihv/Dot11ExtSendPacket, Native_802.11_IHV_Ext_0acd1763-b9d3-4e75-ada6-63f5a77b42c3.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: wlanihv.h
req.include-header: Wlanihv.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating   systems.
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
-	UserDefined
apilocation: 
-	wlanihv.h
apiname: 
-	Dot11ExtSendPacket
product: Windows
targetos: Windows
req.typenames: *PDRIVER_INFO_8W, *LPDRIVER_INFO_8W, DRIVER_INFO_8W
req.product: Windows 10 or later.
---

# DOT11EXT_SEND_PACKET callback


## -description


<div class="alert"><b>Important</b>  The <a href="https://msdn.microsoft.com/library/windows/hardware/ff560689">Native 802.11 Wireless LAN</a> interface is deprecated in Windows 10 and later. Please use the WLAN Device Driver Interface (WDI) instead. For more information about WDI, see <a href="https://msdn.microsoft.com/6EF92E34-7BC9-465E-B05D-2BCB29165A18">WLAN Universal Windows driver model</a>.</div><div> </div>The IHV Extensions DLL calls the 
  <b>Dot11ExtSendPacket</b> function to transmit a packet through the wireless LAN
  (WLAN) adapter.


## -prototype


````
DWORD WINAPI * Dot11ExtSendPacket(
  _In_opt_ HANDLE hDot11SvcHandle,
  _In_     ULONG  uPacketLen,
  _In_     LPVOID pvPacket,
  _In_opt_ HANDLE hSendCompletion
);
````


## -parameters




### -param hDot11SvcHandle [in, optional]

The handle used by the operating system to reference the WLAN adapter. This handle value was
     specified through a previous call to the 
     <a href="..\wlanihv\nc-wlanihv-dot11extihv_init_adapter.md">Dot11ExtIhvInitAdapter</a> IHV
     Handler function.


### -param uPacketLen [in]

The length, in bytes, of the caller-allocated buffer referenced by the 
     <i>pvPacket</i> parameter.


### -param pvPacket [in]

A pointer to a caller-allocated buffer that contains the data to be transmitted, as described in
     the Remarks section.


### -param hSendCompletion [in, optional]

A handle value that uniquely identifies the send packet. 
     

When the WLAN adapter completes the send operation, the operating system notifies the IHV Extensions
     DLL through a call to the 
     <mshelp:link keywords="netvista.dot11extihvsendpacketcompletion" tabindex="0"><i>
     Dot11ExtIhvSendPacketCompletion</i></mshelp:link> IHV Handler function. When making this call, the operating system
     passes the handle value of the packet through the 
     <i>hSendCompletion</i> parameter.


## -returns


If the call succeeds, the function returns ERROR_SUCCESS. Otherwise, it returns an error code
     defined in 
     Winerror.h.



## -remarks


The IHV Extensions DLL must follow these guidelines when calling the 
    <b>Dot11ExtSendPacket</b> function.
<ul>
<li>
The packet sent through a call of the 
      <b>Dot11ExtSendPacket</b> function will complete asynchronously. The IHV
      Extensions DLL must not free the memory referenced by the 
      <i>pvPacket</i> parameter until the 
      <mshelp:link keywords="netvista.dot11extihvsendpacketcompletion" tabindex="0"><i>
      Dot11ExtIhvSendPacketCompletion</i></mshelp:link> IHV Handler function is called with the same handle value as the 
      <i>hSendCompletion</i> parameter.

</li>
<li>
The IHV Extensions DLL must set the 
      <i>hSendCompletion</i> parameter to a value that uniquely identifies the packet data that is referenced
      by the 
      <i>pvPacket</i> parameter.

</li>
</ul>For more information about the IHV Handler functions, see 
    <mshelp:link keywords="netvista.native_802_11_ihv_handler_functions" tabindex="0">Native 802.11 IHV Handler
    Functions</mshelp:link>.

The buffer pointed to by 
    <i>pvPacket</i> should contain the following packet data, specified in network byte order:
<ul>
<li>
MAC address of destination (6 bytes), formatted according to the guidelines discussed in 
      <mshelp:link keywords="netvista.802_11_mac_header_management" tabindex="0">802.11 MAC Header
      Management</mshelp:link>


</li>
<li>
IEEE EtherType (2 bytes)

</li>
<li>
Payload

</li>
</ul>This packet data is passed to the miniport driver.



## -see-also

<a href="https://technet.microsoft.com/en-us/library/cc757419">802.11 MAC Header Management</a>

<a href="..\wlanihv\nc-wlanihv-dot11extihv_init_adapter.md">Dot11ExtIhvInitAdapter</a>

<mshelp:link keywords="netvista.native_802_11_ihv_handler_functions" tabindex="0">Native 802.11 IHV Handler
   Functions</mshelp:link>

<mshelp:link keywords="netvista.dot11extihvsendpacketcompletion" tabindex="0"><i>
   Dot11ExtIhvSendPacketCompletion</i></mshelp:link>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20DOT11EXT_SEND_PACKET callback function%20 RELEASE:%20(1/18/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

