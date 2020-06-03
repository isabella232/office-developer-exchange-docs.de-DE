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
description: Das DeliveryStatus-Element gibt den Status einer Nachricht an.
ms.openlocfilehash: ae32202284d3dd272f693fbb7b76070cb6019d28
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461401"
---
# <a name="deliverystatus"></a><span data-ttu-id="4bdd7-103">DeliveryStatus</span><span class="sxs-lookup"><span data-stu-id="4bdd7-103">DeliveryStatus</span></span>

<span data-ttu-id="4bdd7-104">Das **DeliveryStatus** -Element gibt den Status einer Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="4bdd7-104">The **DeliveryStatus** element specifies the status for a message.</span></span> 
  
```XML
<DeliveryStatus>Unsuccessful | Pending | Delivered | Transferred | Read</DeliveryStatus>
```

 <span data-ttu-id="4bdd7-105">**MessageTrackingDeliveryStatusType**</span><span class="sxs-lookup"><span data-stu-id="4bdd7-105">**MessageTrackingDeliveryStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4bdd7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4bdd7-106">Attributes and elements</span></span>

<span data-ttu-id="4bdd7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4bdd7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4bdd7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4bdd7-108">Attributes</span></span>

<span data-ttu-id="4bdd7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4bdd7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4bdd7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4bdd7-110">Child elements</span></span>

<span data-ttu-id="4bdd7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="4bdd7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4bdd7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4bdd7-112">Parent elements</span></span>

|<span data-ttu-id="4bdd7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4bdd7-113">**Element**</span></span>|<span data-ttu-id="4bdd7-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4bdd7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4bdd7-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="4bdd7-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="4bdd7-116">Enthält Informationen zu einem einzelnen Ereignis für einen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="4bdd7-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4bdd7-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="4bdd7-117">Text value</span></span>

<span data-ttu-id="4bdd7-118">In der folgenden Tabelle sind die möglichen Text Werte für das **DeliveryStatus** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4bdd7-118">The following table lists the possible text values for the **DeliveryStatus** element.</span></span> 
  
<span data-ttu-id="4bdd7-119">**DeliveryStatus-Elementwerte**</span><span class="sxs-lookup"><span data-stu-id="4bdd7-119">**DeliveryStatus element values**</span></span>

|<span data-ttu-id="4bdd7-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4bdd7-120">**Value**</span></span>|<span data-ttu-id="4bdd7-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4bdd7-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4bdd7-122">Erfolglos</span><span class="sxs-lookup"><span data-stu-id="4bdd7-122">Unsuccessful</span></span>  <br/> |<span data-ttu-id="4bdd7-123">Gibt an, dass eine Nachricht nicht zugestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4bdd7-123">Specifies that a message was not delivered.</span></span>  <br/> |
|<span data-ttu-id="4bdd7-124">Ausstehend</span><span class="sxs-lookup"><span data-stu-id="4bdd7-124">Pending</span></span>  <br/> |<span data-ttu-id="4bdd7-125">Gibt an, dass die Nachricht von einem Moderator auf die Genehmigung wartet.</span><span class="sxs-lookup"><span data-stu-id="4bdd7-125">Specifies that the message is waiting for approval from a moderator.</span></span>  <br/> |
|<span data-ttu-id="4bdd7-126">Geliefert</span><span class="sxs-lookup"><span data-stu-id="4bdd7-126">Delivered</span></span>  <br/> |<span data-ttu-id="4bdd7-127">Gibt an, dass die Nachricht an alle angegebenen Empfänger übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="4bdd7-127">Specifies that the message was delivered to all of the specified recipients.</span></span>  <br/> |
|<span data-ttu-id="4bdd7-128">Übertragenen</span><span class="sxs-lookup"><span data-stu-id="4bdd7-128">Transferred</span></span>  <br/> |<span data-ttu-id="4bdd7-129">Gibt an, dass die Nachricht an einen Server außerhalb des Suchbereichs übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="4bdd7-129">Specifies that the message was transferred to a server outside the search scope.</span></span>  <br/> |
|<span data-ttu-id="4bdd7-130">Read</span><span class="sxs-lookup"><span data-stu-id="4bdd7-130">Read</span></span>  <br/> |<span data-ttu-id="4bdd7-131">Gibt an, dass die Nachricht von den Empfängern zugestellt und gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="4bdd7-131">Specifies that the message was delivered and read by the recipients.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4bdd7-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4bdd7-132">Remarks</span></span>

<span data-ttu-id="4bdd7-133">Das **DeliveryStatus** -Element war vom Typ **MessageTrackingDeliveryStatusType** in Exchange Server 2010.</span><span class="sxs-lookup"><span data-stu-id="4bdd7-133">The **DeliveryStatus** element was of type **MessageTrackingDeliveryStatusType** in Exchange Server 2010.</span></span> 
  
<span data-ttu-id="4bdd7-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4bdd7-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4bdd7-135">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4bdd7-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4bdd7-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="4bdd7-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4bdd7-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4bdd7-137">Schema Name</span></span>  <br/> |<span data-ttu-id="4bdd7-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4bdd7-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="4bdd7-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4bdd7-139">Validation File</span></span>  <br/> |<span data-ttu-id="4bdd7-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4bdd7-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4bdd7-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4bdd7-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="4bdd7-142">False</span><span class="sxs-lookup"><span data-stu-id="4bdd7-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4bdd7-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bdd7-143">See also</span></span>

- [<span data-ttu-id="4bdd7-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4bdd7-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

