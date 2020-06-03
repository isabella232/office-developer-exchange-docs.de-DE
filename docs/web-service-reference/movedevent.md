---
title: MovedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MovedEvent
api_type:
- schema
ms.assetid: 572f8b40-dfa8-47bc-b0c1-e1a7138506fd
description: Das MovedEvent-Element stellt ein Ereignis dar, in dem ein Element oder ein Ordner von einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird.
ms.openlocfilehash: 1f8fb57dba7edb769fe0dd658d89c032dccf8c5f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530408"
---
# <a name="movedevent"></a><span data-ttu-id="695a2-103">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="695a2-103">MovedEvent</span></span>

<span data-ttu-id="695a2-104">Das **MovedEvent** -Element stellt ein Ereignis dar, in dem ein Element oder ein Ordner von einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="695a2-104">The **MovedEvent** element represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span> 
  
```xml
<MovedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
   <OldItemId/>
   <OldParentFolderId/>
</MovedEvent>
```

```xml
<MovedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <OldFolderId/>
   <OldParentFolderId/>
</MovedEvent>
```


<span data-ttu-id="695a2-105">**MovedCopiedEventType**</span><span class="sxs-lookup"><span data-stu-id="695a2-105">**MovedCopiedEventType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="695a2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="695a2-106">Attributes and elements</span></span>

<span data-ttu-id="695a2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="695a2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="695a2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="695a2-108">Attributes</span></span>

<span data-ttu-id="695a2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="695a2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="695a2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="695a2-110">Child elements</span></span>

|<span data-ttu-id="695a2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="695a2-111">**Element**</span></span>|<span data-ttu-id="695a2-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="695a2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="695a2-113">Watermark</span><span class="sxs-lookup"><span data-stu-id="695a2-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="695a2-114">Stellt ein Lesezeichen für Ereignisse in der Tabelle Post Fach Ereignisse dar.</span><span class="sxs-lookup"><span data-stu-id="695a2-114">Represents an events bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="695a2-115">Timestamp</span><span class="sxs-lookup"><span data-stu-id="695a2-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="695a2-116">Stellt den Zeitstempel des Post Fach Ereignisses "Element/Ordner Verschiebe" dar.</span><span class="sxs-lookup"><span data-stu-id="695a2-116">Represents the timestamp of a move item/folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="695a2-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="695a2-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="695a2-118">Stellt den Bezeichner des verschobenen Ordners dar.</span><span class="sxs-lookup"><span data-stu-id="695a2-118">Represents the identifier of the moved folder.</span></span>  <br/> |
|[<span data-ttu-id="695a2-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="695a2-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="695a2-120">Stellt den Bezeichner des verschobenen Elements dar.</span><span class="sxs-lookup"><span data-stu-id="695a2-120">Represents the identifier of the moved item.</span></span>  <br/> |
|[<span data-ttu-id="695a2-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="695a2-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="695a2-122">Stellt den Bezeichner des Ordners dar, der das verschobene Element oder den verschobenen Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="695a2-122">Represents the identifier of the folder that contains the moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="695a2-123">OldFolderId</span><span class="sxs-lookup"><span data-stu-id="695a2-123">OldFolderId</span></span>](oldfolderid.md) <br/> |<span data-ttu-id="695a2-124">Enthält den Ordner Bezeichner des ursprünglichen Ordners, bevor er verschoben oder kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="695a2-124">Contains the folder identifier of the original folder before it was moved or copied.</span></span>  <br/> |
|[<span data-ttu-id="695a2-125">OldItemId</span><span class="sxs-lookup"><span data-stu-id="695a2-125">OldItemId</span></span>](olditemid.md) <br/> |<span data-ttu-id="695a2-126">Enthält die eindeutige ID des ursprünglichen Elements, bevor es verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="695a2-126">Contains the unique identifier of the original item before it was moved.</span></span>  <br/> |
|[<span data-ttu-id="695a2-127">OldParentFolderId</span><span class="sxs-lookup"><span data-stu-id="695a2-127">OldParentFolderId</span></span>](oldparentfolderid.md) <br/> |<span data-ttu-id="695a2-128">Enthält den Bezeichner des ursprünglichen übergeordneten Ordners eines verschobenen Elements oder Ordners.</span><span class="sxs-lookup"><span data-stu-id="695a2-128">Contains the identifier of the original parent folder of an item or folder that was moved.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="695a2-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="695a2-129">Parent elements</span></span>

|<span data-ttu-id="695a2-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="695a2-130">**Element**</span></span>|<span data-ttu-id="695a2-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="695a2-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="695a2-132">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="695a2-132">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="695a2-133">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="695a2-133">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="695a2-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="695a2-134">Remarks</span></span>

<span data-ttu-id="695a2-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="695a2-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="695a2-136">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="695a2-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="695a2-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="695a2-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="695a2-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="695a2-138">Schema name</span></span>  <br/> |<span data-ttu-id="695a2-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="695a2-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="695a2-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="695a2-140">Validation file</span></span>  <br/> |<span data-ttu-id="695a2-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="695a2-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="695a2-142">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="695a2-142">Can be empty</span></span>  <br/> |<span data-ttu-id="695a2-143">False</span><span class="sxs-lookup"><span data-stu-id="695a2-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="695a2-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="695a2-144">See also</span></span>

- [<span data-ttu-id="695a2-145">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="695a2-145">Subscribe operation</span></span>](subscribe-operation.md) 
- [<span data-ttu-id="695a2-146">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="695a2-146">GetEvents operation</span></span>](getevents-operation.md) 
- [<span data-ttu-id="695a2-147">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="695a2-147">Unsubscribe operation</span></span>](unsubscribe-operation.md)

