---
title: CreatedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreatedEvent
api_type:
- schema
ms.assetid: f0e53a53-c352-42a5-8280-cd808b0e961b
description: Das CreatedEvent-Element stellt ein Ereignis dar, in dem ein Element oder ein Ordner erstellt wird.
ms.openlocfilehash: 546dde782b3b20cd76acb625067b5f2d8f568854
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44445321"
---
# <a name="createdevent"></a><span data-ttu-id="a6c3b-103">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="a6c3b-103">CreatedEvent</span></span>

<span data-ttu-id="a6c3b-104">Das **CreatedEvent** -Element stellt ein Ereignis dar, in dem ein Element oder ein Ordner erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a6c3b-104">The **CreatedEvent** element represents an event in which an item or folder is created.</span></span> 
  
```xml
<CreatedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</CreatedEvent>
```

```xml
<CreatedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
</CreatedEvent>
```

<span data-ttu-id="a6c3b-105">**BaseObjectChangedEventType**</span><span class="sxs-lookup"><span data-stu-id="a6c3b-105">**BaseObjectChangedEventType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a6c3b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a6c3b-106">Attributes and elements</span></span>

<span data-ttu-id="a6c3b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a6c3b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a6c3b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a6c3b-108">Attributes</span></span>

<span data-ttu-id="a6c3b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a6c3b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a6c3b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a6c3b-110">Child elements</span></span>

|<span data-ttu-id="a6c3b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a6c3b-111">**Element**</span></span>|<span data-ttu-id="a6c3b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a6c3b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6c3b-113">Watermark</span><span class="sxs-lookup"><span data-stu-id="a6c3b-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="a6c3b-114">Stellt eine Ereignis Textmarke in der Tabelle Post Fach Ereignisse dar.</span><span class="sxs-lookup"><span data-stu-id="a6c3b-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="a6c3b-115">Timestamp</span><span class="sxs-lookup"><span data-stu-id="a6c3b-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="a6c3b-116">Stellt den Zeitstempel eines erstellten Element-oder Ordner Postfach-Ereignisses dar.</span><span class="sxs-lookup"><span data-stu-id="a6c3b-116">Represents the timestamp of a created item or folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="a6c3b-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="a6c3b-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="a6c3b-118">Stellt den Bezeichner des erstellten Ordners dar.</span><span class="sxs-lookup"><span data-stu-id="a6c3b-118">Represents the identifier of the created folder.</span></span>  <br/> |
|[<span data-ttu-id="a6c3b-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="a6c3b-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="a6c3b-120">Stellt den Bezeichner des erstellten Elements dar.</span><span class="sxs-lookup"><span data-stu-id="a6c3b-120">Represents the identifier of the created item.</span></span>  <br/> |
|[<span data-ttu-id="a6c3b-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="a6c3b-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="a6c3b-122">Stellt den Bezeichner des übergeordneten Ordners des erstellten Elements oder Ordners dar.</span><span class="sxs-lookup"><span data-stu-id="a6c3b-122">Represents the identifier of the parent folder of the created item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a6c3b-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a6c3b-123">Parent elements</span></span>

|<span data-ttu-id="a6c3b-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="a6c3b-124">**Element**</span></span>|<span data-ttu-id="a6c3b-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a6c3b-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6c3b-126">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="a6c3b-126">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a6c3b-127">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="a6c3b-127">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6c3b-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6c3b-128">Remarks</span></span>

<span data-ttu-id="a6c3b-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a6c3b-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a6c3b-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a6c3b-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6c3b-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="a6c3b-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a6c3b-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a6c3b-132">Schema name</span></span>  <br/> |<span data-ttu-id="a6c3b-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a6c3b-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="a6c3b-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a6c3b-134">Validation file</span></span>  <br/> |<span data-ttu-id="a6c3b-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a6c3b-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a6c3b-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a6c3b-136">Can be empty</span></span>  <br/> |<span data-ttu-id="a6c3b-137">False</span><span class="sxs-lookup"><span data-stu-id="a6c3b-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6c3b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6c3b-138">See also</span></span>

- [<span data-ttu-id="a6c3b-139">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="a6c3b-139">Subscribe operation</span></span>](subscribe-operation.md)  
- [<span data-ttu-id="a6c3b-140">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a6c3b-140">GetEvents operation</span></span>](getevents-operation.md)  
- [<span data-ttu-id="a6c3b-141">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="a6c3b-141">Unsubscribe operation</span></span>](unsubscribe-operation.md)
- [<span data-ttu-id="a6c3b-142">Verwenden von Pullabonnements</span><span class="sxs-lookup"><span data-stu-id="a6c3b-142">Using Pull Subscriptions</span></span>](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx) 
- [<span data-ttu-id="a6c3b-143">Ereignisbenachrichtigungen in EWS</span><span class="sxs-lookup"><span data-stu-id="a6c3b-143">Event notifications in EWS</span></span>](https://msdn.microsoft.com/library/4fd4b351-d35c-4ccc-9ed9-878932ab9d50%28Office.15%29.aspx)

