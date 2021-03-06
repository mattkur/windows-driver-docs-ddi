---
UID: NN:portcls.IPortWaveRTStream
title: IPortWaveRTStream
author: windows-driver-content
description: The IPortWaveRTStream interface is supported in Windows Vista and later operating systems, and it is a stream-specific interface that provides helper methods for use by the WaveRT miniport driver.
old-location: audio\iportwavertstream.htm
old-project: audio
ms.assetid: ca5039ff-d34a-4a61-b288-64f0c1f31b91
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: audio.iportwavertstream, IPortWaveRTStream interface [Audio Devices], IPortWaveRTStream interface [Audio Devices], described, IPortWaveRTStream, portcls/IPortWaveRTStream, audmp-routines_485f04fa-bdd1-4b92-bb3b-4f8653393811.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: portcls.h
req.include-header: 
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
req.lib: Portcls.lib
req.dll: 
req.irql: PASSIVE_LEVEL
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	COM
apilocation: 
-	portcls.h
apiname: 
-	IPortWaveRTStream
product: Windows
targetos: Windows
req.typenames: PC_EXIT_LATENCY, *PPC_EXIT_LATENCY
---

# IPortWaveRTStream interface


## -description


The <code>IPortWaveRTStream</code> interface is supported in Windows Vista and later operating systems, and it is a stream-specific interface that provides helper methods for use by the <a href="https://msdn.microsoft.com/154dc921-424f-4021-8f17-5482ceef99a8">WaveRT miniport driver</a>. The miniport driver calls the methods to perform allocation and mapping of cyclic buffers for audio data. The WaveRT port driver implements this interface. The port driver gives an <code>IPortWaveRTStream</code> object reference to each miniport driver stream object that it creates. <code>IPortWaveRTStream</code> inherits from the <b>IUnknown</b> interface.

An audio stream is associated with each pin instance on a WaveRT filter. The adapter driver forms the filter by binding the WaveRT port and miniport drivers. When the port driver calls the <a href="https://msdn.microsoft.com/efd2eea8-2b05-49a2-b136-a3e1e3e739c5">IMiniportWaveRT::NewStream </a> method to create the miniport driver stream object, the port driver passes an <code>IPortWaveRTStream</code> reference as one of the method's call parameters.

To allocate the memory needed for the cyclic buffer, the miniport driver must call the <a href="https://msdn.microsoft.com/44839b9e-f206-49e6-a9f6-14e79d1e0ae2">AllocatePagesForMdl</a> method or the <a href="https://msdn.microsoft.com/976f7e83-9b2a-4e1b-ab76-76d8e9711bff">AllocateContiguousPagesForMdl</a> method of the <code>IPortWaveRTStream</code> interface. The interface provides additional methods that can map the allocated pages, unmap them, and can also free them.

The methods in the <code>IPortWaveRTStream</code> interface are based on, and are similar to, the MmXxx kernel functions that perform allocation and mapping of memory descriptor lists (<a href="..\wdm\ns-wdm-_mdl.md">MDLs</a>). However, the MmXxx functions cannot be used in place of the <code>IPortWaveRTStream</code> methods. 


## -members

The <b>IPortWaveRTStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536924">IPortWaveRTStream::AllocateContiguousPagesForMdl</a>
</td>
<td align="left" width="63%">
The <code>AllocateContiguousPagesForMdl</code> method allocates a list of contiguous, nonpaged, physical memory pages and returns a pointer to a memory descriptor list (<a href="..\wdm\ns-wdm-_mdl.md">MDL</a>) that describes them.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536925">IPortWaveRTStream::AllocatePagesForMdl</a>
</td>
<td align="left" width="63%">
The <code>AllocatePagesForMdl</code> method allocates a list of nonpaged physical memory pages and returns a pointer to a memory descriptor list (<a href="..\wdm\ns-wdm-_mdl.md">MDL</a>) that describes them.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536926">IPortWaveRTStream::FreePagesFromMdl</a>
</td>
<td align="left" width="63%">
The <code>FreePagesFromMdl</code> method frees a memory descriptor list (<a href="..\wdm\ns-wdm-_mdl.md">MDL</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536928">IPortWaveRTStream::GetPhysicalPageAddress</a>
</td>
<td align="left" width="63%">
The <code>GetPhysicalPageAddress</code> method returns the physical address for a page within a memory descriptor list (<a href="..\wdm\ns-wdm-_mdl.md">MDL</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536930">IPortWaveRTStream::GetPhysicalPagesCount</a>
</td>
<td align="left" width="63%">
The <code>GetPhysicalPagesCount</code> method returns the count of the physical pages in a memory descriptor list (<a href="..\wdm\ns-wdm-_mdl.md">MDL</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536932">IPortWaveRTStream::MapAllocatedPages</a>
</td>
<td align="left" width="63%">
The <code>MapAllocatedPages</code> method maps a list of previously allocated physical pages into a contiguous block of virtual memory that is accessible from kernel-mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536934">IPortWaveRTStream::UnmapAllocatedPages</a>
</td>
<td align="left" width="63%">
The <code>UnmapAllocatedPages</code> method releases a mapping.

</td>
</tr>
</table>The <code>AllocateContiguousPagesForMdl</code> method allocates a list of contiguous, nonpaged, physical memory pages and returns a pointer to a memory descriptor list (<a href="..\wdm\ns-wdm-_mdl.md">MDL</a>) that describes them.

The <code>AllocatePagesForMdl</code> method allocates a list of nonpaged physical memory pages and returns a pointer to a memory descriptor list (<a href="..\wdm\ns-wdm-_mdl.md">MDL</a>) that describes them.

The <code>FreePagesFromMdl</code> method frees a memory descriptor list (<a href="..\wdm\ns-wdm-_mdl.md">MDL</a>).

The <code>GetPhysicalPageAddress</code> method returns the physical address for a page within a memory descriptor list (<a href="..\wdm\ns-wdm-_mdl.md">MDL</a>).

The <code>GetPhysicalPagesCount</code> method returns the count of the physical pages in a memory descriptor list (<a href="..\wdm\ns-wdm-_mdl.md">MDL</a>).

The <code>MapAllocatedPages</code> method maps a list of previously allocated physical pages into a contiguous block of virtual memory that is accessible from kernel-mode.

The <code>UnmapAllocatedPages</code> method releases a mapping.

 

