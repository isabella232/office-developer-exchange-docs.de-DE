---
title: HasBeenProcessed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HasBeenProcessed
api_type:
- schema
ms.assetid: 46d4af8e-0f11-4a74-9365-1d983731fed8
description: Das HasBeenProcessed-Element gibt an, ob ein Besprechungsnachrichten Element verarbeitet wurde.
ms.openlocfilehash: 7251ca86e07a0b72c186c65094b6469331dfd12e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462893"
---
# <a name="hasbeenprocessed"></a><span data-ttu-id="c1e43-103">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="c1e43-103">HasBeenProcessed</span></span>

<span data-ttu-id="c1e43-104">Das **HasBeenProcessed** -Element gibt an, ob ein Besprechungsnachrichten Element verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="c1e43-104">The **HasBeenProcessed** element indicates whether a meeting message item has been processed.</span></span> 
  
```xml
<HasBeenProcessed/>
```

 <span data-ttu-id="c1e43-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="c1e43-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1e43-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c1e43-106">Attributes and elements</span></span>

<span data-ttu-id="c1e43-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c1e43-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1e43-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c1e43-108">Attributes</span></span>

<span data-ttu-id="c1e43-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1e43-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1e43-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1e43-110">Child elements</span></span>

<span data-ttu-id="c1e43-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1e43-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c1e43-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1e43-112">Parent elements</span></span>

|<span data-ttu-id="c1e43-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1e43-113">**Element**</span></span>|<span data-ttu-id="c1e43-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1e43-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1e43-115">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="c1e43-115">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="c1e43-116">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="c1e43-116">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c1e43-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="c1e43-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="c1e43-118">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="c1e43-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c1e43-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="c1e43-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="c1e43-120">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="c1e43-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c1e43-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="c1e43-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="c1e43-122">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="c1e43-122">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c1e43-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="c1e43-123">Text value</span></span>

<span data-ttu-id="c1e43-124">Der Textwert **true** gibt an, dass die Besprechungsnachricht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="c1e43-124">A text value of **true** indicates that the meeting message has been processed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c1e43-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1e43-125">Remarks</span></span>

<span data-ttu-id="c1e43-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c1e43-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1e43-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c1e43-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1e43-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1e43-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c1e43-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c1e43-129">Schema Name</span></span>  <br/> |<span data-ttu-id="c1e43-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c1e43-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="c1e43-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c1e43-131">Validation File</span></span>  <br/> |<span data-ttu-id="c1e43-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c1e43-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c1e43-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c1e43-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1e43-134">False</span><span class="sxs-lookup"><span data-stu-id="c1e43-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1e43-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1e43-135">See also</span></span>



- [<span data-ttu-id="c1e43-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c1e43-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

