---
title: DeliveryStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeliveryStatus
api_type:
- schema
ms.assetid: eab55db3-affb-42be-a586-5caa04052433
description: Das DeliveryStatus-Element gibt den Status für eine Nachricht an.
ms.openlocfilehash: 4e6f31e8ef4f98d8e838ba91167c7dd5d6ab2590
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757948"
---
# <a name="deliverystatus"></a><span data-ttu-id="90735-103">DeliveryStatus</span><span class="sxs-lookup"><span data-stu-id="90735-103">DeliveryStatus</span></span>

<span data-ttu-id="90735-104">Das **DeliveryStatus** -Element gibt den Status für eine Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="90735-104">The **DeliveryStatus** element specifies the status for a message.</span></span> 
  
```XML
<DeliveryStatus>Unsuccessful | Pending | Delivered | Transferred | Read</DeliveryStatus>
```

 <span data-ttu-id="90735-105">**MessageTrackingDeliveryStatusType**</span><span class="sxs-lookup"><span data-stu-id="90735-105">**MessageTrackingDeliveryStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="90735-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="90735-106">Attributes and elements</span></span>

<span data-ttu-id="90735-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="90735-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="90735-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="90735-108">Attributes</span></span>

<span data-ttu-id="90735-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="90735-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="90735-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="90735-110">Child elements</span></span>

<span data-ttu-id="90735-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="90735-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="90735-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="90735-112">Parent elements</span></span>

|<span data-ttu-id="90735-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="90735-113">**Element**</span></span>|<span data-ttu-id="90735-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="90735-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90735-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="90735-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="90735-116">Enthält Informationen für ein einzelnes Ereignis für einen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="90735-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="90735-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="90735-117">Text value</span></span>

<span data-ttu-id="90735-118">Die folgende Tabelle enthält die möglichen Textwerte für das **DeliveryStatus** -Element.</span><span class="sxs-lookup"><span data-stu-id="90735-118">The following table lists the possible text values for the **DeliveryStatus** element.</span></span> 
  
<span data-ttu-id="90735-119">**DeliveryStatus-Elementwerte**</span><span class="sxs-lookup"><span data-stu-id="90735-119">**DeliveryStatus element values**</span></span>

|<span data-ttu-id="90735-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="90735-120">**Value**</span></span>|<span data-ttu-id="90735-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="90735-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90735-122">Nicht erfolgreich</span><span class="sxs-lookup"><span data-stu-id="90735-122">Unsuccessful</span></span>  <br/> |<span data-ttu-id="90735-123">Gibt an, dass eine Nachricht nicht übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="90735-123">Specifies that a message was not delivered.</span></span>  <br/> |
|<span data-ttu-id="90735-124">Ausstehende</span><span class="sxs-lookup"><span data-stu-id="90735-124">Pending</span></span>  <br/> |<span data-ttu-id="90735-125">Gibt an, dass die Nachricht zur Genehmigung von einen Moderator wartet.</span><span class="sxs-lookup"><span data-stu-id="90735-125">Specifies that the message is waiting for approval from a moderator.</span></span>  <br/> |
|<span data-ttu-id="90735-126">Übermittelt</span><span class="sxs-lookup"><span data-stu-id="90735-126">Delivered</span></span>  <br/> |<span data-ttu-id="90735-127">Gibt an, dass die Nachricht an alle der angegebenen Empfänger gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="90735-127">Specifies that the message was delivered to all of the specified recipients.</span></span>  <br/> |
|<span data-ttu-id="90735-128">Übertragen</span><span class="sxs-lookup"><span data-stu-id="90735-128">Transferred</span></span>  <br/> |<span data-ttu-id="90735-129">Gibt an, dass die Nachricht an einen Server außerhalb der Suchbereich übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="90735-129">Specifies that the message was transferred to a server outside the search scope.</span></span>  <br/> |
|<span data-ttu-id="90735-130">Lesen</span><span class="sxs-lookup"><span data-stu-id="90735-130">Read</span></span>  <br/> |<span data-ttu-id="90735-131">Gibt an, dass die Nachricht übermittelt und vom Empfänger gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="90735-131">Specifies that the message was delivered and read by the recipients.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90735-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="90735-132">Remarks</span></span>

<span data-ttu-id="90735-133">Das **DeliveryStatus** -Element wurde vom Typ **MessageTrackingDeliveryStatusType** in Exchange Server 2010.</span><span class="sxs-lookup"><span data-stu-id="90735-133">The **DeliveryStatus** element was of type **MessageTrackingDeliveryStatusType** in Exchange Server 2010.</span></span> 
  
<span data-ttu-id="90735-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="90735-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="90735-135">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="90735-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="90735-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="90735-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="90735-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="90735-137">Schema Name</span></span>  <br/> |<span data-ttu-id="90735-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="90735-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="90735-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="90735-139">Validation File</span></span>  <br/> |<span data-ttu-id="90735-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="90735-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="90735-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="90735-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="90735-142">False</span><span class="sxs-lookup"><span data-stu-id="90735-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="90735-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90735-143">See also</span></span>

- [<span data-ttu-id="90735-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="90735-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

