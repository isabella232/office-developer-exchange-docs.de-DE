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
description: Das CreatedEvent-Element stellt ein Ereignis in der eines Elements oder Ordners erstellt wird.
ms.openlocfilehash: f52516090d0789b4dd9fc1ced824786ce000e885
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757748"
---
# <a name="createdevent"></a><span data-ttu-id="1342c-103">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="1342c-103">CreatedEvent</span></span>

<span data-ttu-id="1342c-104">Das **CreatedEvent** -Element stellt ein Ereignis in der eines Elements oder Ordners erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1342c-104">The **CreatedEvent** element represents an event in which an item or folder is created.</span></span> 
  
```xml
<CreatedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</CreatedEvent>
```

 <span data-ttu-id="1342c-105">**BaseObjectChangedEventType**</span><span class="sxs-lookup"><span data-stu-id="1342c-105">**BaseObjectChangedEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1342c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1342c-106">Attributes and elements</span></span>

<span data-ttu-id="1342c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1342c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1342c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1342c-108">Attributes</span></span>

<span data-ttu-id="1342c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1342c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1342c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1342c-110">Child elements</span></span>

|<span data-ttu-id="1342c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1342c-111">**Element**</span></span>|<span data-ttu-id="1342c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1342c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1342c-113">Wasserzeichen</span><span class="sxs-lookup"><span data-stu-id="1342c-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="1342c-114">Stellt eine Textmarke Ereignis in der Tabelle der Postfach-Ereignisse dar.</span><span class="sxs-lookup"><span data-stu-id="1342c-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="1342c-115">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="1342c-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="1342c-116">Stellt den Zeitstempel der erstellte Elements oder Ordners Postfach-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1342c-116">Represents the timestamp of a created item or folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="1342c-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="1342c-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="1342c-118">Den Bezeichner des erstellten Ordners darstellt.</span><span class="sxs-lookup"><span data-stu-id="1342c-118">Represents the identifier of the created folder.</span></span>  <br/> |
|[<span data-ttu-id="1342c-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="1342c-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="1342c-120">Den Bezeichner, der das erstellte Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="1342c-120">Represents the identifier of the created item.</span></span>  <br/> |
|[<span data-ttu-id="1342c-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="1342c-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="1342c-122">Stellt den Bezeichner des übergeordneten Ordners der erstellte Element oder des Ordners.</span><span class="sxs-lookup"><span data-stu-id="1342c-122">Represents the identifier of the parent folder of the created item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1342c-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1342c-123">Parent elements</span></span>

|<span data-ttu-id="1342c-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="1342c-124">**Element**</span></span>|<span data-ttu-id="1342c-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1342c-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1342c-126">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="1342c-126">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="1342c-127">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="1342c-127">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1342c-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1342c-128">Remarks</span></span>

<span data-ttu-id="1342c-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="1342c-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1342c-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1342c-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1342c-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="1342c-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1342c-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1342c-132">Schema name</span></span>  <br/> |<span data-ttu-id="1342c-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1342c-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="1342c-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1342c-134">Validation file</span></span>  <br/> |<span data-ttu-id="1342c-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1342c-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1342c-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="1342c-136">Can be empty</span></span>  <br/> |<span data-ttu-id="1342c-137">False</span><span class="sxs-lookup"><span data-stu-id="1342c-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1342c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1342c-138">See also</span></span>



[<span data-ttu-id="1342c-139">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="1342c-139">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="1342c-140">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1342c-140">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="1342c-141">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="1342c-141">Unsubscribe operation</span></span>](unsubscribe-operation.md)


[<span data-ttu-id="1342c-142">Mithilfe von Pullabonnements</span><span class="sxs-lookup"><span data-stu-id="1342c-142">Using Pull Subscriptions</span></span>](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[<span data-ttu-id="1342c-143">Ereignisbenachrichtigungen in Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="1342c-143">Event notifications in EWS</span></span>](http://msdn.microsoft.com/library/4fd4b351-d35c-4ccc-9ed9-878932ab9d50%28Office.15%29.aspx)

