---
title: NetShowUrl
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NetShowUrl
api_type:
- schema
ms.assetid: a5d48fc1-b141-422c-bcb0-05d0f9ba90dd
description: NetShowUrl-Element gibt die URL für eine Microsoft NetShow online-Besprechung.
ms.openlocfilehash: 2440e6c1501331d715d0e5ceb31b3b928122f927
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830519"
---
# <a name="netshowurl"></a><span data-ttu-id="b5331-103">NetShowUrl</span><span class="sxs-lookup"><span data-stu-id="b5331-103">NetShowUrl</span></span>

<span data-ttu-id="b5331-104">**NetShowUrl** -Element gibt die URL für eine Microsoft NetShow online-Besprechung.</span><span class="sxs-lookup"><span data-stu-id="b5331-104">The **NetShowUrl** element specifies the URL for a Microsoft NetShow online meeting.</span></span> 
  
```xml
<NetShowUrl/>
```

 <span data-ttu-id="b5331-105">**string**</span><span class="sxs-lookup"><span data-stu-id="b5331-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b5331-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b5331-106">Attributes and elements</span></span>

<span data-ttu-id="b5331-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b5331-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5331-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b5331-108">Attributes</span></span>

<span data-ttu-id="b5331-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5331-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b5331-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5331-110">Child elements</span></span>

<span data-ttu-id="b5331-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5331-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b5331-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5331-112">Parent elements</span></span>

|<span data-ttu-id="b5331-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b5331-113">**Element**</span></span>|<span data-ttu-id="b5331-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b5331-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b5331-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="b5331-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="b5331-116">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="b5331-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b5331-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="b5331-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="b5331-118">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="b5331-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b5331-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="b5331-119">Text value</span></span>

<span data-ttu-id="b5331-120">Ein Textwert, der eine URL darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b5331-120">A text value that represents a URL is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b5331-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b5331-121">Remarks</span></span>

<span data-ttu-id="b5331-122">Diese NetShowUrl-Eigenschaft kann für den Organisator Kalenderelement lesen geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b5331-122">This NetShowUrl property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="b5331-123">Es ist schreibgeschützt, für Besprechungsanfragen und für die Teilnehmer.</span><span class="sxs-lookup"><span data-stu-id="b5331-123">It is read-only for meeting requests and for attendees.</span></span>
  
<span data-ttu-id="b5331-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="b5331-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5331-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b5331-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5331-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5331-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b5331-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b5331-127">Schema name</span></span>  <br/> |<span data-ttu-id="b5331-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b5331-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="b5331-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b5331-129">Validation file</span></span>  <br/> |<span data-ttu-id="b5331-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b5331-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b5331-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b5331-131">Can be empty</span></span>  <br/> |<span data-ttu-id="b5331-132">False</span><span class="sxs-lookup"><span data-stu-id="b5331-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b5331-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5331-133">See also</span></span>



- [<span data-ttu-id="b5331-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b5331-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

