---
UID: NN:filterpipeline.IFixedDocumentSequence
title: IFixedDocumentSequence
author: windows-driver-content
description: The IFixedDocumentSequence interface represents the fixed document sequence for an XPS document.
old-location: print\ifixeddocumentsequence.htm
old-project: print
ms.assetid: 8919e2d1-0c39-46b6-b06e-83fe61f67751
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: print.ifixeddocumentsequence, IFixedDocumentSequence interface [Print Devices], IFixedDocumentSequence interface [Print Devices], described, IFixedDocumentSequence, filterpipeline/IFixedDocumentSequence, filterpipeline_ed0de3e6-e4c7-43e6-a6cf-c16d3a086838.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: filterpipeline.h
req.include-header: Filterpipeline.h
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
req.lib: filterpipeline.h
req.dll: 
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	COM
apilocation: 
-	filterpipeline.h
apiname: 
-	IFixedDocumentSequence
product: Windows
targetos: Windows
req.typenames: EXpsFontRestriction
---

# IFixedDocumentSequence interface


## -description


The <b>IFixedDocumentSequence</b> interface represents the fixed document sequence for an XPS document.


## -members

The <b>IFixedDocumentSequence</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550977">IFixedDocumentSequence::GetPrintTicket</a>
</td>
<td align="left" width="63%">
The <b>GetPrintTicket</b> method gets the print ticket object for the fixed document sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550979">IFixedDocumentSequence::GetUri</a>
</td>
<td align="left" width="63%">
The <b>GetUri</b> method gets the URI of the fixed document sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550987">IFixedDocumentSequence::SetPrintTicket</a>
</td>
<td align="left" width="63%">
The <b>SetPrintTicket</b> method inserts a print ticket into the fixed document sequence.

</td>
</tr>
</table>The <b>GetPrintTicket</b> method gets the print ticket object for the fixed document sequence.

The <b>GetUri</b> method gets the URI of the fixed document sequence.

The <b>SetPrintTicket</b> method inserts a print ticket into the fixed document sequence.

 

