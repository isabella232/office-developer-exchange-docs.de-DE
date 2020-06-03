---
title: Myresponsetype
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MyResponseType
api_type:
- schema
ms.assetid: 9741b71d-a310-4520-81d5-3787a1ee630f
description: Das myresponsetype-Element enthält den Status oder die Antwort auf ein Kalenderelement.
ms.openlocfilehash: 640b0595ac039cc3c119aa52aa6e791e5b695e87
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466626"
---
# <a name="myresponsetype"></a><span data-ttu-id="4dba9-103">Myresponsetype</span><span class="sxs-lookup"><span data-stu-id="4dba9-103">MyResponseType</span></span>

<span data-ttu-id="4dba9-104">Das **myresponsetype** -Element enthält den Status oder die Antwort auf ein Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="4dba9-104">The **MyResponseType** element contains the status of or response to a calendar item.</span></span> 
  
```xml
<MyResponseType/>
```

 <span data-ttu-id="4dba9-105">**ResponseTypeType**</span><span class="sxs-lookup"><span data-stu-id="4dba9-105">**ResponseTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4dba9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4dba9-106">Attributes and elements</span></span>

<span data-ttu-id="4dba9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4dba9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4dba9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4dba9-108">Attributes</span></span>

<span data-ttu-id="4dba9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4dba9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4dba9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4dba9-110">Child elements</span></span>

<span data-ttu-id="4dba9-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="4dba9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4dba9-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4dba9-112">Parent elements</span></span>

|<span data-ttu-id="4dba9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4dba9-113">**Element**</span></span>|<span data-ttu-id="4dba9-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4dba9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4dba9-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="4dba9-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="4dba9-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="4dba9-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="4dba9-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="4dba9-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="4dba9-118">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="4dba9-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4dba9-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="4dba9-119">Text value</span></span>

<span data-ttu-id="4dba9-120">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4dba9-120">A text value is required.</span></span> <span data-ttu-id="4dba9-121">Im folgenden sind die möglichen Text Werte für dieses Element angegeben:</span><span class="sxs-lookup"><span data-stu-id="4dba9-121">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="4dba9-122">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="4dba9-122">Unknown</span></span>
    
- <span data-ttu-id="4dba9-123">Organisator</span><span class="sxs-lookup"><span data-stu-id="4dba9-123">Organizer</span></span>
    
- <span data-ttu-id="4dba9-124">Vorläufige</span><span class="sxs-lookup"><span data-stu-id="4dba9-124">Tentative</span></span>
    
- <span data-ttu-id="4dba9-125">Annehmen</span><span class="sxs-lookup"><span data-stu-id="4dba9-125">Accept</span></span>
    
- <span data-ttu-id="4dba9-126">Ablehnen</span><span class="sxs-lookup"><span data-stu-id="4dba9-126">Decline</span></span>
    
- <span data-ttu-id="4dba9-127">NoResponseReceived</span><span class="sxs-lookup"><span data-stu-id="4dba9-127">NoResponseReceived</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4dba9-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4dba9-128">Remarks</span></span>

<span data-ttu-id="4dba9-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="4dba9-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4dba9-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4dba9-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4dba9-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="4dba9-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4dba9-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4dba9-132">Schema name</span></span>  <br/> |<span data-ttu-id="4dba9-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4dba9-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="4dba9-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4dba9-134">Validation file</span></span>  <br/> |<span data-ttu-id="4dba9-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4dba9-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4dba9-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="4dba9-136">Can be empty</span></span>  <br/> |<span data-ttu-id="4dba9-137">False</span><span class="sxs-lookup"><span data-stu-id="4dba9-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4dba9-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4dba9-138">See also</span></span>



- [<span data-ttu-id="4dba9-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4dba9-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

