---
title: DeletedOccurrences
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeletedOccurrences
api_type:
- schema
ms.assetid: 736fb305-9528-4be8-ad37-65d7556edbf2
description: Das DeletedOccurrences-Element enthält ein Array von gelöschten Vorkommen eines sich wiederholenden Kalenderelements an.
ms.openlocfilehash: 269c1176913cd642f93987462286dd1fee3a7339
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757914"
---
# <a name="deletedoccurrences"></a><span data-ttu-id="40bc5-103">DeletedOccurrences</span><span class="sxs-lookup"><span data-stu-id="40bc5-103">DeletedOccurrences</span></span>

<span data-ttu-id="40bc5-104">Das **DeletedOccurrences** -Element enthält ein Array von gelöschten Vorkommen eines sich wiederholenden Kalenderelements an.</span><span class="sxs-lookup"><span data-stu-id="40bc5-104">The **DeletedOccurrences** element contains an array of deleted occurrences of a recurring calendar item.</span></span> 
  
```xml
<DeletedOccurrences>
   <DeletedOccurrence/>
</DeletedOccurrences>
```

 <span data-ttu-id="40bc5-105">**NonEmptyArrayOfDeletedOccurrencesType**</span><span class="sxs-lookup"><span data-stu-id="40bc5-105">**NonEmptyArrayOfDeletedOccurrencesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="40bc5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="40bc5-106">Attributes and elements</span></span>

<span data-ttu-id="40bc5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="40bc5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="40bc5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="40bc5-108">Attributes</span></span>

<span data-ttu-id="40bc5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="40bc5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="40bc5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="40bc5-110">Child elements</span></span>

|<span data-ttu-id="40bc5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="40bc5-111">**Element**</span></span>|<span data-ttu-id="40bc5-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="40bc5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40bc5-113">DeletedOccurrence</span><span class="sxs-lookup"><span data-stu-id="40bc5-113">DeletedOccurrence</span></span>](deletedoccurrence.md) <br/> |<span data-ttu-id="40bc5-114">Stellt eine gelöschte Vorkommen eines sich wiederholenden Kalenderelements an.</span><span class="sxs-lookup"><span data-stu-id="40bc5-114">Represents a deleted occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="40bc5-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="40bc5-115">Parent elements</span></span>

|<span data-ttu-id="40bc5-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="40bc5-116">**Element**</span></span>|<span data-ttu-id="40bc5-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="40bc5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40bc5-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="40bc5-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="40bc5-119">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="40bc5-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="40bc5-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="40bc5-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="40bc5-121">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="40bc5-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40bc5-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="40bc5-122">Remarks</span></span>

<span data-ttu-id="40bc5-123">Dieses Element ist gültig, wenn der Wert der RecurringMaster-Text für das [CalendarItemType](calendaritemtype.md) -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="40bc5-123">This element is valid if the RecurringMaster text value is used for the [CalendarItemType](calendaritemtype.md) element.</span></span> 
  
<span data-ttu-id="40bc5-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="40bc5-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="40bc5-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="40bc5-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40bc5-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="40bc5-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="40bc5-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="40bc5-127">Schema name</span></span>  <br/> |<span data-ttu-id="40bc5-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="40bc5-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="40bc5-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="40bc5-129">Validation file</span></span>  <br/> |<span data-ttu-id="40bc5-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="40bc5-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="40bc5-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="40bc5-131">Can be empty</span></span>  <br/> |<span data-ttu-id="40bc5-132">False</span><span class="sxs-lookup"><span data-stu-id="40bc5-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40bc5-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40bc5-133">See also</span></span>

- [<span data-ttu-id="40bc5-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="40bc5-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)  
- [<span data-ttu-id="40bc5-135">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="40bc5-135">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

