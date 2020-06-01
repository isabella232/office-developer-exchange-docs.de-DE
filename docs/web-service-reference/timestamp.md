---
title: Timestamp
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeStamp
api_type:
- schema
ms.assetid: 5eae859a-5a74-4bf6-b196-d1b2fd38501a
description: Das Timestamp-Element stellt den Zeitstempel eines Post Fach Ereignisses dar.
ms.openlocfilehash: f2280d4eab67b603963c4f0a7468bf35a2b63a88
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459889"
---
# <a name="timestamp"></a><span data-ttu-id="71e11-103">Timestamp</span><span class="sxs-lookup"><span data-stu-id="71e11-103">TimeStamp</span></span>

<span data-ttu-id="71e11-104">Das **timestamp** -Element stellt den Zeitstempel eines Post Fach Ereignisses dar.</span><span class="sxs-lookup"><span data-stu-id="71e11-104">The **Timestamp** element represents the timestamp of a mailbox event.</span></span> 
  
```xml
<TimeStamp/>
```

 <span data-ttu-id="71e11-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="71e11-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="71e11-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="71e11-106">Attributes and elements</span></span>

<span data-ttu-id="71e11-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="71e11-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="71e11-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="71e11-108">Attributes</span></span>

<span data-ttu-id="71e11-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="71e11-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="71e11-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="71e11-110">Child elements</span></span>

<span data-ttu-id="71e11-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="71e11-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="71e11-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="71e11-112">Parent elements</span></span>

|<span data-ttu-id="71e11-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="71e11-113">**Element**</span></span>|<span data-ttu-id="71e11-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="71e11-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="71e11-115">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="71e11-115">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="71e11-116">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="71e11-116">Represents an event where an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="71e11-117">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="71e11-117">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="71e11-118">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="71e11-118">Represents an event where an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="71e11-119">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="71e11-119">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="71e11-120">Stellt ein Ereignis dar, bei dem ein Element oder ein Ordner gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="71e11-120">Represents an event where an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="71e11-121">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="71e11-121">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="71e11-122">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner geändert wird.</span><span class="sxs-lookup"><span data-stu-id="71e11-122">Represents an event where an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="71e11-123">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="71e11-123">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="71e11-124">Stellt ein Ereignis dar, bei dem ein Element oder ein Ordner von einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="71e11-124">Represents an event where an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="71e11-125">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="71e11-125">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="71e11-126">Stellt ein Ereignis dar, das durch ein neues e-Mail-Element in einem Postfach ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="71e11-126">Represents an event triggered by a new mail item in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="71e11-127">Textwert</span><span class="sxs-lookup"><span data-stu-id="71e11-127">Text value</span></span>

<span data-ttu-id="71e11-128">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="71e11-128">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="71e11-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71e11-129">Remarks</span></span>

<span data-ttu-id="71e11-130">Dieses Element steht in erster Linie zur Verwendung in der Client Ermittlung der Ereignishäufigkeit zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="71e11-130">This element is primarily available for use in client determination of event frequency.</span></span> <span data-ttu-id="71e11-131">Dies ist in [StatusEvent](statusevent.md)nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="71e11-131">This is not present in [StatusEvent](statusevent.md).</span></span>
  
<span data-ttu-id="71e11-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="71e11-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="71e11-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="71e11-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71e11-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="71e11-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="71e11-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="71e11-135">Schema name</span></span>  <br/> |<span data-ttu-id="71e11-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="71e11-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="71e11-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="71e11-137">Validation file</span></span>  <br/> |<span data-ttu-id="71e11-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="71e11-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="71e11-139">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="71e11-139">Can be empty</span></span>  <br/> |<span data-ttu-id="71e11-140">False</span><span class="sxs-lookup"><span data-stu-id="71e11-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="71e11-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71e11-141">See also</span></span>



[<span data-ttu-id="71e11-142">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="71e11-142">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="71e11-143">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="71e11-143">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="71e11-144">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="71e11-144">Unsubscribe operation</span></span>](unsubscribe-operation.md)

