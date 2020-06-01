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
description: Das MeetingWorkspaceUrl-Element enthält die URL für den Besprechungsarbeitsbereich, der im Kalenderelement enthalten ist. Ein Besprechungsarbeitsbereich ist eine freigegebene Website zum Planen der Besprechung und zum Nachverfolgen der Ergebnisse.
ms.openlocfilehash: cd4396e590ab1471278bd44b9a4e0009fe326eaf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466283"
---
# <a name="meetingworkspaceurl"></a><span data-ttu-id="45a5f-104">MeetingWorkspaceUrl</span><span class="sxs-lookup"><span data-stu-id="45a5f-104">MeetingWorkspaceUrl</span></span>

<span data-ttu-id="45a5f-105">Das **MeetingWorkspaceUrl** -Element enthält die URL für den Besprechungsarbeitsbereich, der im Kalenderelement enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="45a5f-105">The **MeetingWorkspaceUrl** element contains the URL for the meeting workspace that is included in the calendar item.</span></span> <span data-ttu-id="45a5f-106">Ein Besprechungsarbeitsbereich ist eine freigegebene Website zum Planen der Besprechung und zum Nachverfolgen der Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="45a5f-106">A meeting workspace is a shared Web site for planning the meeting and tracking the results.</span></span> 
  
```xml
<MeetingWorkspaceUrl/>
```

 <span data-ttu-id="45a5f-107">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45a5f-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="45a5f-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="45a5f-108">Attributes and elements</span></span>

<span data-ttu-id="45a5f-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="45a5f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="45a5f-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="45a5f-110">Attributes</span></span>

<span data-ttu-id="45a5f-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="45a5f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="45a5f-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="45a5f-112">Child elements</span></span>

<span data-ttu-id="45a5f-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="45a5f-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="45a5f-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="45a5f-114">Parent elements</span></span>

|<span data-ttu-id="45a5f-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="45a5f-115">**Element**</span></span>|<span data-ttu-id="45a5f-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="45a5f-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="45a5f-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="45a5f-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="45a5f-118">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="45a5f-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="45a5f-119">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="45a5f-119">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="45a5f-120">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="45a5f-120">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="45a5f-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="45a5f-121">Text value</span></span>

<span data-ttu-id="45a5f-122">Ein Text Wert, der eine URL darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="45a5f-122">A text value that represents a URL is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="45a5f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45a5f-123">Remarks</span></span>

<span data-ttu-id="45a5f-124">Die MeetingWorkspaceUrl-Eigenschaft ist für das Kalenderelement des Organisators schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="45a5f-124">The MeetingWorkspaceUrl property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="45a5f-125">Er ist schreibgeschützt für Besprechungsanfragen und für die Kalenderelemente von Teilnehmern.</span><span class="sxs-lookup"><span data-stu-id="45a5f-125">It is read-only for meeting requests and for attendees' calendar items.</span></span>
  
<span data-ttu-id="45a5f-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="45a5f-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="45a5f-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="45a5f-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45a5f-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="45a5f-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="45a5f-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="45a5f-129">Schema name</span></span>  <br/> |<span data-ttu-id="45a5f-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="45a5f-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="45a5f-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="45a5f-131">Validation file</span></span>  <br/> |<span data-ttu-id="45a5f-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="45a5f-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="45a5f-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="45a5f-133">Can be empty</span></span>  <br/> |<span data-ttu-id="45a5f-134">False</span><span class="sxs-lookup"><span data-stu-id="45a5f-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="45a5f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45a5f-135">See also</span></span>



- [<span data-ttu-id="45a5f-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="45a5f-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

