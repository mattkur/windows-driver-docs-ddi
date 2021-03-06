---
UID: NE:wwan._WWAN_ACTIVATION_COMMAND
title: _WWAN_ACTIVATION_COMMAND
author: windows-driver-content
description: The WWAN_ACTIVATION_COMMAND enumeration lists the Packet Data Protocol (PDP) activation commands that are supported by the MB device.
old-location: netvista\wwan_activation_command.htm
old-project: netvista
ms.assetid: e9d25ac3-8ffc-4137-8409-731d8caaa730
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: WwanActivationCommandActivate, WwanActivationCommandMax, WWAN_ACTIVATION_COMMAND, _WWAN_ACTIVATION_COMMAND, PWWAN_ACTIVATION_COMMAND, wwan/WWAN_ACTIVATION_COMMAND, WwanRef_55137856-bb05-49ac-b318-cc6922a90445.xml, *PWWAN_ACTIVATION_COMMAND, wwan/WwanActivationCommandMax, netvista.wwan_activation_command, wwan/PWWAN_ACTIVATION_COMMAND, WWAN_ACTIVATION_COMMAND enumeration [Network Drivers Starting with Windows Vista], PWWAN_ACTIVATION_COMMAND enumeration pointer [Network Drivers Starting with Windows Vista], wwan/WwanActivationCommandDeactivate, WwanActivationCommandDeactivate, wwan/WwanActivationCommandActivate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wwan.h
req.include-header: Wwan.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 and later versions of Windows.
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
-	wwan.h
apiname: 
-	WWAN_ACTIVATION_COMMAND
product: Windows
targetos: Windows
req.typenames: *PWWAN_ACTIVATION_COMMAND, WWAN_ACTIVATION_COMMAND
req.product: Windows 10 or later.
---

# _WWAN_ACTIVATION_COMMAND enumeration


## -description


The WWAN_ACTIVATION_COMMAND enumeration lists the Packet Data Protocol (PDP) activation commands that
  are supported by the MB device.


## -syntax


````
typedef enum _WWAN_ACTIVATION_COMMAND { 
  WwanActivationCommandDeactivate  = 0,
  WwanActivationCommandActivate,
  WwanActivationCommandMax
} WWAN_ACTIVATION_COMMAND, *PWWAN_ACTIVATION_COMMAND;
````


## -enum-fields




### -field WwanActivationCommandDeactivate

Deactivate a currently activated PDP context identified by 
     <b>ConnectionId</b> .


### -field WwanActivationCommandActivate

Activate PDP context.


### -field WwanActivationCommandMax

The total number of supported activation commands.


## -see-also

<a href="..\wwan\ns-wwan-_wwan_set_context_state.md">WWAN_SET_CONTEXT_STATE</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20WWAN_ACTIVATION_COMMAND enumeration%20 RELEASE:%20(1/18/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

