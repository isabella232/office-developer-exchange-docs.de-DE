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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463930"
---
# <a name="conferencetype"></a><span data-ttu-id="9bf55-103">Conferencetype</span><span class="sxs-lookup"><span data-stu-id="9bf55-103">ConferenceType</span></span>

<span data-ttu-id="9bf55-104">Das **conferencetype** -Element beschreibt die Art der Konferenz, die mit einem Kalenderelement durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9bf55-104">The **ConferenceType** element describes the type of conferencing that is performed with a calendar item.</span></span> 
  
```xml
<ConferenceType/>
```

 <span data-ttu-id="9bf55-105">**int**</span><span class="sxs-lookup"><span data-stu-id="9bf55-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9bf55-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9bf55-106">Attributes and elements</span></span>

<span data-ttu-id="9bf55-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9bf55-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9bf55-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9bf55-108">Attributes</span></span>

<span data-ttu-id="9bf55-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9bf55-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9bf55-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9bf55-110">Child elements</span></span>

<span data-ttu-id="9bf55-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="9bf55-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9bf55-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9bf55-112">Parent elements</span></span>

|<span data-ttu-id="9bf55-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9bf55-113">**Element**</span></span>|<span data-ttu-id="9bf55-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9bf55-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9bf55-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="9bf55-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="9bf55-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="9bf55-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="9bf55-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="9bf55-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="9bf55-118">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9bf55-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9bf55-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="9bf55-119">Text value</span></span>

<span data-ttu-id="9bf55-120">Ein Textwert, der einen ganzzahligen Wert darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9bf55-120">A text value that represents an integer value is required if this element is used.</span></span> <span data-ttu-id="9bf55-121">Im folgenden sind die möglichen Werte für dieses Element angegeben:</span><span class="sxs-lookup"><span data-stu-id="9bf55-121">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="9bf55-122">0 = NetMeeting</span><span class="sxs-lookup"><span data-stu-id="9bf55-122">0 = NetMeeting</span></span>
    
- <span data-ttu-id="9bf55-123">1 = NetShow</span><span class="sxs-lookup"><span data-stu-id="9bf55-123">1 = NetShow</span></span>
    
- <span data-ttu-id="9bf55-124">2 = Chat</span><span class="sxs-lookup"><span data-stu-id="9bf55-124">2 = Chat</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9bf55-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9bf55-125">Remarks</span></span>

<span data-ttu-id="9bf55-126">Die **MeetingWorkspaceUrl** -Eigenschaft ist für das Kalenderelement des Organisators schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9bf55-126">The **MeetingWorkspaceUrl** property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="9bf55-127">Er ist schreibgeschützt für Besprechungsanfragen und Kalenderelemente des Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="9bf55-127">It is read-only for meeting requests and for attendee's calendar items.</span></span> 
  
<span data-ttu-id="9bf55-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="9bf55-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="9bf55-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9bf55-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9bf55-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="9bf55-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9bf55-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9bf55-131">Schema Name</span></span>  <br/> |<span data-ttu-id="9bf55-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9bf55-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="9bf55-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9bf55-133">Validation File</span></span>  <br/> |<span data-ttu-id="9bf55-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9bf55-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9bf55-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9bf55-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="9bf55-136">False</span><span class="sxs-lookup"><span data-stu-id="9bf55-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9bf55-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bf55-137">See also</span></span>



- [<span data-ttu-id="9bf55-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9bf55-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

