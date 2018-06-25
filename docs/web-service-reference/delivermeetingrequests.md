---
title: DeliverMeetingRequests
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeliverMeetingRequests
api_type:
- schema
ms.assetid: 04b999af-0b27-4e6d-a8b1-400955a1afaa
description: Das DeliverMeetingRequests-Element definiert, wie Besprechungsanfragen zwischen den Delegaten und dem Prinzipalnamen behandelt werden. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 803bd2da72bdb21b507a59cc11635a40d4431acf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757947"
---
# <a name="delivermeetingrequests"></a><span data-ttu-id="19271-104">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="19271-104">DeliverMeetingRequests</span></span>

<span data-ttu-id="19271-105">Das **DeliverMeetingRequests** -Element definiert, wie Besprechungsanfragen zwischen den Delegaten und dem Prinzipalnamen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="19271-105">The **DeliverMeetingRequests** element defines how meeting requests are handled between the delegate and the principal.</span></span> <span data-ttu-id="19271-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="19271-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```XML
<DeliverMeetingRequests>DelegatesOnly or DelegatesAndMe or DelegatesAndSendInformationToMe or NoForward</DeliverMeetingRequests>
```

 <span data-ttu-id="19271-107">**DeliverMeetingRequestsType**</span><span class="sxs-lookup"><span data-stu-id="19271-107">**DeliverMeetingRequestsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="19271-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="19271-108">Attributes and elements</span></span>

<span data-ttu-id="19271-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="19271-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19271-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="19271-110">Attributes</span></span>

<span data-ttu-id="19271-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="19271-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19271-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="19271-112">Child elements</span></span>

<span data-ttu-id="19271-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="19271-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="19271-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="19271-114">Parent elements</span></span>

|<span data-ttu-id="19271-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="19271-115">**Element**</span></span>|<span data-ttu-id="19271-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="19271-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19271-117">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="19271-117">AddDelegate</span></span>](adddelegate.md) <br/> |<span data-ttu-id="19271-118">Definiert eine Anforderung zum Hinzufügen von Stellvertretern für ein Postfach.</span><span class="sxs-lookup"><span data-stu-id="19271-118">Defines a request to add delegates to a mailbox.</span></span> <span data-ttu-id="19271-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="19271-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="19271-120">UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="19271-120">UpdateDelegate</span></span>](updatedelegate.md) <br/> |<span data-ttu-id="19271-121">Definiert eine Anforderung zum Aktualisieren von Stellvertretern in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="19271-121">Defines a request to update delegates in a mailbox.</span></span> <span data-ttu-id="19271-122">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="19271-122">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="19271-123">GetDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="19271-123">GetDelegateResponse</span></span>](getdelegateresponse.md) <br/> |<span data-ttu-id="19271-124">Enthält den Status und das Ergebnis einer Anforderung GetDelegate.</span><span class="sxs-lookup"><span data-stu-id="19271-124">Contains the status and result of a GetDelegate request.</span></span> <span data-ttu-id="19271-125">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="19271-125">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="19271-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="19271-126">Text value</span></span>

<span data-ttu-id="19271-127">Die folgende Tabelle enthält die möglichen Werte für das **DeliverMeetingRequests** -Element.</span><span class="sxs-lookup"><span data-stu-id="19271-127">The following table lists the possible values for the **DeliverMeetingRequests** element.</span></span> 
  
<span data-ttu-id="19271-128">**DeliverMeetingRequests-Elementwerte**</span><span class="sxs-lookup"><span data-stu-id="19271-128">**DeliverMeetingRequests element values**</span></span>

|<span data-ttu-id="19271-129">**Wert**</span><span class="sxs-lookup"><span data-stu-id="19271-129">**Value**</span></span>|<span data-ttu-id="19271-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="19271-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="19271-131">DelegatesOnly</span><span class="sxs-lookup"><span data-stu-id="19271-131">DelegatesOnly</span></span>  <br/> |<span data-ttu-id="19271-132">Besprechungsanfragen werden an die Stellvertretung weitergeleitet und in den Ordner Gelöschte Elemente im Postfach des Prinzipals verschoben.</span><span class="sxs-lookup"><span data-stu-id="19271-132">Meeting requests are forwarded to the delegate and moved to the Deleted Items folder in the principal's mailbox.</span></span>  <br/> |
|<span data-ttu-id="19271-133">DelegatesAndMe</span><span class="sxs-lookup"><span data-stu-id="19271-133">DelegatesAndMe</span></span>  <br/> |<span data-ttu-id="19271-134">Besprechungsanfragen an die Stellvertretung weitergeleitet werden und im Ordner "Posteingang" im Postfach des Prinzipals bleiben.</span><span class="sxs-lookup"><span data-stu-id="19271-134">Meeting requests are forwarded to the delegate and remain in the Inbox folder in the principal's mailbox.</span></span>  <br/> |
|<span data-ttu-id="19271-135">DelegatesAndSendInformationToMe</span><span class="sxs-lookup"><span data-stu-id="19271-135">DelegatesAndSendInformationToMe</span></span>  <br/> |<span data-ttu-id="19271-136">Besprechungsanfragen an die Stellvertretung weitergeleitet werden und im Ordner "Posteingang" im Postfach des Prinzipals bleiben, aber die Schaltflächen mit Vorbehalt, annehmen und Ablehnen nicht in der Microsoft Office Outlook-Lesebereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="19271-136">Meeting requests are forwarded to the delegate and remain in the Inbox folder in the principal's mailbox, but the Accept, Tentative, and Decline buttons do not appear in the Microsoft Office Outlook reading pane.</span></span>  <br/> |
|<span data-ttu-id="19271-137">NoForward</span><span class="sxs-lookup"><span data-stu-id="19271-137">NoForward</span></span>  <br/> |<span data-ttu-id="19271-138">Besprechungsanfragen werden nicht an die Stellvertretung weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="19271-138">Meeting requests are not forwarded to the delegate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19271-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="19271-139">Remarks</span></span>

<span data-ttu-id="19271-140">Die Einstellung **DeliverMeetingRequests** wirkt sich auf alle Delegaten im Postfach des Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="19271-140">The **DeliverMeetingRequests** setting affects all delegates in a principal's mailbox.</span></span> 
  
<span data-ttu-id="19271-141">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="19271-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="19271-142">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="19271-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19271-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="19271-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="19271-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="19271-144">Schema Name</span></span>  <br/> |<span data-ttu-id="19271-145">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="19271-145">Messages schema</span></span>  <br/> |
|<span data-ttu-id="19271-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="19271-146">Validation File</span></span>  <br/> |<span data-ttu-id="19271-147">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="19271-147">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="19271-148">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="19271-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="19271-149">False</span><span class="sxs-lookup"><span data-stu-id="19271-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="19271-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19271-150">See also</span></span>

- [<span data-ttu-id="19271-151">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="19271-151">AddDelegate operation</span></span>](adddelegate-operation.md)  
- [<span data-ttu-id="19271-152">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="19271-152">UpdateDelegate operation</span></span>](updatedelegate-operation.md)  
- [<span data-ttu-id="19271-153">GetDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="19271-153">GetDelegate operation</span></span>](getdelegate-operation.md)
- [<span data-ttu-id="19271-154">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="19271-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="19271-155">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="19271-155">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

