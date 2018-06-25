---
title: IsMeeting
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsMeeting
api_type:
- schema
ms.assetid: 6ce22f17-7a31-46c4-b643-0894d087e852
description: Das IsMeeting-Element gibt an, ob das Kalenderelement einer Besprechung oder eines Termins ist.
ms.openlocfilehash: bb1349a8690450882e6beac0ccd84a8d03272a7d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830051"
---
# <a name="ismeeting"></a><span data-ttu-id="83dc9-103">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="83dc9-103">IsMeeting</span></span>

<span data-ttu-id="83dc9-104">Das **IsMeeting** -Element gibt an, ob das Kalenderelement einer Besprechung oder eines Termins ist.</span><span class="sxs-lookup"><span data-stu-id="83dc9-104">The **IsMeeting** element indicates whether the calendar item is a meeting or an appointment.</span></span> 
  
```xml
<IsMeeting/>
```

 <span data-ttu-id="83dc9-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="83dc9-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83dc9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="83dc9-106">Attributes and elements</span></span>

<span data-ttu-id="83dc9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="83dc9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83dc9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="83dc9-108">Attributes</span></span>

<span data-ttu-id="83dc9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="83dc9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83dc9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83dc9-110">Child elements</span></span>

<span data-ttu-id="83dc9-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="83dc9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="83dc9-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83dc9-112">Parent elements</span></span>

|<span data-ttu-id="83dc9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="83dc9-113">**Element**</span></span>|<span data-ttu-id="83dc9-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="83dc9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83dc9-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="83dc9-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="83dc9-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="83dc9-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="83dc9-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="83dc9-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="83dc9-118">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="83dc9-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="83dc9-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="83dc9-119">Text value</span></span>

<span data-ttu-id="83dc9-120">Ein Textwert, der einen booleschen Wert darstellt ist erforderlich, wenn dieses Element enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="83dc9-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="83dc9-121">Der Wert **true** gibt an, dass das Kalenderelement eine Besprechung ist.</span><span class="sxs-lookup"><span data-stu-id="83dc9-121">A value of **true** indicates that the calendar item is a meeting.</span></span> <span data-ttu-id="83dc9-122">Der Wert **false** gibt an, dass das Kalenderelement einen Termin handelt.</span><span class="sxs-lookup"><span data-stu-id="83dc9-122">A value of **false** indicates that the calendar item is an appointment.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="83dc9-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="83dc9-123">Remarks</span></span>

<span data-ttu-id="83dc9-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="83dc9-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83dc9-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="83dc9-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83dc9-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="83dc9-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="83dc9-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="83dc9-127">Schema name</span></span>  <br/> |<span data-ttu-id="83dc9-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="83dc9-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="83dc9-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="83dc9-129">Validation file</span></span>  <br/> |<span data-ttu-id="83dc9-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="83dc9-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="83dc9-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="83dc9-131">Can be empty</span></span>  <br/> |<span data-ttu-id="83dc9-132">False</span><span class="sxs-lookup"><span data-stu-id="83dc9-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83dc9-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83dc9-133">See also</span></span>



- [<span data-ttu-id="83dc9-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="83dc9-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

