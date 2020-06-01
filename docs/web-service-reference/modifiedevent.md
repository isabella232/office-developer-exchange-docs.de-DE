---
title: ModifiedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ModifiedEvent
api_type:
- schema
ms.assetid: ca1309f4-2df7-4289-811c-75c3db0e7072
description: Das ModifiedEvent-Element stellt ein Ereignis dar, in dem ein Element oder ein Ordner geändert wird.
ms.openlocfilehash: 1a798773601a0857b9064c7fa6a532a7a36517ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468551"
---
# <a name="modifiedevent"></a><span data-ttu-id="9d5c6-103">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="9d5c6-103">ModifiedEvent</span></span>

<span data-ttu-id="9d5c6-104">Das **ModifiedEvent** -Element stellt ein Ereignis dar, in dem ein Element oder ein Ordner geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9d5c6-104">The **ModifiedEvent** element represents an event in which an item or folder is modified.</span></span> 
  
```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/> 
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

<span data-ttu-id="9d5c6-105">**ModifiedEventType**</span><span class="sxs-lookup"><span data-stu-id="9d5c6-105">**ModifiedEventType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9d5c6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9d5c6-106">Attributes and elements</span></span>

<span data-ttu-id="9d5c6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9d5c6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d5c6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9d5c6-108">Attributes</span></span>

<span data-ttu-id="9d5c6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9d5c6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9d5c6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d5c6-110">Child elements</span></span>

|<span data-ttu-id="9d5c6-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d5c6-111">**Element**</span></span>|<span data-ttu-id="9d5c6-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d5c6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d5c6-113">Watermark</span><span class="sxs-lookup"><span data-stu-id="9d5c6-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="9d5c6-114">Stellt eine Ereignis Textmarke in der Tabelle Post Fach Ereignisse dar.</span><span class="sxs-lookup"><span data-stu-id="9d5c6-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="9d5c6-115">Timestamp</span><span class="sxs-lookup"><span data-stu-id="9d5c6-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="9d5c6-116">Stellt den Zeitstempel eines geänderten Element-oder Ordner Postfach-Ereignisses dar.</span><span class="sxs-lookup"><span data-stu-id="9d5c6-116">Represents the timestamp of a modified item or folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="9d5c6-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="9d5c6-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="9d5c6-118">Stellt den Bezeichner des geänderten Ordners dar.</span><span class="sxs-lookup"><span data-stu-id="9d5c6-118">Represents the identifier of the modified folder.</span></span>  <br/> |
|[<span data-ttu-id="9d5c6-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="9d5c6-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="9d5c6-120">Stellt den Bezeichner des geänderten Elements dar.</span><span class="sxs-lookup"><span data-stu-id="9d5c6-120">Represents the identifier of the modified item.</span></span>  <br/> |
|[<span data-ttu-id="9d5c6-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="9d5c6-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="9d5c6-122">Stellt den Bezeichner des übergeordneten Ordners des geänderten Elements oder Ordners dar.</span><span class="sxs-lookup"><span data-stu-id="9d5c6-122">Represents the identifier of the parent folder of the modified item or folder.</span></span>  <br/> |
|[<span data-ttu-id="9d5c6-123">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="9d5c6-123">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="9d5c6-124">Stellt die Anzahl der ungelesenen Elemente in einem bestimmten Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="9d5c6-124">Represents the count of unread items within a given folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9d5c6-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d5c6-125">Parent elements</span></span>

|<span data-ttu-id="9d5c6-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d5c6-126">**Element**</span></span>|<span data-ttu-id="9d5c6-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d5c6-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d5c6-128">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="9d5c6-128">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="9d5c6-129">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="9d5c6-129">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d5c6-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d5c6-130">Remarks</span></span>

<span data-ttu-id="9d5c6-131">Für jede Änderung eines Elements in einem Ordner werden zwei geänderte Ereignisse generiert.</span><span class="sxs-lookup"><span data-stu-id="9d5c6-131">Two modified events are generated for each modification of an item in a folder.</span></span> <span data-ttu-id="9d5c6-132">Ein Ereignis ist für das geänderte Element relevant.</span><span class="sxs-lookup"><span data-stu-id="9d5c6-132">One event is relevant to the item that changed.</span></span> <span data-ttu-id="9d5c6-133">Das andere Ereignis ist für den übergeordneten Ordner des Elements relevant.</span><span class="sxs-lookup"><span data-stu-id="9d5c6-133">The other event is relevant to the parent folder of the item.</span></span> <span data-ttu-id="9d5c6-134">Dies ist derselbe Ordner, für den das Abonnement erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9d5c6-134">This is the same folder that the subscription was created against.</span></span> <span data-ttu-id="9d5c6-135">Das Ereignis, das dem Ordner zugeordnet ist, wird verwendet, um eine mögliche Änderung an der [UnreadCount](unreadcount.md) -Eigenschaft für den Ordner zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="9d5c6-135">The event that is associated with the folder is used to communicate a potential change to the [UnreadCount](unreadcount.md) property on the folder.</span></span> 
  
<span data-ttu-id="9d5c6-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="9d5c6-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d5c6-137">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9d5c6-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d5c6-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d5c6-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9d5c6-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9d5c6-139">Schema name</span></span>  <br/> |<span data-ttu-id="9d5c6-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9d5c6-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="9d5c6-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9d5c6-141">Validation file</span></span>  <br/> |<span data-ttu-id="9d5c6-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9d5c6-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9d5c6-143">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="9d5c6-143">Can be empty</span></span>  <br/> |<span data-ttu-id="9d5c6-144">False</span><span class="sxs-lookup"><span data-stu-id="9d5c6-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d5c6-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d5c6-145">See also</span></span>

- [<span data-ttu-id="9d5c6-146">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="9d5c6-146">Subscribe operation</span></span>](subscribe-operation.md)  
- [<span data-ttu-id="9d5c6-147">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9d5c6-147">GetEvents operation</span></span>](getevents-operation.md)  
- [<span data-ttu-id="9d5c6-148">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="9d5c6-148">Unsubscribe operation</span></span>](unsubscribe-operation.md)

