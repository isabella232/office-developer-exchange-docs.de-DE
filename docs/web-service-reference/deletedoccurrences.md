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
description: Das DeletedOccurrences-Element enthält ein Array von gelöschten Vorkommen eines wiederkehrenden Kalenderelements.
ms.openlocfilehash: be39ff95b5529481a36b7549e638818a20e01283
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463706"
---
# <a name="deletedoccurrences"></a><span data-ttu-id="913df-103">DeletedOccurrences</span><span class="sxs-lookup"><span data-stu-id="913df-103">DeletedOccurrences</span></span>

<span data-ttu-id="913df-104">Das **DeletedOccurrences** -Element enthält ein Array von gelöschten Vorkommen eines wiederkehrenden Kalenderelements.</span><span class="sxs-lookup"><span data-stu-id="913df-104">The **DeletedOccurrences** element contains an array of deleted occurrences of a recurring calendar item.</span></span> 
  
```xml
<DeletedOccurrences>
   <DeletedOccurrence/>
</DeletedOccurrences>
```

 <span data-ttu-id="913df-105">**NonEmptyArrayOfDeletedOccurrencesType**</span><span class="sxs-lookup"><span data-stu-id="913df-105">**NonEmptyArrayOfDeletedOccurrencesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="913df-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="913df-106">Attributes and elements</span></span>

<span data-ttu-id="913df-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="913df-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="913df-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="913df-108">Attributes</span></span>

<span data-ttu-id="913df-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="913df-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="913df-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="913df-110">Child elements</span></span>

|<span data-ttu-id="913df-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="913df-111">**Element**</span></span>|<span data-ttu-id="913df-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="913df-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="913df-113">DeletedOccurrence</span><span class="sxs-lookup"><span data-stu-id="913df-113">DeletedOccurrence</span></span>](deletedoccurrence.md) <br/> |<span data-ttu-id="913df-114">Stellt ein gelöschtes Vorkommen eines wiederkehrenden Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="913df-114">Represents a deleted occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="913df-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="913df-115">Parent elements</span></span>

|<span data-ttu-id="913df-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="913df-116">**Element**</span></span>|<span data-ttu-id="913df-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="913df-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="913df-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="913df-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="913df-119">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="913df-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="913df-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="913df-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="913df-121">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="913df-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="913df-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="913df-122">Remarks</span></span>

<span data-ttu-id="913df-123">Dieses Element ist gültig, wenn der RecurringMaster-Textwert für das [CalendarItemType](calendaritemtype.md) -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="913df-123">This element is valid if the RecurringMaster text value is used for the [CalendarItemType](calendaritemtype.md) element.</span></span> 
  
<span data-ttu-id="913df-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="913df-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="913df-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="913df-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="913df-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="913df-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="913df-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="913df-127">Schema name</span></span>  <br/> |<span data-ttu-id="913df-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="913df-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="913df-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="913df-129">Validation file</span></span>  <br/> |<span data-ttu-id="913df-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="913df-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="913df-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="913df-131">Can be empty</span></span>  <br/> |<span data-ttu-id="913df-132">False</span><span class="sxs-lookup"><span data-stu-id="913df-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="913df-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="913df-133">See also</span></span>

- [<span data-ttu-id="913df-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="913df-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)  
- [<span data-ttu-id="913df-135">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="913df-135">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

