---
UID: NC:fwpsk.FWPS_CALLOUT_CLASSIFY_FN1
title: FWPS_CALLOUT_CLASSIFY_FN1
author: windows-driver-content
description: The filter engine calls a callout's classifyFn1 callout function whenever there is data to be processed by the callout.Note  classifyFn1 is the specific version of classifyFn used in Windows 7 and later.
old-location: netvista\classifyfn1.htm
old-project: netvista
ms.assetid: 128fd929-6e83-46a0-9475-e459ede58f30
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: netvista.classifyfn1, classifyFn1 callback function [Network Drivers Starting with Windows Vista], classifyFn1, FWPS_CALLOUT_CLASSIFY_FN1, FWPS_CALLOUT_CLASSIFY_FN1, fwpsk/classifyFn1, wfp_ref_2_funct_4_callout_db29c2d0-9b7c-4737-b66f-472c78fff234.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: fwpsk.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 7.
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
req.irql: <= DISPATCH_LEVEL
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	UserDefined
apilocation: 
-	Fwpsk.h
apiname: 
-	classifyFn1
product: Windows
targetos: Windows
req.typenames: PINSTANCE_PARTIAL_INFORMATION, INSTANCE_PARTIAL_INFORMATION
---

# FWPS_CALLOUT_CLASSIFY_FN1 callback


## -description


The filter engine calls a callout's 
  <i>classifyFn1</i> callout function whenever there is data to be processed by the callout.
<div class="alert"><b>Note</b>  <i>classifyFn1</i> is the specific version of <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> used in Windows 7 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="..\fwpsk\nc-fwpsk-fwps_callout_classify_fn2.md">classifyFn2</a> is available. For Windows Vista, <a href="..\fwpsk\nc-fwpsk-fwps_callout_classify_fn0.md">classifyFn0</a> is available.</div><div> </div>

## -prototype


````
FWPS_CALLOUT_CLASSIFY_FN1 classifyFn1;

void NTAPI classifyFn1(
  _In_     const FWPS_INCOMING_VALUES0          *inFixedValues,
  _In_     const FWPS_INCOMING_METADATA_VALUES0 *inMetaValues,
  _Inout_        void                           *layerData,
  _In_opt_ const void                           *classifyContext,
  _In_     const FWPS_FILTER1                   *filter,
  _In_           UINT64                         flowContext,
  _Inout_        FWPS_CLASSIFY_OUT0             *classifyOut
)
{ ... }
````


## -parameters




### -param *inFixedValues



### -param *inMetaValues



### -param *layerData



### -param *classifyContext



### -param *filter



### -param flowContext [in]

A UINT64-typed variable that contains the context associated with the data flow. If no context is
     associated with the data flow, then this parameter is zero. If the callout is added to the filter engine
     at a filtering layer that does not support data flows, the 
     <i>classifyFn1</i> callout function should ignore this parameter.


### -param *classifyOut






#### - inMetaValues [in]

A pointer to an 
     <mshelp:link keywords="netvista.fwps_incoming_metadata_values0" tabindex="0"><b>
     FWPS_INCOMING_METADATA_VALUES0</b></mshelp:link> structure. This structure contains the values for each of the
     metadata fields in the layer being filtered.


#### - inFixedValues [in]

A pointer to an 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff552401">FWPS_INCOMING_VALUES0</a> structure. This
     structure contains the values for each of the data fields in the layer being filtered.


#### - classifyContext [in, optional]

A pointer to context data associated with the callout driver by the filter engine.


#### - layerData [in, out]

A pointer to a structure that describes the raw data in the layer being filtered. This parameter
     might be <b>NULL</b>, depending on the layer being filtered and the conditions under which the 
     <i>classifyFn1</i> callout function is called. For the stream layer, this parameter points to an 
     <mshelp:link keywords="netvista.fwps_stream_callout_io_packet0" tabindex="0"><b>
     FWPS_STREAM_CALLOUT_IO_PACKET0</b></mshelp:link> structure. For all of the other layers, this parameter points to a 
     <a href="..\ndis\ns-ndis-_net_buffer_list.md">NET_BUFFER_LIST</a> structure if it is not
     <b>NULL</b>.


#### - classifyOut [in, out]

