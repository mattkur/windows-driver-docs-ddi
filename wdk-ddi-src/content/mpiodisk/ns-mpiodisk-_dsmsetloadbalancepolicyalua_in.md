---
UID: NS:mpiodisk._DsmSetLoadBalancePolicyALUA_IN
title: _DsmSetLoadBalancePolicyALUA_IN
author: windows-driver-content
description: The DsmSetLoadBalancePolicyALUA_IN structure provides the input parameter for the DsmSetLoadBalancePolicyALUA method.
old-location: storage\dsmsetloadbalancepolicyalua_in.htm
old-project: storage
ms.assetid: d46cfba0-a749-436a-99ad-d3606aea9a4d
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: mpiodisk/DsmSetLoadBalancePolicyALUA_IN, mpiodisk/PDsmSetLoadBalancePolicyALUA_IN, PDsmSetLoadBalancePolicyALUA_IN structure pointer [Storage Devices], *PDsmSetLoadBalancePolicyALUA_IN, storage.dsmsetloadbalancepolicyalua_in, _DsmSetLoadBalancePolicyALUA_IN, structs-scsibus_898bd48b-e522-4a78-ac0a-a7ae10d0c1d0.xml, DsmSetLoadBalancePolicyALUA_IN structure [Storage Devices], PDsmSetLoadBalancePolicyALUA_IN, DsmSetLoadBalancePolicyALUA_IN
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mpiodisk.h
req.include-header: Mpiowmi.h
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
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	mpiodisk.h
apiname: 
-	DsmSetLoadBalancePolicyALUA_IN
product: Windows
targetos: Windows
req.typenames: DsmSetLoadBalancePolicyALUA_IN, *PDsmSetLoadBalancePolicyALUA_IN
---

# _DsmSetLoadBalancePolicyALUA_IN structure


## -description


The DsmSetLoadBalancePolicyALUA_IN structure provides the input parameter for the DsmSetLoadBalancePolicyALUA method.


## -syntax


````
typedef struct _DsmSetLoadBalancePolicyALUA_IN {
  DSM_Load_Balance_Policy_V2 LoadBalancePolicy;
} DsmSetLoadBalancePolicyALUA_IN, *PDsmSetLoadBalancePolicyALUA_IN;
````


## -struct-fields




### -field LoadBalancePolicy

A structure of type DSM_Load_Balance_Policy_V2.

