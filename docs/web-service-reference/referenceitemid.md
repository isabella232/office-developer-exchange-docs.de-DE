---
title: ReferenceItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReferenceItemId
api_type:
- schema
ms.assetid: 8fd4bb12-a94b-43f5-be3b-f435684e311d
description: Das ReferenceItemId-Element identifiziert das Element auf dem im Response-Objekt verweist.
ms.openlocfilehash: d29f2dfec8f2c23fe0ac8c84d2bb9029fce613d2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831032"
---
# <a name="referenceitemid"></a><span data-ttu-id="b5b6d-103">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="b5b6d-103">ReferenceItemId</span></span>

<span data-ttu-id="b5b6d-104">Das **ReferenceItemId** -Element identifiziert das Element auf dem im Response-Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="b5b6d-104">The **ReferenceItemId** element identifies the item to which the response object refers.</span></span> 
  
```xml
<ReferenceItemId Id="" ChangeKey="" />
```

 <span data-ttu-id="b5b6d-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="b5b6d-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b5b6d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b5b6d-106">Attributes and elements</span></span>

<span data-ttu-id="b5b6d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b5b6d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5b6d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b5b6d-108">Attributes</span></span>

|<span data-ttu-id="b5b6d-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b5b6d-109">**Attribute**</span></span>|<span data-ttu-id="b5b6d-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b5b6d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b5b6d-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="b5b6d-111">**Id**</span></span> <br/> |<span data-ttu-id="b5b6d-112">Gibt ein bestimmtes Element in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="b5b6d-112">Identifies a specific item in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="b5b6d-113">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="b5b6d-113">**ChangeKey**</span></span> <br/> |<span data-ttu-id="b5b6d-114">Identifiziert eine bestimmte Version eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="b5b6d-114">Identifies a specific version of an item.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b5b6d-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5b6d-115">Child elements</span></span>

<span data-ttu-id="b5b6d-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5b6d-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b5b6d-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5b6d-117">Parent elements</span></span>

|<span data-ttu-id="b5b6d-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="b5b6d-118">**Element**</span></span>|<span data-ttu-id="b5b6d-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b5b6d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b5b6d-120">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="b5b6d-120">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="b5b6d-121">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="b5b6d-121">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="b5b6d-122">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="b5b6d-122">AcceptSharingInvitation</span></span>](acceptsharinginvitation.md) <br/> |<span data-ttu-id="b5b6d-123">Stellt eine Accept-Antwort auf eine freigabeeinladung dar.</span><span class="sxs-lookup"><span data-stu-id="b5b6d-123">Represents an Accept reply to a sharing invitation.</span></span>  <br/> |
|[<span data-ttu-id="b5b6d-124">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="b5b6d-124">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="b5b6d-125">Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b5b6d-125">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="b5b6d-126">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="b5b6d-126">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="b5b6d-127">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="b5b6d-127">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="b5b6d-128">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="b5b6d-128">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="b5b6d-129">Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="b5b6d-129">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="b5b6d-130">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="b5b6d-130">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="b5b6d-131">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="b5b6d-131">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b5b6d-132">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="b5b6d-132">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="b5b6d-133">Enthält eine Antwort an alle identifizierten Empfänger eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="b5b6d-133">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b5b6d-134">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="b5b6d-134">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="b5b6d-135">Enthält eine Antwort an den Ersteller eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="b5b6d-135">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b5b6d-136">SuppressReadReceipt</span><span class="sxs-lookup"><span data-stu-id="b5b6d-136">SuppressReadReceipt</span></span>](suppressreadreceipt.md) <br/> |<span data-ttu-id="b5b6d-137">Verwendet, um zum Lesen von bestätigungsanforderungen reagieren.</span><span class="sxs-lookup"><span data-stu-id="b5b6d-137">Used to respond to read receipt requests.</span></span>  <br/> |
|[<span data-ttu-id="b5b6d-138">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="b5b6d-138">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="b5b6d-139">Stellt eine mit Vorbehalt Antworten auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="b5b6d-139">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5b6d-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b5b6d-140">Remarks</span></span>

<span data-ttu-id="b5b6d-141">Das Schema, das dieses Element beschreibt befindet sich das virtuelle IIS-Verzeichnis, dass Hosts Exchange-Webdienste des Computers, auf dem Microsoft Exchange Server ausgeführt wird die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b5b6d-141">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5b6d-142">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b5b6d-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5b6d-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5b6d-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b5b6d-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b5b6d-144">Schema Name</span></span>  <br/> |<span data-ttu-id="b5b6d-145">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b5b6d-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="b5b6d-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b5b6d-146">Validation File</span></span>  <br/> |<span data-ttu-id="b5b6d-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b5b6d-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b5b6d-148">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b5b6d-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="b5b6d-149">False</span><span class="sxs-lookup"><span data-stu-id="b5b6d-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b5b6d-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5b6d-150">See also</span></span>



- [<span data-ttu-id="b5b6d-151">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b5b6d-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

