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
description: Das DeliverMeetingRequests-Element definiert, wie Besprechungsanfragen zwischen der Stellvertretung und dem Prinzipal verarbeitet werden. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 3998443613437bca2267678f7bc2c5584b779135
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463678"
---
# <a name="delivermeetingrequests"></a><span data-ttu-id="b27f5-104">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="b27f5-104">DeliverMeetingRequests</span></span>

<span data-ttu-id="b27f5-105">Das **DeliverMeetingRequests** -Element definiert, wie Besprechungsanfragen zwischen der Stellvertretung und dem Prinzipal verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="b27f5-105">The **DeliverMeetingRequests** element defines how meeting requests are handled between the delegate and the principal.</span></span> <span data-ttu-id="b27f5-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b27f5-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```XML
<DeliverMeetingRequests>DelegatesOnly or DelegatesAndMe or DelegatesAndSendInformationToMe or NoForward</DeliverMeetingRequests>
```

 <span data-ttu-id="b27f5-107">**DeliverMeetingRequestsType**</span><span class="sxs-lookup"><span data-stu-id="b27f5-107">**DeliverMeetingRequestsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b27f5-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b27f5-108">Attributes and elements</span></span>

<span data-ttu-id="b27f5-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b27f5-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b27f5-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="b27f5-110">Attributes</span></span>

<span data-ttu-id="b27f5-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b27f5-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b27f5-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b27f5-112">Child elements</span></span>

<span data-ttu-id="b27f5-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b27f5-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b27f5-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b27f5-114">Parent elements</span></span>

|<span data-ttu-id="b27f5-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="b27f5-115">**Element**</span></span>|<span data-ttu-id="b27f5-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b27f5-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b27f5-117">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="b27f5-117">AddDelegate</span></span>](adddelegate.md) <br/> |<span data-ttu-id="b27f5-118">Definiert eine Anforderung zum Hinzufügen von Stellvertretern für ein Postfach.</span><span class="sxs-lookup"><span data-stu-id="b27f5-118">Defines a request to add delegates to a mailbox.</span></span> <span data-ttu-id="b27f5-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b27f5-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="b27f5-120">UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="b27f5-120">UpdateDelegate</span></span>](updatedelegate.md) <br/> |<span data-ttu-id="b27f5-121">Definiert eine Anforderung zum Aktualisieren von Stellvertretern in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="b27f5-121">Defines a request to update delegates in a mailbox.</span></span> <span data-ttu-id="b27f5-122">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b27f5-122">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="b27f5-123">GetDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="b27f5-123">GetDelegateResponse</span></span>](getdelegateresponse.md) <br/> |<span data-ttu-id="b27f5-124">Enthält den Status und das Ergebnis einer getdelegate-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b27f5-124">Contains the status and result of a GetDelegate request.</span></span> <span data-ttu-id="b27f5-125">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b27f5-125">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b27f5-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="b27f5-126">Text value</span></span>

<span data-ttu-id="b27f5-127">In der folgenden Tabelle sind die möglichen Werte für das **DeliverMeetingRequests** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b27f5-127">The following table lists the possible values for the **DeliverMeetingRequests** element.</span></span> 
  
<span data-ttu-id="b27f5-128">**DeliverMeetingRequests-Elementwerte**</span><span class="sxs-lookup"><span data-stu-id="b27f5-128">**DeliverMeetingRequests element values**</span></span>

|<span data-ttu-id="b27f5-129">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b27f5-129">**Value**</span></span>|<span data-ttu-id="b27f5-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b27f5-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b27f5-131">DelegatesOnly</span><span class="sxs-lookup"><span data-stu-id="b27f5-131">DelegatesOnly</span></span>  <br/> |<span data-ttu-id="b27f5-132">Besprechungsanfragen werden an die Stellvertretung weitergeleitet und in den Ordner "Gelöschte Elemente" im Postfach des Prinzipals verschoben.</span><span class="sxs-lookup"><span data-stu-id="b27f5-132">Meeting requests are forwarded to the delegate and moved to the Deleted Items folder in the principal's mailbox.</span></span>  <br/> |
|<span data-ttu-id="b27f5-133">DelegatesAndMe</span><span class="sxs-lookup"><span data-stu-id="b27f5-133">DelegatesAndMe</span></span>  <br/> |<span data-ttu-id="b27f5-134">Besprechungsanfragen werden an die Stellvertretung weitergeleitet und verbleiben im Posteingangsordner im Postfach des Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="b27f5-134">Meeting requests are forwarded to the delegate and remain in the Inbox folder in the principal's mailbox.</span></span>  <br/> |
|<span data-ttu-id="b27f5-135">DelegatesAndSendInformationToMe</span><span class="sxs-lookup"><span data-stu-id="b27f5-135">DelegatesAndSendInformationToMe</span></span>  <br/> |<span data-ttu-id="b27f5-136">Besprechungsanfragen werden an die Stellvertretung weitergeleitet und verbleiben im Posteingangsordner im Postfach des Prinzipals, die Schaltflächen akzeptieren, vorläufig und ablehnen werden im Lesebereich Microsoft Office Outlook nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b27f5-136">Meeting requests are forwarded to the delegate and remain in the Inbox folder in the principal's mailbox, but the Accept, Tentative, and Decline buttons do not appear in the Microsoft Office Outlook reading pane.</span></span>  <br/> |
|<span data-ttu-id="b27f5-137">Noforward</span><span class="sxs-lookup"><span data-stu-id="b27f5-137">NoForward</span></span>  <br/> |<span data-ttu-id="b27f5-138">Besprechungsanfragen werden nicht an die Stellvertretung weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="b27f5-138">Meeting requests are not forwarded to the delegate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b27f5-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b27f5-139">Remarks</span></span>

<span data-ttu-id="b27f5-140">Die **DeliverMeetingRequests** -Einstellung wirkt sich auf alle Delegaten im Postfach eines Prinzipals aus.</span><span class="sxs-lookup"><span data-stu-id="b27f5-140">The **DeliverMeetingRequests** setting affects all delegates in a principal's mailbox.</span></span> 
  
<span data-ttu-id="b27f5-141">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b27f5-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b27f5-142">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b27f5-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b27f5-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="b27f5-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b27f5-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b27f5-144">Schema Name</span></span>  <br/> |<span data-ttu-id="b27f5-145">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b27f5-145">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b27f5-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b27f5-146">Validation File</span></span>  <br/> |<span data-ttu-id="b27f5-147">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b27f5-147">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b27f5-148">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b27f5-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="b27f5-149">False</span><span class="sxs-lookup"><span data-stu-id="b27f5-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b27f5-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b27f5-150">See also</span></span>

- [<span data-ttu-id="b27f5-151">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b27f5-151">AddDelegate operation</span></span>](adddelegate-operation.md)  
- [<span data-ttu-id="b27f5-152">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b27f5-152">UpdateDelegate operation</span></span>](updatedelegate-operation.md)  
- [<span data-ttu-id="b27f5-153">GetDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b27f5-153">GetDelegate operation</span></span>](getdelegate-operation.md)
- [<span data-ttu-id="b27f5-154">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b27f5-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="b27f5-155">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="b27f5-155">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

