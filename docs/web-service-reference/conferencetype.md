---
title: Conferencetype
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConferenceType
api_type:
- schema
ms.assetid: 6bcf6c18-2695-44b1-aabe-dadc52b2633a
description: Das conferencetype-Element beschreibt die Art der Konferenz, die mit einem Kalenderelement durchgeführt wird.
ms.openlocfilehash: 482fc09d709e2b151b255107af59cb98de236aec
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463930"
---
# <a name="conferencetype"></a><span data-ttu-id="8eba0-103">Conferencetype</span><span class="sxs-lookup"><span data-stu-id="8eba0-103">ConferenceType</span></span>

<span data-ttu-id="8eba0-104">Das **conferencetype** -Element beschreibt die Art der Konferenz, die mit einem Kalenderelement durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8eba0-104">The **ConferenceType** element describes the type of conferencing that is performed with a calendar item.</span></span> 
  
```xml
<ConferenceType/>
```

 <span data-ttu-id="8eba0-105">**int**</span><span class="sxs-lookup"><span data-stu-id="8eba0-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8eba0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8eba0-106">Attributes and elements</span></span>

<span data-ttu-id="8eba0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8eba0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8eba0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8eba0-108">Attributes</span></span>

<span data-ttu-id="8eba0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8eba0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8eba0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8eba0-110">Child elements</span></span>

<span data-ttu-id="8eba0-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="8eba0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8eba0-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8eba0-112">Parent elements</span></span>

|<span data-ttu-id="8eba0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="8eba0-113">**Element**</span></span>|<span data-ttu-id="8eba0-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8eba0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8eba0-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="8eba0-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="8eba0-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="8eba0-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="8eba0-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="8eba0-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="8eba0-118">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="8eba0-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8eba0-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="8eba0-119">Text value</span></span>

<span data-ttu-id="8eba0-120">Ein Textwert, der einen ganzzahligen Wert darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8eba0-120">A text value that represents an integer value is required if this element is used.</span></span> <span data-ttu-id="8eba0-121">Im folgenden sind die möglichen Werte für dieses Element angegeben:</span><span class="sxs-lookup"><span data-stu-id="8eba0-121">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="8eba0-122">0 = NetMeeting</span><span class="sxs-lookup"><span data-stu-id="8eba0-122">0 = NetMeeting</span></span>
    
- <span data-ttu-id="8eba0-123">1 = NetShow</span><span class="sxs-lookup"><span data-stu-id="8eba0-123">1 = NetShow</span></span>
    
- <span data-ttu-id="8eba0-124">2 = Chat</span><span class="sxs-lookup"><span data-stu-id="8eba0-124">2 = Chat</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8eba0-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8eba0-125">Remarks</span></span>

<span data-ttu-id="8eba0-126">Die **MeetingWorkspaceUrl** -Eigenschaft ist für das Kalenderelement des Organisators schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8eba0-126">The **MeetingWorkspaceUrl** property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="8eba0-127">Er ist schreibgeschützt für Besprechungsanfragen und Kalenderelemente des Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="8eba0-127">It is read-only for meeting requests and for attendee's calendar items.</span></span> 
  
<span data-ttu-id="8eba0-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="8eba0-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="8eba0-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8eba0-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8eba0-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="8eba0-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8eba0-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8eba0-131">Schema Name</span></span>  <br/> |<span data-ttu-id="8eba0-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8eba0-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="8eba0-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8eba0-133">Validation File</span></span>  <br/> |<span data-ttu-id="8eba0-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8eba0-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8eba0-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8eba0-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="8eba0-136">False</span><span class="sxs-lookup"><span data-stu-id="8eba0-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8eba0-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8eba0-137">See also</span></span>



- [<span data-ttu-id="8eba0-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8eba0-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

