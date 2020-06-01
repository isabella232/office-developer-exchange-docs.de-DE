---
title: IsCancelled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsCancelled
api_type:
- schema
ms.assetid: 50c1e97f-2913-47a1-8457-60428a3c5b92
description: Das IsCanceled-Element gibt an, ob ein Termin oder eine Besprechung abgebrochen wurde.
ms.openlocfilehash: 946c9d956da9cf31e9fa08d4ab6f4950b11214b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455569"
---
# <a name="iscancelled"></a><span data-ttu-id="039d2-103">IsCancelled</span><span class="sxs-lookup"><span data-stu-id="039d2-103">IsCancelled</span></span>

<span data-ttu-id="039d2-104">Das **IsCanceled** -Element gibt an, ob ein Termin oder eine Besprechung abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="039d2-104">The **IsCancelled** element indicates whether an appointment or meeting has been canceled.</span></span> 
  
```xml
<IsCancelled/>
```

 <span data-ttu-id="039d2-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="039d2-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="039d2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="039d2-106">Attributes and elements</span></span>

<span data-ttu-id="039d2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="039d2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="039d2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="039d2-108">Attributes</span></span>

<span data-ttu-id="039d2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="039d2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="039d2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="039d2-110">Child elements</span></span>

<span data-ttu-id="039d2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="039d2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="039d2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="039d2-112">Parent elements</span></span>

|<span data-ttu-id="039d2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="039d2-113">**Element**</span></span>|<span data-ttu-id="039d2-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="039d2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="039d2-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="039d2-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="039d2-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="039d2-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="039d2-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="039d2-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="039d2-118">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="039d2-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="039d2-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="039d2-119">Text value</span></span>

<span data-ttu-id="039d2-120">Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich, wenn dieses Element enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="039d2-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="039d2-121">Der Wert **true** gibt an, dass das Kalenderelement abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="039d2-121">A value of **true** indicates that the calendar item has been canceled.</span></span> <span data-ttu-id="039d2-122">Der Wert **false** gibt an, dass ein Kalenderelement nicht abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="039d2-122">A value of **false** indicates that a calendar item has not been canceled.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="039d2-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="039d2-123">Remarks</span></span>

<span data-ttu-id="039d2-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="039d2-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="039d2-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="039d2-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="039d2-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="039d2-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="039d2-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="039d2-127">Schema name</span></span>  <br/> |<span data-ttu-id="039d2-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="039d2-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="039d2-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="039d2-129">Validation file</span></span>  <br/> |<span data-ttu-id="039d2-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="039d2-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="039d2-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="039d2-131">Can be empty</span></span>  <br/> |<span data-ttu-id="039d2-132">False</span><span class="sxs-lookup"><span data-stu-id="039d2-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="039d2-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="039d2-133">See also</span></span>



- [<span data-ttu-id="039d2-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="039d2-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

