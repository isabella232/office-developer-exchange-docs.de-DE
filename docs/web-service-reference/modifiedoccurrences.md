---
title: ModifiedOccurrences
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ModifiedOccurrences
api_type:
- schema
ms.assetid: 552932fc-b3b4-486e-8d73-32c0bb10bd68
description: Das ModifiedOccurrences-Element enthält ein Array von wiederkehrenden Kalenderelement vorkommen, die geändert wurden, sodass Sie sich vom Serienmasterelement unterscheiden.
ms.openlocfilehash: d599e3d232bfffc5bedd37f3dae4d8b10a82ffde
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530422"
---
# <a name="modifiedoccurrences"></a><span data-ttu-id="5ccf3-103">ModifiedOccurrences</span><span class="sxs-lookup"><span data-stu-id="5ccf3-103">ModifiedOccurrences</span></span>

<span data-ttu-id="5ccf3-104">Das **ModifiedOccurrences** -Element enthält ein Array von wiederkehrenden Kalenderelement vorkommen, die geändert wurden, sodass Sie sich vom Serienmasterelement unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="5ccf3-104">The **ModifiedOccurrences** element contains an array of recurring calendar item occurrences that have been modified so that they are different than the recurrence master item.</span></span> 
  
```xml
<ModifiedOccurrences>
   <Occurrence/>
</ModifiedOccurrences>
```

 <span data-ttu-id="5ccf3-105">**NonEmptyArrayOfOccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="5ccf3-105">**NonEmptyArrayOfOccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5ccf3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5ccf3-106">Attributes and elements</span></span>

<span data-ttu-id="5ccf3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5ccf3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5ccf3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5ccf3-108">Attributes</span></span>

<span data-ttu-id="5ccf3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5ccf3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5ccf3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5ccf3-110">Child elements</span></span>

|<span data-ttu-id="5ccf3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5ccf3-111">**Element**</span></span>|<span data-ttu-id="5ccf3-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5ccf3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5ccf3-113">Vorkommen</span><span class="sxs-lookup"><span data-stu-id="5ccf3-113">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="5ccf3-114">Stellt ein einzelnes geändertes Vorkommen eines wiederkehrenden Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="5ccf3-114">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5ccf3-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5ccf3-115">Parent elements</span></span>

|<span data-ttu-id="5ccf3-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="5ccf3-116">**Element**</span></span>|<span data-ttu-id="5ccf3-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5ccf3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5ccf3-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="5ccf3-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="5ccf3-119">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="5ccf3-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="5ccf3-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="5ccf3-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="5ccf3-121">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="5ccf3-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ccf3-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ccf3-122">Remarks</span></span>

<span data-ttu-id="5ccf3-123">Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den RecurringMaster-Wert aufweist.</span><span class="sxs-lookup"><span data-stu-id="5ccf3-123">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="5ccf3-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="5ccf3-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5ccf3-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5ccf3-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5ccf3-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ccf3-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5ccf3-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5ccf3-127">Schema name</span></span>  <br/> |<span data-ttu-id="5ccf3-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5ccf3-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="5ccf3-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5ccf3-129">Validation file</span></span>  <br/> |<span data-ttu-id="5ccf3-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5ccf3-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5ccf3-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="5ccf3-131">Can be empty</span></span>  <br/> |<span data-ttu-id="5ccf3-132">False</span><span class="sxs-lookup"><span data-stu-id="5ccf3-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5ccf3-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ccf3-133">See also</span></span>



- [<span data-ttu-id="5ccf3-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5ccf3-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