A pointer to an 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff551229">FWPS_CLASSIFY_OUT0</a> structure that
     receives any data that the 
     <i>classifyFn1</i> callout function returns to the caller.


#### - filter [in]

A pointer to an 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff552389">FWPS_FILTER1</a> structure. This structure
     describes the filter that specifies the callout for the filter's action.


## -returns


None.



## -remarks


A callout driver registers a callout's callout functions with the filter engine by calling the 
    <a href="..\fwpsk\nf-fwpsk-fwpscalloutregister1.md">FwpsCalloutRegister1</a> function.

The filter engine calls a callout's 
    <i>classifyFn1</i> callout function with data to be processed whenever all of the test conditions are true
    for a filter in the filter engine that specifies the callout for the filter's action.

A callout's 
    <i>classifyFn1</i> callout function should clear the FWPS_RIGHT_ACTION_WRITE flag in the 
    <b>rights</b> member of the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff551229">FWPS_CLASSIFY_OUT0</a> structure in any of
    the following situations:
<ul>
<li>
When the 
      <i>classifyFn1</i> callout function sets the 
      <b>actionType</b> member of the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/ff551229">FWPS_CLASSIFY_OUT0</a> structure to
      FWP_ACTION_BLOCK.

</li>
<li>
When the 
      <i>classifyFn1</i> callout function sets the 
      <b>actionType</b> member of the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/ff551229">FWPS_CLASSIFY_OUT0</a> structure to
      FWP_ACTION_PERMIT and the FWPS_FILTER_FLAG_CLEAR_ACTION_RIGHT flag is set in the 
      <b>Flags</b> member of the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/ff552389">FWPS_FILTER1</a> structure.

</li>
<li>
When a callout has indicated that it intends to modify the clone net buffer list by setting the 
      <i>intendToModify</i> parameter to <b>TRUE</b> in a call to the 
      <mshelp:link keywords="netvista.fwpsreferencenetbufferlist0" tabindex="0"><b>
      FwpsReferenceNetBufferList0</b></mshelp:link> function.

</li>
</ul>


## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a>

<a href="https://msdn.microsoft.com/a5bade33-e3d1-4e1d-8503-51485097046e">Registering Callouts with the Filter Engine</a>

<a href="..\fwpsk\nc-fwpsk-fwps_callout_classify_fn0.md">classifyFn0</a>

<a href="..\fwpsk\nc-fwpsk-fwps_callout_classify_fn2.md">classifyFn2</a>

<a href="https://msdn.microsoft.com/dec76575-041b-4cbd-8042-184b15354f61">Packet Modification Examples</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff551229">FWPS_CLASSIFY_OUT0</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff552401">FWPS_INCOMING_VALUES0</a>

<a href="https://msdn.microsoft.com/464c74ae-5e37-41f1-b305-ef57039b28ba">Using a Callout for Deep Inspection</a>

<mshelp:link keywords="netvista.fwps_incoming_metadata_values0" tabindex="0"><b>
   FWPS_INCOMING_METADATA_VALUES0</b></mshelp:link>

<a href="..\fwpsk\nf-fwpsk-fwpsreferencenetbufferlist0.md">FwpsReferenceNetBufferList0</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff552389">FWPS_FILTER1</a>

<a href="https://msdn.microsoft.com/1e4f00e0-0fc6-459d-bbdd-02fbca5b9945">Data Logging</a>

<a href="..\fwpsk\nf-fwpsk-fwpscalloutregister1.md">FwpsCalloutRegister1</a>

<mshelp:link keywords="netvista.using_a_callout_for_deep_inspection_of_stream_data" tabindex="0">Using a Callout
    for Deep Inspection of Stream Data</mshelp:link>

<a href="..\ndis\ns-ndis-_net_buffer_list.md">NET_BUFFER_LIST</a>

<a href="https://msdn.microsoft.com/75f5838e-626d-4a59-810e-fec9a40640ed">Associating Context with a Data Flow</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff543875">Callout Driver Callout Functions</a>

<a href="..\fwpsk\ns-fwpsk-fwps_callout0_.md">FWPS_CALLOUT0</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20FWPS_CALLOUT_CLASSIFY_FN1 callback function%20 RELEASE:%20(1/18/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

