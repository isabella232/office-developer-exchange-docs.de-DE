---
title: Isexception
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsException
api_type:
- schema
ms.assetid: e7bd8ae2-2643-411e-ae08-358bac445800
description: Das isexception-Element gibt an, ob eine Instanz eines wiederkehrenden Kalenderelements aus dem Master-Objekt geändert wird.
ms.openlocfilehash: f2e45e0f1010449d4a494f5e15ecd0b22dc598e4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457585"
---
# <a name="isexception"></a><span data-ttu-id="894df-103">Isexception</span><span class="sxs-lookup"><span data-stu-id="894df-103">IsException</span></span>

<span data-ttu-id="894df-104">Das **isexception** -Element gibt an, ob eine Instanz eines wiederkehrenden Kalenderelements aus dem Master-Objekt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="894df-104">The **IsException** element indicates whether an instance of a recurring calendar item is changed from the master.</span></span> 
  
[<span data-ttu-id="894df-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="894df-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="894df-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="894df-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="894df-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="894df-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="894df-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="894df-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="894df-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="894df-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="894df-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="894df-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="894df-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="894df-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="894df-112">Isexception</span><span class="sxs-lookup"><span data-stu-id="894df-112">IsException</span></span>](isexception.md)
  
```xml
<IsException/>
```

 <span data-ttu-id="894df-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="894df-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="894df-114">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="894df-114">Attributes and elements</span></span>

<span data-ttu-id="894df-115">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="894df-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="894df-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="894df-116">Attributes</span></span>

<span data-ttu-id="894df-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="894df-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="894df-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="894df-118">Child elements</span></span>

<span data-ttu-id="894df-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="894df-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="894df-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="894df-120">Parent elements</span></span>

|<span data-ttu-id="894df-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="894df-121">**Element**</span></span>|<span data-ttu-id="894df-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="894df-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="894df-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="894df-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="894df-124">Enthält zusätzliche Informationen zu einem Kalenderereignis.</span><span class="sxs-lookup"><span data-stu-id="894df-124">Provides additional information about a calendar event.</span></span>  <br/> <span data-ttu-id="894df-125">Im folgenden finden Sie den XPath 2,0-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="894df-125">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="894df-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="894df-126">Text value</span></span>

<span data-ttu-id="894df-127">Ein Textwert ist erforderlich, wenn dieses Element in der Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="894df-127">A text value is required if this element is returned in the response.</span></span> <span data-ttu-id="894df-128">Dieses Element ist erforderlich, wenn das [CalendarEventDetails](calendareventdetails.md) -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="894df-128">This element is required if the [CalendarEventDetails](calendareventdetails.md) element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="894df-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="894df-129">Remarks</span></span>

<span data-ttu-id="894df-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="894df-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="894df-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="894df-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="894df-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="894df-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="894df-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="894df-133">Schema Name</span></span>  <br/> |<span data-ttu-id="894df-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="894df-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="894df-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="894df-135">Validation File</span></span>  <br/> |<span data-ttu-id="894df-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="894df-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="894df-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="894df-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="894df-138">False</span><span class="sxs-lookup"><span data-stu-id="894df-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="894df-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="894df-139">See also</span></span>



[<span data-ttu-id="894df-140">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="894df-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="894df-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="894df-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="894df-142">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="894df-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

