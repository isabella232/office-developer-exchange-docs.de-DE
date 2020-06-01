---
title: Ismeeting
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
description: Das ismeeting-Element gibt an, ob es sich bei dem Kalenderelement um eine Besprechung oder einen Termin handelt.
ms.openlocfilehash: fd72766977567210cd08b47d0723cd73aa53a622
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465968"
---
# <a name="ismeeting"></a><span data-ttu-id="c9038-103">Ismeeting</span><span class="sxs-lookup"><span data-stu-id="c9038-103">IsMeeting</span></span>

<span data-ttu-id="c9038-104">Das **ismeeting** -Element gibt an, ob es sich bei dem Kalenderelement um eine Besprechung oder einen Termin handelt.</span><span class="sxs-lookup"><span data-stu-id="c9038-104">The **IsMeeting** element indicates whether the calendar item is a meeting or an appointment.</span></span> 
  
```xml
<IsMeeting/>
```

 <span data-ttu-id="c9038-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="c9038-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c9038-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c9038-106">Attributes and elements</span></span>

<span data-ttu-id="c9038-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c9038-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c9038-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c9038-108">Attributes</span></span>

<span data-ttu-id="c9038-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c9038-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c9038-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c9038-110">Child elements</span></span>

<span data-ttu-id="c9038-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c9038-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c9038-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c9038-112">Parent elements</span></span>

|<span data-ttu-id="c9038-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c9038-113">**Element**</span></span>|<span data-ttu-id="c9038-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c9038-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9038-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="c9038-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="c9038-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="c9038-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c9038-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="c9038-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="c9038-118">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="c9038-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c9038-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="c9038-119">Text value</span></span>

<span data-ttu-id="c9038-120">Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich, wenn dieses Element enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="c9038-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="c9038-121">Der Wert **true** gibt an, dass es sich bei dem Kalenderelement um eine Besprechung handelt.</span><span class="sxs-lookup"><span data-stu-id="c9038-121">A value of **true** indicates that the calendar item is a meeting.</span></span> <span data-ttu-id="c9038-122">Der Wert **false** gibt an, dass das Kalenderelement ein Termin ist.</span><span class="sxs-lookup"><span data-stu-id="c9038-122">A value of **false** indicates that the calendar item is an appointment.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c9038-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9038-123">Remarks</span></span>

<span data-ttu-id="c9038-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c9038-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c9038-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c9038-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9038-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="c9038-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c9038-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c9038-127">Schema name</span></span>  <br/> |<span data-ttu-id="c9038-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c9038-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="c9038-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c9038-129">Validation file</span></span>  <br/> |<span data-ttu-id="c9038-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c9038-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c9038-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c9038-131">Can be empty</span></span>  <br/> |<span data-ttu-id="c9038-132">False</span><span class="sxs-lookup"><span data-stu-id="c9038-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9038-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9038-133">See also</span></span>



- [<span data-ttu-id="c9038-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c9038-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

