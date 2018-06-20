---
title: MeetingWorkspaceUrl
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingWorkspaceUrl
api_type:
- schema
ms.assetid: 0ca942fe-8f57-4065-93ad-65790f9a04c3
description: Das MeetingWorkspaceUrl-Element enthält die URL für den Besprechungsarbeitsbereich, der im Kalenderelement enthalten ist. Ein Besprechungsarbeitsbereich ist eine freigegebene Website zum Planen einer Besprechung und Protokollieren der Besprechungsergebnisse.
ms.openlocfilehash: 7d84547eafe4e77fb23a792fbf15633dbf93d775
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830436"
---
# <a name="meetingworkspaceurl"></a><span data-ttu-id="0555b-104">MeetingWorkspaceUrl</span><span class="sxs-lookup"><span data-stu-id="0555b-104">MeetingWorkspaceUrl</span></span>

<span data-ttu-id="0555b-105">Das **MeetingWorkspaceUrl** -Element enthält die URL für den Besprechungsarbeitsbereich, der im Kalenderelement enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="0555b-105">The **MeetingWorkspaceUrl** element contains the URL for the meeting workspace that is included in the calendar item.</span></span> <span data-ttu-id="0555b-106">Ein Besprechungsarbeitsbereich ist eine freigegebene Website zum Planen einer Besprechung und Protokollieren der Besprechungsergebnisse.</span><span class="sxs-lookup"><span data-stu-id="0555b-106">A meeting workspace is a shared Web site for planning the meeting and tracking the results.</span></span> 
  
```xml
<MeetingWorkspaceUrl/>
```

 <span data-ttu-id="0555b-107">**string**</span><span class="sxs-lookup"><span data-stu-id="0555b-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0555b-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0555b-108">Attributes and elements</span></span>

<span data-ttu-id="0555b-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0555b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0555b-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0555b-110">Attributes</span></span>

<span data-ttu-id="0555b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0555b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0555b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0555b-112">Child elements</span></span>

<span data-ttu-id="0555b-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="0555b-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0555b-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0555b-114">Parent elements</span></span>

|<span data-ttu-id="0555b-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="0555b-115">**Element**</span></span>|<span data-ttu-id="0555b-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0555b-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0555b-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="0555b-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="0555b-118">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="0555b-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0555b-119">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="0555b-119">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="0555b-120">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="0555b-120">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0555b-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="0555b-121">Text value</span></span>

<span data-ttu-id="0555b-122">Ein Textwert, der eine URL darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0555b-122">A text value that represents a URL is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0555b-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0555b-123">Remarks</span></span>

<span data-ttu-id="0555b-124">Meetingworkspaceurl (Eigenschaft) kann für den Organisator Kalenderelement lesen geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="0555b-124">The MeetingWorkspaceUrl property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="0555b-125">Es ist schreibgeschützt, für Besprechungsanfragen und Kalenderelemente Teilnehmer.</span><span class="sxs-lookup"><span data-stu-id="0555b-125">It is read-only for meeting requests and for attendees' calendar items.</span></span>
  
<span data-ttu-id="0555b-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="0555b-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0555b-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0555b-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0555b-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="0555b-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0555b-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0555b-129">Schema name</span></span>  <br/> |<span data-ttu-id="0555b-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0555b-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="0555b-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0555b-131">Validation file</span></span>  <br/> |<span data-ttu-id="0555b-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0555b-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0555b-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="0555b-133">Can be empty</span></span>  <br/> |<span data-ttu-id="0555b-134">False</span><span class="sxs-lookup"><span data-stu-id="0555b-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0555b-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0555b-135">See also</span></span>



- [<span data-ttu-id="0555b-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0555b-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

