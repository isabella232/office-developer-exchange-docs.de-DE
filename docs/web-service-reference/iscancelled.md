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
description: Das IsCancelled-Element gibt an, ob eines Termins oder einer Besprechung abgebrochen wurde.
ms.openlocfilehash: 594b8a9ccb535f074a8cf1da060373f640231a29
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829993"
---
# <a name="iscancelled"></a><span data-ttu-id="78cfd-103">IsCancelled</span><span class="sxs-lookup"><span data-stu-id="78cfd-103">IsCancelled</span></span>

<span data-ttu-id="78cfd-104">Das **IsCancelled** -Element gibt an, ob eines Termins oder einer Besprechung abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="78cfd-104">The **IsCancelled** element indicates whether an appointment or meeting has been canceled.</span></span> 
  
```xml
<IsCancelled/>
```

 <span data-ttu-id="78cfd-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="78cfd-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="78cfd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="78cfd-106">Attributes and elements</span></span>

<span data-ttu-id="78cfd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="78cfd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="78cfd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="78cfd-108">Attributes</span></span>

<span data-ttu-id="78cfd-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="78cfd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="78cfd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="78cfd-110">Child elements</span></span>

<span data-ttu-id="78cfd-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="78cfd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="78cfd-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="78cfd-112">Parent elements</span></span>

|<span data-ttu-id="78cfd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="78cfd-113">**Element**</span></span>|<span data-ttu-id="78cfd-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78cfd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78cfd-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="78cfd-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="78cfd-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="78cfd-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="78cfd-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="78cfd-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="78cfd-118">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="78cfd-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="78cfd-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="78cfd-119">Text value</span></span>

<span data-ttu-id="78cfd-120">Ein Textwert, der einen booleschen Wert darstellt ist erforderlich, wenn dieses Element enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="78cfd-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="78cfd-121">Der Wert **true** gibt an, dass das Kalenderelement abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="78cfd-121">A value of **true** indicates that the calendar item has been canceled.</span></span> <span data-ttu-id="78cfd-122">Der Wert **false** gibt an, dass ein Kalenderelement nicht abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="78cfd-122">A value of **false** indicates that a calendar item has not been canceled.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="78cfd-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="78cfd-123">Remarks</span></span>

<span data-ttu-id="78cfd-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="78cfd-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="78cfd-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="78cfd-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78cfd-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="78cfd-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="78cfd-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="78cfd-127">Schema name</span></span>  <br/> |<span data-ttu-id="78cfd-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="78cfd-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="78cfd-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="78cfd-129">Validation file</span></span>  <br/> |<span data-ttu-id="78cfd-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="78cfd-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="78cfd-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="78cfd-131">Can be empty</span></span>  <br/> |<span data-ttu-id="78cfd-132">False</span><span class="sxs-lookup"><span data-stu-id="78cfd-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78cfd-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78cfd-133">See also</span></span>



- [<span data-ttu-id="78cfd-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="78cfd-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

