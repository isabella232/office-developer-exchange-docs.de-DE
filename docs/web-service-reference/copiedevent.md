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
description: Das CopiedEvent-Element stellt ein Ereignis in der eines Elements oder Ordners kopiert wird.
ms.openlocfilehash: 7ebfbb744a80e3a2d14ee9e0e1b952d2269dbf94
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353168"
---
# <a name="copiedevent"></a><span data-ttu-id="5f9f8-103">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="5f9f8-103">CopiedEvent</span></span>

<span data-ttu-id="5f9f8-104">Das **CopiedEvent** -Element stellt ein Ereignis in der eines Elements oder Ordners kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-104">The **CopiedEvent** element represents an event in which an item or folder is copied.</span></span> 
  
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

<span data-ttu-id="5f9f8-105">**MovedCopiedEventType**</span><span class="sxs-lookup"><span data-stu-id="5f9f8-105">**MovedCopiedEventType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5f9f8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5f9f8-106">Attributes and elements</span></span>

<span data-ttu-id="5f9f8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f9f8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5f9f8-108">Attributes</span></span>

<span data-ttu-id="5f9f8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5f9f8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f9f8-110">Child elements</span></span>

|<span data-ttu-id="5f9f8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5f9f8-111">**Element**</span></span>|<span data-ttu-id="5f9f8-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5f9f8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f9f8-113">Watermark</span><span class="sxs-lookup"><span data-stu-id="5f9f8-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="5f9f8-114">Stellt eine Textmarke Ereignisse in der Tabelle der Postfach-Ereignisse dar.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-114">Represents an events bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="5f9f8-115">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="5f9f8-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="5f9f8-116">Steht für den Zeitstempel eines Ereignisses Postfach Element-Ordner kopieren.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-116">Represents the timestamp of a copy item/folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="5f9f8-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="5f9f8-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="5f9f8-118">Den Bezeichner des Ordners darstellt.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-118">Represents the identifier of the folder.</span></span>  <br/> |
|[<span data-ttu-id="5f9f8-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="5f9f8-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="5f9f8-120">Den Bezeichner des Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-120">Represents the identifier of the item.</span></span>  <br/> |
|[<span data-ttu-id="5f9f8-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="5f9f8-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="5f9f8-122">Stellt den Bezeichner des Ordners, der die Kopie enthält.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-122">Represents the identifier of the folder that contains the copy.</span></span>  <br/> |
|[<span data-ttu-id="5f9f8-123">OldFolderId</span><span class="sxs-lookup"><span data-stu-id="5f9f8-123">OldFolderId</span></span>](oldfolderid.md) <br/> |<span data-ttu-id="5f9f8-124">Die Ordner-ID des ursprünglichen Ordners darstellt, bevor sie kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-124">Represents the folder identifier of the original folder before it was copied.</span></span>  <br/> |
|[<span data-ttu-id="5f9f8-125">OldItemId</span><span class="sxs-lookup"><span data-stu-id="5f9f8-125">OldItemId</span></span>](olditemid.md) <br/> |<span data-ttu-id="5f9f8-126">Enthält die eindeutige ID des ursprünglichen Elements an, bevor sie kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-126">Contains the unique identifier of the original item before it was copied.</span></span>  <br/> |
|[<span data-ttu-id="5f9f8-127">OldParentFolderId</span><span class="sxs-lookup"><span data-stu-id="5f9f8-127">OldParentFolderId</span></span>](oldparentfolderid.md) <br/> |<span data-ttu-id="5f9f8-128">Enthält den Bezeichner des übergeordneten Ordners ursprünglichen eines Elements oder Ordners, der kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-128">Contains the identifier of the original parent folder of an item or folder that was copied.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5f9f8-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f9f8-129">Parent elements</span></span>

|<span data-ttu-id="5f9f8-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="5f9f8-130">**Element**</span></span>|<span data-ttu-id="5f9f8-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5f9f8-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f9f8-132">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="5f9f8-132">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5f9f8-133">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-133">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f9f8-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5f9f8-134">Remarks</span></span>

<span data-ttu-id="5f9f8-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="5f9f8-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5f9f8-136">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5f9f8-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f9f8-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f9f8-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5f9f8-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5f9f8-138">Schema name</span></span>  <br/> |<span data-ttu-id="5f9f8-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5f9f8-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="5f9f8-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5f9f8-140">Validation file</span></span>  <br/> |<span data-ttu-id="5f9f8-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5f9f8-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5f9f8-142">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="5f9f8-142">Can be empty</span></span>  <br/> |<span data-ttu-id="5f9f8-143">False</span><span class="sxs-lookup"><span data-stu-id="5f9f8-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5f9f8-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f9f8-144">See also</span></span>

- [<span data-ttu-id="5f9f8-145">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="5f9f8-145">Subscribe operation</span></span>](subscribe-operation.md) 
- [<span data-ttu-id="5f9f8-146">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5f9f8-146">GetEvents operation</span></span>](getevents-operation.md) 
- [<span data-ttu-id="5f9f8-147">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="5f9f8-147">Unsubscribe operation</span></span>](unsubscribe-operation.md)
- [<span data-ttu-id="5f9f8-148">Mithilfe von Pullabonnements</span><span class="sxs-lookup"><span data-stu-id="5f9f8-148">Using Pull Subscriptions</span></span>](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx) 
- [<span data-ttu-id="5f9f8-149">Beispielanwendung für Pushbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="5f9f8-149">Push Notification Sample Application</span></span>](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

