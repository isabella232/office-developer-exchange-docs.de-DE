---
title: Kategorien
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Categories
api_type:
- schema
ms.assetid: d84d4927-b524-4e62-bf3d-1f12fec8c21a
description: Das categories-Element enthält eine Auflistung von Zeichenfolgen, die die Kategorien identifizieren, zu denen ein Element im Postfach gehört.
ms.openlocfilehash: 0d9f7068aa81306a10436ed0ca0d45f6d3b2c3a3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462213"
---
# <a name="categories"></a><span data-ttu-id="9592f-103">Kategorien</span><span class="sxs-lookup"><span data-stu-id="9592f-103">Categories</span></span>

<span data-ttu-id="9592f-104">Das **Categories** -Element enthält eine Auflistung von Zeichenfolgen, die die Kategorien identifizieren, zu denen ein Element im Postfach gehört.</span><span class="sxs-lookup"><span data-stu-id="9592f-104">The **Categories** element contains a collection of strings that identify the categories to which an item in the mailbox belongs.</span></span> 
  
```XML
<Categories>
   <String/>
</Categories>
```

 <span data-ttu-id="9592f-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="9592f-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9592f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9592f-106">Attributes and elements</span></span>

<span data-ttu-id="9592f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9592f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9592f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9592f-108">Attributes</span></span>

<span data-ttu-id="9592f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9592f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9592f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9592f-110">Child elements</span></span>

|<span data-ttu-id="9592f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9592f-111">**Element**</span></span>|<span data-ttu-id="9592f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9592f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9592f-113">String</span><span class="sxs-lookup"><span data-stu-id="9592f-113">String</span></span>](string.md) <br/> |<span data-ttu-id="9592f-114">Enthält eine Zeichenfolge, die eine einzelne Kategorie identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9592f-114">Contains a string that identifies a single category.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9592f-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9592f-115">Parent elements</span></span>

|<span data-ttu-id="9592f-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="9592f-116">**Element**</span></span>|<span data-ttu-id="9592f-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9592f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9592f-118">Element</span><span class="sxs-lookup"><span data-stu-id="9592f-118">Item</span></span>](item.md) <br/> |<span data-ttu-id="9592f-119">Stellt ein Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9592f-119">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9592f-120">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="9592f-120">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="9592f-121">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="9592f-121">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9592f-122">Message</span><span class="sxs-lookup"><span data-stu-id="9592f-122">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="9592f-123">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="9592f-123">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="9592f-124">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="9592f-124">Task</span></span>](task.md) <br/> |<span data-ttu-id="9592f-125">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9592f-125">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9592f-126">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="9592f-126">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="9592f-127">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="9592f-127">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="9592f-128">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="9592f-128">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="9592f-129">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="9592f-129">Represents a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="9592f-130">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="9592f-130">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="9592f-131">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9592f-131">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9592f-132">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="9592f-132">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="9592f-133">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9592f-133">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9592f-134">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="9592f-134">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="9592f-135">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9592f-135">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9592f-136">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="9592f-136">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="9592f-137">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9592f-137">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9592f-138">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="9592f-138">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="9592f-139">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="9592f-139">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="9592f-140">DistributionList</span><span class="sxs-lookup"><span data-stu-id="9592f-140">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="9592f-141">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="9592f-141">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="9592f-142">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="9592f-142">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="9592f-143">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="9592f-143">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="9592f-144">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="9592f-144">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="9592f-145">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel dar.</span><span class="sxs-lookup"><span data-stu-id="9592f-145">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="9592f-146">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="9592f-146">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="9592f-147">Enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9592f-147">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9592f-148">Textwert</span><span class="sxs-lookup"><span data-stu-id="9592f-148">Text value</span></span>

<span data-ttu-id="9592f-149">Keine.</span><span class="sxs-lookup"><span data-stu-id="9592f-149">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9592f-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9592f-150">Remarks</span></span>

<span data-ttu-id="9592f-151">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9592f-151">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9592f-152">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9592f-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9592f-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="9592f-153">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9592f-154">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9592f-154">Schema Name</span></span>  <br/> |<span data-ttu-id="9592f-155">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9592f-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="9592f-156">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9592f-156">Validation File</span></span>  <br/> |<span data-ttu-id="9592f-157">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9592f-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9592f-158">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9592f-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="9592f-159">False</span><span class="sxs-lookup"><span data-stu-id="9592f-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9592f-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9592f-160">See also</span></span>



- [<span data-ttu-id="9592f-161">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9592f-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

