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
description: Das Conversation-ID-Element enthält den Bezeichner eines Elements oder einer Unterhaltung.
ms.openlocfilehash: 4f12d70ae6b72773760a731f5778cf6743ce699f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461471"
---
# <a name="conversationid"></a><span data-ttu-id="7dbf0-103">ConversationId</span><span class="sxs-lookup"><span data-stu-id="7dbf0-103">ConversationId</span></span>

<span data-ttu-id="7dbf0-104">Das **Conversation** -ID-Element enthält den Bezeichner eines Elements oder einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-104">The **ConversationId** element contains the identifier of an item or conversation.</span></span> 
  
```XML
<ConversationId Id="" ChangeKey="" />
```

 <span data-ttu-id="7dbf0-105">**Itemidtype**</span><span class="sxs-lookup"><span data-stu-id="7dbf0-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7dbf0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7dbf0-106">Attributes and elements</span></span>

<span data-ttu-id="7dbf0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7dbf0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7dbf0-108">Attributes</span></span>

|<span data-ttu-id="7dbf0-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7dbf0-109">**Attribute**</span></span>|<span data-ttu-id="7dbf0-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7dbf0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7dbf0-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="7dbf0-111">**Id**</span></span> <br/> |<span data-ttu-id="7dbf0-112">Identifiziert ein bestimmtes Element in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-112">Identifies a specific item in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="7dbf0-113">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="7dbf0-113">**ChangeKey**</span></span> <br/> | <span data-ttu-id="7dbf0-114">Gibt eine bestimmte Version eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-114">Identifies a specific version of an item.</span></span> <span data-ttu-id="7dbf0-115">Für die folgenden Szenarien ist ein **ChangeKey** erforderlich:</span><span class="sxs-lookup"><span data-stu-id="7dbf0-115">A **ChangeKey** is required for the following scenarios:</span></span>  <br/><br/><span data-ttu-id="7dbf0-116">-Das [UpdateItem](updateitem.md) -Element erfordert ein **ChangeKey** , wenn das **ConflictResolution** -Attribut auf autoresolve festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-116">- The [UpdateItem](updateitem.md) element requires a **ChangeKey** if the **ConflictResolution** attribute is set to AutoResolve.</span></span> <span data-ttu-id="7dbf0-117">Autoresolve ist ein Standardwert.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-117">AutoResolve is a default value.</span></span> <span data-ttu-id="7dbf0-118">Wenn das **ChangeKey** -Attribut nicht enthalten ist, gibt die Antwort einen [Response Code](responsecode.md) -Wert zurück, der **ErrorChangeKeyRequired**entspricht.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-118">If the **ChangeKey** attribute is not included, the response will return a [ResponseCode](responsecode.md) value equal to **ErrorChangeKeyRequired**.</span></span><br/><br/><span data-ttu-id="7dbf0-119">- [SendItem](senditem.md)-, [DeleteItem](deleteitem.md)-und [DeleteFolder](deletefolder.md) -Elemente erfordern ein **ChangeKey** , um zu testen, ob der versuchte Vorgang auf die neueste Version eines Elements angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-119">- [SendItem](senditem.md), [DeleteItem](deleteitem.md), and [DeleteFolder](deletefolder.md) elements require a **ChangeKey** to test whether the attempted operation will act upon the most recent version of an item.</span></span> <span data-ttu-id="7dbf0-120">Wenn das **ChangeKey** -Attribut nicht in der **ItemID** -Eigenschaft enthalten ist oder wenn das **ChangeKey** -Objekt leer ist, gibt die Antwort einen [Response Code](responsecode.md) -Wert zurück, der **ErrorStaleObject**entspricht.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-120">If the **ChangeKey** attribute is not included in the **ItemId** or if the **ChangeKey** is empty, the response will return a [ResponseCode](responsecode.md) value equal to **ErrorStaleObject**.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7dbf0-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7dbf0-121">Child elements</span></span>

<span data-ttu-id="7dbf0-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7dbf0-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7dbf0-123">Parent elements</span></span>

|<span data-ttu-id="7dbf0-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="7dbf0-124">**Element**</span></span>|<span data-ttu-id="7dbf0-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7dbf0-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7dbf0-126">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="7dbf0-126">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="7dbf0-127">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-127">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="7dbf0-128">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="7dbf0-128">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="7dbf0-129">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-129">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="7dbf0-130">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="7dbf0-130">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="7dbf0-131">Stellt eine einzelne Aktion dar, die auf eine einzelne Unterhaltung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-131">Represents a single action to be applied to a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="7dbf0-132">DistributionList</span><span class="sxs-lookup"><span data-stu-id="7dbf0-132">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="7dbf0-133">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-133">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="7dbf0-134">Element</span><span class="sxs-lookup"><span data-stu-id="7dbf0-134">Item</span></span>](item.md) <br/> |<span data-ttu-id="7dbf0-135">Stellt ein Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-135">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7dbf0-136">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="7dbf0-136">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="7dbf0-137">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-137">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7dbf0-138">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="7dbf0-138">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="7dbf0-139">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-139">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7dbf0-140">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="7dbf0-140">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="7dbf0-141">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-141">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7dbf0-142">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="7dbf0-142">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="7dbf0-143">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-143">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7dbf0-144">Message</span><span class="sxs-lookup"><span data-stu-id="7dbf0-144">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7dbf0-145">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-145">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="7dbf0-146">PostItem</span><span class="sxs-lookup"><span data-stu-id="7dbf0-146">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="7dbf0-147">Stellt ein Post-Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-147">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7dbf0-148">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="7dbf0-148">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="7dbf0-149">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-149">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7dbf0-150">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="7dbf0-150">Task</span></span>](task.md) <br/> |<span data-ttu-id="7dbf0-151">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-151">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7dbf0-152">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="7dbf0-152">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="7dbf0-153">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-153">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7dbf0-154">Textwert</span><span class="sxs-lookup"><span data-stu-id="7dbf0-154">Text value</span></span>

<span data-ttu-id="7dbf0-155">Keine.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-155">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7dbf0-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7dbf0-156">Remarks</span></span>

<span data-ttu-id="7dbf0-157">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7dbf0-157">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7dbf0-158">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7dbf0-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7dbf0-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="7dbf0-159">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7dbf0-160">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7dbf0-160">Schema Name</span></span>  <br/> |<span data-ttu-id="7dbf0-161">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7dbf0-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="7dbf0-162">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7dbf0-162">Validation File</span></span>  <br/> |<span data-ttu-id="7dbf0-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7dbf0-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7dbf0-164">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7dbf0-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="7dbf0-165">False</span><span class="sxs-lookup"><span data-stu-id="7dbf0-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7dbf0-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7dbf0-166">See also</span></span>

- [<span data-ttu-id="7dbf0-167">FindConversation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7dbf0-167">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="7dbf0-168">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7dbf0-168">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

