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
description: Das MovedEvent-Element stellt ein Ereignis in der eines Elements oder Ordners von einem übergeordneten Ordner in einer anderen übergeordneten Ordner verschoben wird.
ms.openlocfilehash: 07f9c02ea194187a9fdfb1e27b19eb311392f51f
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353259"
---
# <a name="movedevent"></a><span data-ttu-id="ae1d8-103">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="ae1d8-103">MovedEvent</span></span>

<span data-ttu-id="ae1d8-104">Das **MovedEvent** -Element stellt ein Ereignis in der eines Elements oder Ordners von einem übergeordneten Ordner in einer anderen übergeordneten Ordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-104">The **MovedEvent** element represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span> 
  
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


<span data-ttu-id="ae1d8-105">**MovedCopiedEventType**</span><span class="sxs-lookup"><span data-stu-id="ae1d8-105">**MovedCopiedEventType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ae1d8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ae1d8-106">Attributes and elements</span></span>

<span data-ttu-id="ae1d8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae1d8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ae1d8-108">Attributes</span></span>

<span data-ttu-id="ae1d8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae1d8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ae1d8-110">Child elements</span></span>

|<span data-ttu-id="ae1d8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ae1d8-111">**Element**</span></span>|<span data-ttu-id="ae1d8-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ae1d8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae1d8-113">Watermark</span><span class="sxs-lookup"><span data-stu-id="ae1d8-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="ae1d8-114">Stellt eine Textmarke Ereignisse in der Tabelle der Postfach-Ereignisse dar.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-114">Represents an events bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="ae1d8-115">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="ae1d8-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="ae1d8-116">Stellt den Zeitstempel der ein Element-Ordner Postfach-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-116">Represents the timestamp of a move item/folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="ae1d8-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="ae1d8-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="ae1d8-118">Den Bezeichner des verschobenen Ordners darstellt.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-118">Represents the identifier of the moved folder.</span></span>  <br/> |
|[<span data-ttu-id="ae1d8-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="ae1d8-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="ae1d8-120">Stellt die das verschobene Element-ID an.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-120">Represents the identifier of the moved item.</span></span>  <br/> |
|[<span data-ttu-id="ae1d8-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="ae1d8-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="ae1d8-122">Stellt den Bezeichner des Ordners, die das verschobene Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-122">Represents the identifier of the folder that contains the moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="ae1d8-123">OldFolderId</span><span class="sxs-lookup"><span data-stu-id="ae1d8-123">OldFolderId</span></span>](oldfolderid.md) <br/> |<span data-ttu-id="ae1d8-124">Die Ordner-ID des ursprünglichen Ordners enthält, bevor sie verschoben oder kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-124">Contains the folder identifier of the original folder before it was moved or copied.</span></span>  <br/> |
|[<span data-ttu-id="ae1d8-125">OldItemId</span><span class="sxs-lookup"><span data-stu-id="ae1d8-125">OldItemId</span></span>](olditemid.md) <br/> |<span data-ttu-id="ae1d8-126">Enthält die eindeutige ID des ursprünglichen Elements an, bevor sie verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-126">Contains the unique identifier of the original item before it was moved.</span></span>  <br/> |
|[<span data-ttu-id="ae1d8-127">OldParentFolderId</span><span class="sxs-lookup"><span data-stu-id="ae1d8-127">OldParentFolderId</span></span>](oldparentfolderid.md) <br/> |<span data-ttu-id="ae1d8-128">Enthält den Bezeichner des übergeordneten Ordners ursprünglichen eines Elements oder Ordners, die verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-128">Contains the identifier of the original parent folder of an item or folder that was moved.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ae1d8-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ae1d8-129">Parent elements</span></span>

|<span data-ttu-id="ae1d8-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="ae1d8-130">**Element**</span></span>|<span data-ttu-id="ae1d8-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ae1d8-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae1d8-132">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="ae1d8-132">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ae1d8-133">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-133">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae1d8-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ae1d8-134">Remarks</span></span>

<span data-ttu-id="ae1d8-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae1d8-136">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ae1d8-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae1d8-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae1d8-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ae1d8-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ae1d8-138">Schema name</span></span>  <br/> |<span data-ttu-id="ae1d8-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ae1d8-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="ae1d8-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ae1d8-140">Validation file</span></span>  <br/> |<span data-ttu-id="ae1d8-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ae1d8-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ae1d8-142">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ae1d8-142">Can be empty</span></span>  <br/> |<span data-ttu-id="ae1d8-143">False</span><span class="sxs-lookup"><span data-stu-id="ae1d8-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae1d8-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae1d8-144">See also</span></span>

- [<span data-ttu-id="ae1d8-145">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="ae1d8-145">Subscribe operation</span></span>](subscribe-operation.md) 
- [<span data-ttu-id="ae1d8-146">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ae1d8-146">GetEvents operation</span></span>](getevents-operation.md) 
- [<span data-ttu-id="ae1d8-147">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="ae1d8-147">Unsubscribe operation</span></span>](unsubscribe-operation.md)

