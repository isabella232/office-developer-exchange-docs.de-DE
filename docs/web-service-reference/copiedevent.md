---
title: CopiedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopiedEvent
api_type:
- schema
ms.assetid: 82f2fcac-deaa-4ff8-801f-4fe28d8a19f5
description: Das CopiedEvent-Element stellt ein Ereignis dar, in dem ein Element oder ein Ordner kopiert wird.
ms.openlocfilehash: 928910ddbe0bf1e48549d1665ab373f7382366d1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529245"
---
# <a name="copiedevent"></a><span data-ttu-id="531ec-103">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="531ec-103">CopiedEvent</span></span>

<span data-ttu-id="531ec-104">Das **CopiedEvent** -Element stellt ein Ereignis dar, in dem ein Element oder ein Ordner kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="531ec-104">The **CopiedEvent** element represents an event in which an item or folder is copied.</span></span> 
  
```xml
<CopiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <OldFolderId/>
   <OldParentFolderId/>
</CopiedEvent>
```

```xml
<CopiedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
   <OldFolderId/>
   <OldParentFolderId/>
</CopiedEvent>
```

<span data-ttu-id="531ec-105">**MovedCopiedEventType**</span><span class="sxs-lookup"><span data-stu-id="531ec-105">**MovedCopiedEventType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="531ec-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="531ec-106">Attributes and elements</span></span>

<span data-ttu-id="531ec-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="531ec-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="531ec-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="531ec-108">Attributes</span></span>

<span data-ttu-id="531ec-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="531ec-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="531ec-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="531ec-110">Child elements</span></span>

|<span data-ttu-id="531ec-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="531ec-111">**Element**</span></span>|<span data-ttu-id="531ec-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="531ec-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="531ec-113">Watermark</span><span class="sxs-lookup"><span data-stu-id="531ec-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="531ec-114">Stellt ein Lesezeichen für Ereignisse in der Tabelle Post Fach Ereignisse dar.</span><span class="sxs-lookup"><span data-stu-id="531ec-114">Represents an events bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="531ec-115">Timestamp</span><span class="sxs-lookup"><span data-stu-id="531ec-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="531ec-116">Stellt den Zeitstempel eines Post Fach Ereignisses zum Kopieren von Elementen/Ordnern dar.</span><span class="sxs-lookup"><span data-stu-id="531ec-116">Represents the timestamp of a copy item/folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="531ec-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="531ec-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="531ec-118">Stellt den Bezeichner des Ordners dar.</span><span class="sxs-lookup"><span data-stu-id="531ec-118">Represents the identifier of the folder.</span></span>  <br/> |
|[<span data-ttu-id="531ec-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="531ec-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="531ec-120">Stellt den Bezeichner des Elements dar.</span><span class="sxs-lookup"><span data-stu-id="531ec-120">Represents the identifier of the item.</span></span>  <br/> |
|[<span data-ttu-id="531ec-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="531ec-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="531ec-122">Stellt den Bezeichner des Ordners dar, der die Kopie enthält.</span><span class="sxs-lookup"><span data-stu-id="531ec-122">Represents the identifier of the folder that contains the copy.</span></span>  <br/> |
|[<span data-ttu-id="531ec-123">OldFolderId</span><span class="sxs-lookup"><span data-stu-id="531ec-123">OldFolderId</span></span>](oldfolderid.md) <br/> |<span data-ttu-id="531ec-124">Stellt die Ordner-ID des ursprünglichen Ordners vor dem Kopieren dar.</span><span class="sxs-lookup"><span data-stu-id="531ec-124">Represents the folder identifier of the original folder before it was copied.</span></span>  <br/> |
|[<span data-ttu-id="531ec-125">OldItemId</span><span class="sxs-lookup"><span data-stu-id="531ec-125">OldItemId</span></span>](olditemid.md) <br/> |<span data-ttu-id="531ec-126">Enthält den eindeutigen Bezeichner des ursprünglichen Elements, bevor es kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="531ec-126">Contains the unique identifier of the original item before it was copied.</span></span>  <br/> |
|[<span data-ttu-id="531ec-127">OldParentFolderId</span><span class="sxs-lookup"><span data-stu-id="531ec-127">OldParentFolderId</span></span>](oldparentfolderid.md) <br/> |<span data-ttu-id="531ec-128">Enthält den Bezeichner des ursprünglichen übergeordneten Ordners eines Elements oder Ordners, das kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="531ec-128">Contains the identifier of the original parent folder of an item or folder that was copied.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="531ec-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="531ec-129">Parent elements</span></span>

|<span data-ttu-id="531ec-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="531ec-130">**Element**</span></span>|<span data-ttu-id="531ec-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="531ec-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="531ec-132">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="531ec-132">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="531ec-133">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="531ec-133">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="531ec-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="531ec-134">Remarks</span></span>

<span data-ttu-id="531ec-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="531ec-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="531ec-136">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="531ec-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="531ec-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="531ec-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="531ec-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="531ec-138">Schema name</span></span>  <br/> |<span data-ttu-id="531ec-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="531ec-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="531ec-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="531ec-140">Validation file</span></span>  <br/> |<span data-ttu-id="531ec-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="531ec-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="531ec-142">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="531ec-142">Can be empty</span></span>  <br/> |<span data-ttu-id="531ec-143">False</span><span class="sxs-lookup"><span data-stu-id="531ec-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="531ec-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="531ec-144">See also</span></span>

- [<span data-ttu-id="531ec-145">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="531ec-145">Subscribe operation</span></span>](subscribe-operation.md) 
- [<span data-ttu-id="531ec-146">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="531ec-146">GetEvents operation</span></span>](getevents-operation.md) 
- [<span data-ttu-id="531ec-147">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="531ec-147">Unsubscribe operation</span></span>](unsubscribe-operation.md)
- [<span data-ttu-id="531ec-148">Verwenden von Pullabonnements</span><span class="sxs-lookup"><span data-stu-id="531ec-148">Using Pull Subscriptions</span></span>](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx) 
- [<span data-ttu-id="531ec-149">Beispielanwendung für Pushbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="531ec-149">Push Notification Sample Application</span></span>](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

