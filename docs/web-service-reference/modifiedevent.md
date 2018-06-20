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
description: Das ModifiedEvent-Element stellt ein Ereignis in der eines Elements oder Ordners geändert wird.
ms.openlocfilehash: fb464fb0a270d8ca7d33d40e5425e260970b2f1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830482"
---
# <a name="modifiedevent"></a><span data-ttu-id="3b26a-103">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="3b26a-103">ModifiedEvent</span></span>

<span data-ttu-id="3b26a-104">Das **ModifiedEvent** -Element stellt ein Ereignis in der eines Elements oder Ordners geändert wird.</span><span class="sxs-lookup"><span data-stu-id="3b26a-104">The **ModifiedEvent** element represents an event in which an item or folder is modified.</span></span> 
  
```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

 <span data-ttu-id="3b26a-105">**ModifiedEventType**</span><span class="sxs-lookup"><span data-stu-id="3b26a-105">**ModifiedEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3b26a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3b26a-106">Attributes and elements</span></span>

<span data-ttu-id="3b26a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3b26a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b26a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3b26a-108">Attributes</span></span>

<span data-ttu-id="3b26a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3b26a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3b26a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b26a-110">Child elements</span></span>

|<span data-ttu-id="3b26a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3b26a-111">**Element**</span></span>|<span data-ttu-id="3b26a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b26a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b26a-113">Wasserzeichen</span><span class="sxs-lookup"><span data-stu-id="3b26a-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="3b26a-114">Stellt eine Textmarke Ereignis in der Tabelle der Postfach-Ereignisse dar.</span><span class="sxs-lookup"><span data-stu-id="3b26a-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="3b26a-115">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="3b26a-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="3b26a-116">Den Zeitstempel des geänderten Elements oder Ordners Postfach-Ereignisses darstellt.</span><span class="sxs-lookup"><span data-stu-id="3b26a-116">Represents the timestamp of a modified item or folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="3b26a-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="3b26a-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="3b26a-118">Den Bezeichner des geänderten Ordners darstellt.</span><span class="sxs-lookup"><span data-stu-id="3b26a-118">Represents the identifier of the modified folder.</span></span>  <br/> |
|[<span data-ttu-id="3b26a-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="3b26a-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="3b26a-120">Den Bezeichner des geänderten Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="3b26a-120">Represents the identifier of the modified item.</span></span>  <br/> |
|[<span data-ttu-id="3b26a-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="3b26a-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="3b26a-122">Den Bezeichner des übergeordneten Ordners des geänderten Elements oder Ordners darstellt.</span><span class="sxs-lookup"><span data-stu-id="3b26a-122">Represents the identifier of the parent folder of the modified item or folder.</span></span>  <br/> |
|[<span data-ttu-id="3b26a-123">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="3b26a-123">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="3b26a-124">Die Anzahl der ungelesenen Elemente innerhalb eines bestimmten Ordners darstellt.</span><span class="sxs-lookup"><span data-stu-id="3b26a-124">Represents the count of unread items within a given folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3b26a-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b26a-125">Parent elements</span></span>

|<span data-ttu-id="3b26a-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="3b26a-126">**Element**</span></span>|<span data-ttu-id="3b26a-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b26a-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b26a-128">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="3b26a-128">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3b26a-129">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="3b26a-129">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b26a-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3b26a-130">Remarks</span></span>

<span data-ttu-id="3b26a-131">Für jede Änderung eines Elements in einem Ordner werden zwei geänderte Ereignisse generiert.</span><span class="sxs-lookup"><span data-stu-id="3b26a-131">Two modified events are generated for each modification of an item in a folder.</span></span> <span data-ttu-id="3b26a-132">Ein Ereignis ist relevant für das Element, das geändert.</span><span class="sxs-lookup"><span data-stu-id="3b26a-132">One event is relevant to the item that changed.</span></span> <span data-ttu-id="3b26a-133">Das anderen Ereignis mit ist dem übergeordneten Ordner des Elements relevant.</span><span class="sxs-lookup"><span data-stu-id="3b26a-133">The other event is relevant to the parent folder of the item.</span></span> <span data-ttu-id="3b26a-134">Dies ist die gleichen Ordner wie, dem gegen das Abonnement erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3b26a-134">This is the same folder that the subscription was created against.</span></span> <span data-ttu-id="3b26a-135">Das Ereignis, das den Ordner zugeordnet ist wird verwendet, um eine mögliche Änderung der [UnreadCount](unreadcount.md) -Eigenschaft auf den Ordner zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="3b26a-135">The event that is associated with the folder is used to communicate a potential change to the [UnreadCount](unreadcount.md) property on the folder.</span></span> 
  
<span data-ttu-id="3b26a-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="3b26a-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3b26a-137">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3b26a-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b26a-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="3b26a-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3b26a-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3b26a-139">Schema name</span></span>  <br/> |<span data-ttu-id="3b26a-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3b26a-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="3b26a-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3b26a-141">Validation file</span></span>  <br/> |<span data-ttu-id="3b26a-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3b26a-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3b26a-143">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="3b26a-143">Can be empty</span></span>  <br/> |<span data-ttu-id="3b26a-144">False</span><span class="sxs-lookup"><span data-stu-id="3b26a-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b26a-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b26a-145">See also</span></span>



[<span data-ttu-id="3b26a-146">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="3b26a-146">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="3b26a-147">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3b26a-147">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="3b26a-148">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="3b26a-148">Unsubscribe operation</span></span>](unsubscribe-operation.md)

