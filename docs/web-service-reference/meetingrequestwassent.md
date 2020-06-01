---
title: MeetingRequestWasSent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingRequestWasSent
api_type:
- schema
ms.assetid: 9192400a-8eef-4147-9f94-aa8ea91b41d8
description: Das MeetingRequestWasSent-Element gibt an, ob eine Besprechungsanfrage an angeforderte Teilnehmer gesendet wurde.
ms.openlocfilehash: d5005eb86d5f8d2f438a69e634f0617c2311d720
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44465765"
---
# <a name="meetingrequestwassent"></a><span data-ttu-id="e9156-103">MeetingRequestWasSent</span><span class="sxs-lookup"><span data-stu-id="e9156-103">MeetingRequestWasSent</span></span>

<span data-ttu-id="e9156-104">Das **MeetingRequestWasSent** -Element gibt an, ob eine Besprechungsanfrage an angeforderte Teilnehmer gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e9156-104">The **MeetingRequestWasSent** element indicates whether a meeting request has been sent to requested attendees.</span></span> 
  
```xml
<MeetingRequestWasSent/>
```

 <span data-ttu-id="e9156-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="e9156-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e9156-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e9156-106">Attributes and elements</span></span>

<span data-ttu-id="e9156-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e9156-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e9156-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e9156-108">Attributes</span></span>

<span data-ttu-id="e9156-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e9156-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e9156-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e9156-110">Child elements</span></span>

<span data-ttu-id="e9156-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e9156-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e9156-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e9156-112">Parent elements</span></span>

|<span data-ttu-id="e9156-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e9156-113">**Element**</span></span>|<span data-ttu-id="e9156-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e9156-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e9156-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="e9156-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="e9156-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="e9156-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e9156-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="e9156-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="e9156-118">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="e9156-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e9156-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="e9156-119">Text value</span></span>

<span data-ttu-id="e9156-120">Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich, wenn dieses Element enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e9156-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="e9156-121">Der Wert **true** gibt an, dass eine Besprechungsanfrage gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e9156-121">A value of **true** indicates that a meeting request was sent.</span></span> <span data-ttu-id="e9156-122">Der Wert **false** gibt an, dass keine Besprechungsanfrage gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e9156-122">A value of **false** indicates that a meeting request has not been sent.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e9156-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9156-123">Remarks</span></span>

<span data-ttu-id="e9156-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e9156-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e9156-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e9156-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e9156-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="e9156-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e9156-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e9156-127">Schema name</span></span>  <br/> |<span data-ttu-id="e9156-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e9156-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="e9156-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e9156-129">Validation file</span></span>  <br/> |<span data-ttu-id="e9156-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e9156-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e9156-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e9156-131">Can be empty</span></span>  <br/> |<span data-ttu-id="e9156-132">False</span><span class="sxs-lookup"><span data-stu-id="e9156-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e9156-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9156-133">See also</span></span>



- [<span data-ttu-id="e9156-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e9156-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

