---
UID: NF:wiamdef.wiasValidateItemProperties
title: wiasValidateItemProperties function
author: windows-driver-content
description: The wiasValidateItemProperties function validates a list of simple item properties against their current valid values.
old-location: image\wiasvalidateitemproperties.htm
old-project: image
ms.assetid: d7858b1b-88cf-4e75-a466-40afdcb01d9b
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: wiasFncs_98dc1f86-1cba-43c0-9f2a-3598701439bc.xml, wiamdef/wiasValidateItemProperties, image.wiasvalidateitemproperties, wiasValidateItemProperties function [Imaging Devices], wiasValidateItemProperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wiamdef.h
req.include-header: Wiamdef.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows Me and in Windows XP and later versions of the Windows operating systems.
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
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	DllExport
apilocation: 
-	Wiaservc.dll
apiname: 
-	wiasValidateItemProperties
product: Windows
targetos: Windows
req.typenames: DEVICEDIALOGDATA2, *PDEVICEDIALOGDATA2, *LPDEVICEDIALOGDATA2
req.product: Windows 10 or later.
---

# wiasValidateItemProperties function


## -description


The <b>wiasValidateItemProperties </b>function validates a list of simple item properties against their current valid values.


## -syntax


````
HRESULT _stdcall wiasValidateItemProperties(
  _In_       BYTE     *pWiasContext,
             ULONG    nPropSpec,
  _In_ const PROPSPEC *pPropSpec
);
````


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param nPropSpec

Specifies the number of properties to validate.


### -param pPropSpec [in]

Pointer to the first element of an array of PROPSPEC structures indicating the properties to validate.


## -returns


On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).



## -remarks


This function validates simple property values of the following types grouped by attribute.
<table>
<tr>
<th>Attributes</th>
<th>Supported Types</th>
</tr>
<tr>
<td>
WIA_PROP_FLAG

</td>
<td>
VT_UI1, VT_UI2, VT_UI4, VT_UI8, VT_I1, VT_I2, VT_I4

</td>
</tr>
<tr>
<td>
WIA_PROP_RANGE

</td>
<td>
VT_UI1, VT_UI2, VT_UI4, VT_UI8, VT_I1, VT_I2, VT_I4, VT_R4, VT_R8

</td>
</tr>
<tr>
<td>
WIA_PROP_LIST

</td>
<td>
VT_UI1, VT_UI2, VT_UI4, VT_UI8, VT_I1, VT_I2, VT_I4, VT_R4, VT_R8, VT_BSTR

</td>
</tr>
</table> 

The PROPSPEC structure is defined in the Windows SDK documentation.


