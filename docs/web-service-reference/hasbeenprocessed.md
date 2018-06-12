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
description: Das HasBeenProcessed-Element gibt an, ob eine Besprechungsnachricht Element verarbeitet wurde.
ms.openlocfilehash: cccd3b2258490fcbe902bcd391f25b0be2fe7c26
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829796"
---
# <a name="hasbeenprocessed"></a><span data-ttu-id="977c8-103">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="977c8-103">HasBeenProcessed</span></span>

<span data-ttu-id="977c8-104">Das **HasBeenProcessed** -Element gibt an, ob eine Besprechungsnachricht Element verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="977c8-104">The **HasBeenProcessed** element indicates whether a meeting message item has been processed.</span></span> 
  
```xml
<HasBeenProcessed/>
```

 <span data-ttu-id="977c8-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="977c8-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="977c8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="977c8-106">Attributes and elements</span></span>

<span data-ttu-id="977c8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="977c8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="977c8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="977c8-108">Attributes</span></span>

<span data-ttu-id="977c8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="977c8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="977c8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="977c8-110">Child elements</span></span>

<span data-ttu-id="977c8-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="977c8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="977c8-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="977c8-112">Parent elements</span></span>

|<span data-ttu-id="977c8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="977c8-113">**Element**</span></span>|<span data-ttu-id="977c8-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="977c8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="977c8-115">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="977c8-115">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="977c8-116">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="977c8-116">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="977c8-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="977c8-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="977c8-118">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="977c8-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="977c8-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="977c8-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="977c8-120">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="977c8-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="977c8-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="977c8-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="977c8-122">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="977c8-122">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="977c8-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="977c8-123">Text value</span></span>

<span data-ttu-id="977c8-124">Der Textwert **true** gibt an, dass die Besprechungsnachricht verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="977c8-124">A text value of **true** indicates that the meeting message has been processed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="977c8-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="977c8-125">Remarks</span></span>

<span data-ttu-id="977c8-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="977c8-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="977c8-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="977c8-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="977c8-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="977c8-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="977c8-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="977c8-129">Schema Name</span></span>  <br/> |<span data-ttu-id="977c8-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="977c8-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="977c8-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="977c8-131">Validation File</span></span>  <br/> |<span data-ttu-id="977c8-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="977c8-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="977c8-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="977c8-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="977c8-134">False</span><span class="sxs-lookup"><span data-stu-id="977c8-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="977c8-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="977c8-135">See also</span></span>



- [<span data-ttu-id="977c8-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="977c8-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

