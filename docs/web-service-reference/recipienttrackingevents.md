---
title: RecipientTrackingEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientTrackingEvents
api_type:
- schema
ms.assetid: c4f729aa-674e-43b2-97f2-bf49740b0a34
description: Das RecipientTrackingEvents-Element stellt eine Auflistung von einem oder mehreren Ereignissen für eine Nachricht dar.
ms.openlocfilehash: c0b25a0e22d13bc1f26768b9b7089d96eb2e8cfc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468481"
---
# <a name="recipienttrackingevents"></a><span data-ttu-id="1d002-103">RecipientTrackingEvents</span><span class="sxs-lookup"><span data-stu-id="1d002-103">RecipientTrackingEvents</span></span>

<span data-ttu-id="1d002-104">Das **RecipientTrackingEvents** -Element stellt eine Auflistung von einem oder mehreren Ereignissen für eine Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="1d002-104">The **RecipientTrackingEvents** element represents a collection of one or more events for a message.</span></span> 
  
```XML
<RecipientTrackingEvents>
   <RecipientTrackingEvent/>
</RecipientTrackingEvents>
```

 <span data-ttu-id="1d002-105">**ArrayOfRecipientTrackingEventType**</span><span class="sxs-lookup"><span data-stu-id="1d002-105">**ArrayOfRecipientTrackingEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1d002-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1d002-106">Attributes and elements</span></span>

<span data-ttu-id="1d002-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1d002-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d002-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1d002-108">Attributes</span></span>

<span data-ttu-id="1d002-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1d002-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1d002-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1d002-110">Child elements</span></span>

|<span data-ttu-id="1d002-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1d002-111">**Element**</span></span>|<span data-ttu-id="1d002-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1d002-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d002-113">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="1d002-113">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="1d002-114">Enthält Details für ein bestimmtes Ereignis im Überwachungsbericht.</span><span class="sxs-lookup"><span data-stu-id="1d002-114">Contains details for a specific event in the tracking report.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1d002-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1d002-115">Parent elements</span></span>

|<span data-ttu-id="1d002-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="1d002-116">**Element**</span></span>|<span data-ttu-id="1d002-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1d002-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d002-118">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="1d002-118">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="1d002-119">Enthält eine Nachricht, die in einem [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1d002-119">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d002-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d002-120">Remarks</span></span>

<span data-ttu-id="1d002-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1d002-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d002-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1d002-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d002-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d002-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1d002-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1d002-124">Schema Name</span></span>  <br/> |<span data-ttu-id="1d002-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1d002-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="1d002-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1d002-126">Validation File</span></span>  <br/> |<span data-ttu-id="1d002-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1d002-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1d002-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1d002-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="1d002-129">False</span><span class="sxs-lookup"><span data-stu-id="1d002-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d002-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d002-130">See also</span></span>



[<span data-ttu-id="1d002-131">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1d002-131">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="1d002-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1d002-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

