---
title: ConversationId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationId
api_type:
- schema
ms.assetid: d5f1ddb3-9af3-4677-a6ba-111b304a951e
description: ConversationId-Element enthält die ID eines Elements oder einer Unterhaltung.
ms.openlocfilehash: 1f82e6ade60fb70db4a9f026fd72d9f11cc63821
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757698"
---
# <a name="conversationid"></a><span data-ttu-id="b4ebe-103">ConversationId</span><span class="sxs-lookup"><span data-stu-id="b4ebe-103">ConversationId</span></span>

<span data-ttu-id="b4ebe-104">**ConversationId** -Element enthält die ID eines Elements oder einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-104">The **ConversationId** element contains the identifier of an item or conversation.</span></span> 
  
```XML
<ConversationId Id="" ChangeKey="" />
```

 <span data-ttu-id="b4ebe-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="b4ebe-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b4ebe-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b4ebe-106">Attributes and elements</span></span>

<span data-ttu-id="b4ebe-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b4ebe-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b4ebe-108">Attributes</span></span>

|<span data-ttu-id="b4ebe-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b4ebe-109">**Attribute**</span></span>|<span data-ttu-id="b4ebe-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b4ebe-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b4ebe-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="b4ebe-111">**Id**</span></span> <br/> |<span data-ttu-id="b4ebe-112">Gibt ein bestimmtes Element in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-112">Identifies a specific item in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="b4ebe-113">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="b4ebe-113">**ChangeKey**</span></span> <br/> | <span data-ttu-id="b4ebe-114">Identifiziert eine bestimmte Version eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-114">Identifies a specific version of an item.</span></span> <span data-ttu-id="b4ebe-115">Eine **ChangeKey** ist erforderlich für die folgenden Szenarien:</span><span class="sxs-lookup"><span data-stu-id="b4ebe-115">A **ChangeKey** is required for the following scenarios:</span></span>  <br/><br/><span data-ttu-id="b4ebe-116">-Das [UpdateItem](updateitem.md) -Element muss ein **ChangeKey** , wenn das Attribut **ConflictResolution** auf auflösen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-116">- The [UpdateItem](updateitem.md) element requires a **ChangeKey** if the **ConflictResolution** attribute is set to AutoResolve.</span></span> <span data-ttu-id="b4ebe-117">Auflösen ist ein Standardwert.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-117">AutoResolve is a default value.</span></span> <span data-ttu-id="b4ebe-118">Wenn das Attribut **ChangeKey** nicht angegeben ist, gibt die Antwort einen [ResponseCode](responsecode.md) Wert **ErrorChangeKeyRequired**gleich zurück.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-118">If the **ChangeKey** attribute is not included, the response will return a [ResponseCode](responsecode.md) value equal to **ErrorChangeKeyRequired**.</span></span><br/><br/><span data-ttu-id="b4ebe-119">- [Den SendItem](senditem.md), [DeleteItem](deleteitem.md)und [DeleteFolder](deletefolder.md) Elemente erfordern eine **ChangeKey** zu prüfen, ob der Vorgang die neueste Version eines Elements bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-119">- [SendItem](senditem.md), [DeleteItem](deleteitem.md), and [DeleteFolder](deletefolder.md) elements require a **ChangeKey** to test whether the attempted operation will act upon the most recent version of an item.</span></span> <span data-ttu-id="b4ebe-120">Wenn das Attribut **ChangeKey** nicht in die **ItemId** enthalten ist oder die **ChangeKey** leer ist, wird die Antwort [ResponseCode](responsecode.md) Wert gleich **ErrorStaleObject**zurück.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-120">If the **ChangeKey** attribute is not included in the **ItemId** or if the **ChangeKey** is empty, the response will return a [ResponseCode](responsecode.md) value equal to **ErrorStaleObject**.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b4ebe-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b4ebe-121">Child elements</span></span>

<span data-ttu-id="b4ebe-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b4ebe-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b4ebe-123">Parent elements</span></span>

|<span data-ttu-id="b4ebe-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="b4ebe-124">**Element**</span></span>|<span data-ttu-id="b4ebe-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b4ebe-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b4ebe-126">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="b4ebe-126">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="b4ebe-127">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-127">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="b4ebe-128">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="b4ebe-128">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="b4ebe-129">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-129">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="b4ebe-130">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="b4ebe-130">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="b4ebe-131">Stellt eine einzelne Aktion auf einem einzelnen Gespräch angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-131">Represents a single action to be applied to a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="b4ebe-132">DistributionList</span><span class="sxs-lookup"><span data-stu-id="b4ebe-132">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="b4ebe-133">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-133">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="b4ebe-134">Element</span><span class="sxs-lookup"><span data-stu-id="b4ebe-134">Item</span></span>](item.md) <br/> |<span data-ttu-id="b4ebe-135">Stellt ein Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-135">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b4ebe-136">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="b4ebe-136">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="b4ebe-137">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-137">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b4ebe-138">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="b4ebe-138">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="b4ebe-139">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-139">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b4ebe-140">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="b4ebe-140">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="b4ebe-141">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-141">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b4ebe-142">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="b4ebe-142">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="b4ebe-143">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-143">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b4ebe-144">Message</span><span class="sxs-lookup"><span data-stu-id="b4ebe-144">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b4ebe-145">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-145">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="b4ebe-146">PostItem-Objekt</span><span class="sxs-lookup"><span data-stu-id="b4ebe-146">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="b4ebe-147">Stellt ein Post-Element im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-147">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b4ebe-148">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="b4ebe-148">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="b4ebe-149">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-149">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b4ebe-150">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="b4ebe-150">Task</span></span>](task.md) <br/> |<span data-ttu-id="b4ebe-151">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-151">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b4ebe-152">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="b4ebe-152">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="b4ebe-153">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-153">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b4ebe-154">Textwert</span><span class="sxs-lookup"><span data-stu-id="b4ebe-154">Text value</span></span>

<span data-ttu-id="b4ebe-155">Keine.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-155">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b4ebe-156">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b4ebe-156">Remarks</span></span>

<span data-ttu-id="b4ebe-157">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b4ebe-157">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b4ebe-158">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b4ebe-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4ebe-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="b4ebe-159">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b4ebe-160">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b4ebe-160">Schema Name</span></span>  <br/> |<span data-ttu-id="b4ebe-161">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b4ebe-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="b4ebe-162">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b4ebe-162">Validation File</span></span>  <br/> |<span data-ttu-id="b4ebe-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b4ebe-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b4ebe-164">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b4ebe-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="b4ebe-165">False</span><span class="sxs-lookup"><span data-stu-id="b4ebe-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b4ebe-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4ebe-166">See also</span></span>

- [<span data-ttu-id="b4ebe-167">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="b4ebe-167">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="b4ebe-168">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b4ebe-168">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

