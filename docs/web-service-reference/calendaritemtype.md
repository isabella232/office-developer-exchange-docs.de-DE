---
title: CalendarItemType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarItemType
api_type:
- schema
ms.assetid: 1feb0788-adf7-4a7c-830c-005214ad930f
description: Das CalendarItemType-Element darstellt den Typ des ein Kalenderelement.
ms.openlocfilehash: 3fe95c86ea24e6dfeb4740ead5e787bd63b5190d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757531"
---
# <a name="calendaritemtype"></a><span data-ttu-id="3dee0-103">CalendarItemType</span><span class="sxs-lookup"><span data-stu-id="3dee0-103">CalendarItemType</span></span>

<span data-ttu-id="3dee0-104">Das **CalendarItemType** -Element darstellt den Typ des ein Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="3dee0-104">The **CalendarItemType** element represents the type of a calendar item.</span></span> 
  
```xml
<CalendarItemType/>
```

 <span data-ttu-id="3dee0-105">**CalendarItemTypeType**</span><span class="sxs-lookup"><span data-stu-id="3dee0-105">**CalendarItemTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3dee0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3dee0-106">Attributes and elements</span></span>

<span data-ttu-id="3dee0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3dee0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3dee0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3dee0-108">Attributes</span></span>

<span data-ttu-id="3dee0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3dee0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3dee0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3dee0-110">Child elements</span></span>

<span data-ttu-id="3dee0-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3dee0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3dee0-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3dee0-112">Parent elements</span></span>

|<span data-ttu-id="3dee0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3dee0-113">**Element**</span></span>|<span data-ttu-id="3dee0-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3dee0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3dee0-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="3dee0-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="3dee0-116">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="3dee0-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3dee0-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="3dee0-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="3dee0-118">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="3dee0-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3dee0-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="3dee0-119">Text value</span></span>

<span data-ttu-id="3dee0-120">Ein Textwert ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3dee0-120">A text value is required if this element is used.</span></span> <span data-ttu-id="3dee0-121">Es folgen die möglichen Werte für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="3dee0-121">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="3dee0-122">**Einzelne** Das Element ist kein wiederkehrendes Kalenderelement zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3dee0-122">**Single** The item is not associated with a recurring calendar item.</span></span> 
    
- <span data-ttu-id="3dee0-123">**Vorkommen** Das Element ist ein Vorkommen eines sich wiederholenden Kalenderelements an.</span><span class="sxs-lookup"><span data-stu-id="3dee0-123">**Occurrence** The item is an occurrence of a recurring calendar item.</span></span> 
    
- <span data-ttu-id="3dee0-124">**Ausnahme** Das Element ist eine Ausnahme in ein wiederkehrendes Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="3dee0-124">**Exception** The item is an exception to a recurring calendar item.</span></span> 
    
- <span data-ttu-id="3dee0-125">**RecurringMaster** Das Element ist für eine Reihe von wiederkehrende Kalenderelemente master.</span><span class="sxs-lookup"><span data-stu-id="3dee0-125">**RecurringMaster** The item is master for a set of recurring calendar items.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3dee0-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3dee0-126">Remarks</span></span>

<span data-ttu-id="3dee0-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="3dee0-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3dee0-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3dee0-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3dee0-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="3dee0-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3dee0-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3dee0-130">Schema name</span></span>  <br/> |<span data-ttu-id="3dee0-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3dee0-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="3dee0-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3dee0-132">Validation file</span></span>  <br/> |<span data-ttu-id="3dee0-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3dee0-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3dee0-134">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="3dee0-134">Can be empty</span></span>  <br/> |<span data-ttu-id="3dee0-135">False</span><span class="sxs-lookup"><span data-stu-id="3dee0-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3dee0-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dee0-136">See also</span></span>



- [<span data-ttu-id="3dee0-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3dee0-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

