---
title: DeletedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeletedEvent
api_type:
- schema
ms.assetid: c4565eb4-b537-466c-b1ff-11602533812b
description: Das DeletedEvent-Element stellt ein Ereignis in der eines Elements oder Ordners gelöscht wird.
ms.openlocfilehash: f06ca0727916f415c648e876f88bf7eacef5a5ff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757911"
---
# <a name="deletedevent"></a><span data-ttu-id="6ed8a-103">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="6ed8a-103">DeletedEvent</span></span>

<span data-ttu-id="6ed8a-104">Das **DeletedEvent** -Element stellt ein Ereignis in der eines Elements oder Ordners gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="6ed8a-104">The **DeletedEvent** element represents an event in which an item or folder is deleted.</span></span> 
  
```xml
<DeletedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</DeletedEvent>
```

<span data-ttu-id="6ed8a-105">**BaseObjectChangedEventType**</span><span class="sxs-lookup"><span data-stu-id="6ed8a-105">**BaseObjectChangedEventType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6ed8a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6ed8a-106">Attributes and elements</span></span>

<span data-ttu-id="6ed8a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6ed8a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6ed8a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6ed8a-108">Attributes</span></span>

<span data-ttu-id="6ed8a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6ed8a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6ed8a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6ed8a-110">Child elements</span></span>

|<span data-ttu-id="6ed8a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6ed8a-111">**Element**</span></span>|<span data-ttu-id="6ed8a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ed8a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ed8a-113">Wasserzeichen</span><span class="sxs-lookup"><span data-stu-id="6ed8a-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="6ed8a-114">Stellt eine Textmarke Ereignis in der Tabelle der Postfach-Ereignisse dar.</span><span class="sxs-lookup"><span data-stu-id="6ed8a-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="6ed8a-115">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="6ed8a-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="6ed8a-116">Den Zeitstempel des ein gelöschtes Postfach-Ereignis Elements oder Ordners darstellt.</span><span class="sxs-lookup"><span data-stu-id="6ed8a-116">Represents the timestamp of a deleted item or folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="6ed8a-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="6ed8a-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="6ed8a-118">Den Bezeichner des gelöschten Ordners darstellt.</span><span class="sxs-lookup"><span data-stu-id="6ed8a-118">Represents the identifier of the deleted folder.</span></span>  <br/> |
|[<span data-ttu-id="6ed8a-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="6ed8a-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="6ed8a-120">Den Bezeichner des gelöschten Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="6ed8a-120">Represents the identifier of the deleted item.</span></span>  <br/> |
|[<span data-ttu-id="6ed8a-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="6ed8a-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="6ed8a-122">Stellt den Bezeichner des übergeordneten Ordners des gelöschten Elements oder Ordners vor dem Löschen.</span><span class="sxs-lookup"><span data-stu-id="6ed8a-122">Represents the identifier of the parent folder of the deleted item or folder before deletion.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6ed8a-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6ed8a-123">Parent elements</span></span>

|<span data-ttu-id="6ed8a-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="6ed8a-124">**Element**</span></span>|<span data-ttu-id="6ed8a-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ed8a-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ed8a-126">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="6ed8a-126">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="6ed8a-127">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="6ed8a-127">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ed8a-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6ed8a-128">Remarks</span></span>

<span data-ttu-id="6ed8a-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="6ed8a-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6ed8a-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6ed8a-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ed8a-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ed8a-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6ed8a-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6ed8a-132">Schema name</span></span>  <br/> |<span data-ttu-id="6ed8a-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6ed8a-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="6ed8a-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6ed8a-134">Validation file</span></span>  <br/> |<span data-ttu-id="6ed8a-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6ed8a-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6ed8a-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="6ed8a-136">Can be empty</span></span>  <br/> |<span data-ttu-id="6ed8a-137">False</span><span class="sxs-lookup"><span data-stu-id="6ed8a-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ed8a-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ed8a-138">See also</span></span>

- [<span data-ttu-id="6ed8a-139">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="6ed8a-139">Subscribe operation</span></span>](subscribe-operation.md)  
- [<span data-ttu-id="6ed8a-140">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6ed8a-140">GetEvents operation</span></span>](getevents-operation.md)  
- [<span data-ttu-id="6ed8a-141">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="6ed8a-141">Unsubscribe operation</span></span>](unsubscribe-operation.md)

