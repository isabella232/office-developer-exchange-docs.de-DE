---
title: FreeBusyChangedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyChangedEvent
api_type:
- schema
ms.assetid: 63abbfc5-c29f-4110-a922-6b1247187f28
description: Das FreeBusyChangedEvent-Element stellt ein Ereignis in der Frei/Gebucht-Zeit eines Elements geändert hat.
ms.openlocfilehash: 7271d375526e7614d0150594c2b988666a59eb8d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758543"
---
# <a name="freebusychangedevent"></a><span data-ttu-id="6b1ac-103">FreeBusyChangedEvent</span><span class="sxs-lookup"><span data-stu-id="6b1ac-103">FreeBusyChangedEvent</span></span>

<span data-ttu-id="6b1ac-104">Das **FreeBusyChangedEvent** -Element stellt ein Ereignis in der Frei/Gebucht-Zeit eines Elements geändert hat.</span><span class="sxs-lookup"><span data-stu-id="6b1ac-104">The **FreeBusyChangedEvent** element represents an event in which an item's free/busy time has changed.</span></span> 
  
```xml
<CreatedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</CreatedEvent>
```

 <span data-ttu-id="6b1ac-105">**BaseObjectChangedEventType**</span><span class="sxs-lookup"><span data-stu-id="6b1ac-105">**BaseObjectChangedEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6b1ac-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6b1ac-106">Attributes and elements</span></span>

<span data-ttu-id="6b1ac-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6b1ac-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6b1ac-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6b1ac-108">Attributes</span></span>

<span data-ttu-id="6b1ac-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6b1ac-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6b1ac-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6b1ac-110">Child elements</span></span>

|<span data-ttu-id="6b1ac-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6b1ac-111">**Element**</span></span>|<span data-ttu-id="6b1ac-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6b1ac-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b1ac-113">Wasserzeichen</span><span class="sxs-lookup"><span data-stu-id="6b1ac-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="6b1ac-114">Stellt eine Textmarke Ereignis in der Tabelle der Postfach-Ereignisse dar.</span><span class="sxs-lookup"><span data-stu-id="6b1ac-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="6b1ac-115">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="6b1ac-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="6b1ac-116">Den Zeitstempel eines Ereignisses Postfach Frei/Gebucht-Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="6b1ac-116">Represents the timestamp of a free/busy item mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="6b1ac-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="6b1ac-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="6b1ac-118">Stellt den Bezeichner des Elements Frei/Gebucht-Informationen.</span><span class="sxs-lookup"><span data-stu-id="6b1ac-118">Represents the identifier of the free/busy item.</span></span>  <br/> |
|[<span data-ttu-id="6b1ac-119">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="6b1ac-119">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="6b1ac-120">Den Bezeichner des übergeordneten Ordners des Frei/Gebucht-Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="6b1ac-120">Represents the identifier of the parent folder of the free/busy item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6b1ac-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6b1ac-121">Parent elements</span></span>

|<span data-ttu-id="6b1ac-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="6b1ac-122">**Element**</span></span>|<span data-ttu-id="6b1ac-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6b1ac-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b1ac-124">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="6b1ac-124">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="6b1ac-125">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="6b1ac-125">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6b1ac-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="6b1ac-126">Text value</span></span>

<span data-ttu-id="6b1ac-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="6b1ac-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6b1ac-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6b1ac-128">Remarks</span></span>

<span data-ttu-id="6b1ac-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6b1ac-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b1ac-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6b1ac-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b1ac-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="6b1ac-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6b1ac-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6b1ac-132">Schema name</span></span>  <br/> |<span data-ttu-id="6b1ac-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6b1ac-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="6b1ac-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6b1ac-134">Validation file</span></span>  <br/> |<span data-ttu-id="6b1ac-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6b1ac-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6b1ac-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="6b1ac-136">Can be empty</span></span>  <br/> |<span data-ttu-id="6b1ac-137">False</span><span class="sxs-lookup"><span data-stu-id="6b1ac-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b1ac-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b1ac-138">See also</span></span>



[<span data-ttu-id="6b1ac-139">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="6b1ac-139">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="6b1ac-140">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6b1ac-140">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="6b1ac-141">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="6b1ac-141">Unsubscribe operation</span></span>](unsubscribe-operation.md)


[<span data-ttu-id="6b1ac-142">Mithilfe von Pullabonnements</span><span class="sxs-lookup"><span data-stu-id="6b1ac-142">Using Pull Subscriptions</span></span>](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[<span data-ttu-id="6b1ac-143">Ereignisbenachrichtigungen in Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="6b1ac-143">Event notifications in EWS</span></span>](http://msdn.microsoft.com/library/4fd4b351-d35c-4ccc-9ed9-878932ab9d50%28Office.15%29.aspx)

