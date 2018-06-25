---
title: NewMailEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NewMailEvent
api_type:
- schema
ms.assetid: 45057945-a3ec-4dac-92db-f0dc5fcfc34d
description: Das NewMailEvent-Element stellt ein Ereignis, das durch eine neue e-Mail-Element in einem Postfach ausgelöst wird.
ms.openlocfilehash: 8df3e4a218a8eaa9d129854e4816a3a43beddafa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830527"
---
# <a name="newmailevent"></a><span data-ttu-id="80b07-103">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="80b07-103">NewMailEvent</span></span>

<span data-ttu-id="80b07-104">Das **NewMailEvent** -Element stellt ein Ereignis, das durch eine neue e-Mail-Element in einem Postfach ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="80b07-104">The **NewMailEvent** element represents an event that is triggered by a new mail item in a mailbox.</span></span> 
  
```xml
<NewMailEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</NewMailEvent>
```

 <span data-ttu-id="80b07-105">**BaseObjectChangedEventType**</span><span class="sxs-lookup"><span data-stu-id="80b07-105">**BaseObjectChangedEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="80b07-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="80b07-106">Attributes and elements</span></span>

<span data-ttu-id="80b07-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="80b07-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80b07-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="80b07-108">Attributes</span></span>

<span data-ttu-id="80b07-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="80b07-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="80b07-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="80b07-110">Child elements</span></span>

|<span data-ttu-id="80b07-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="80b07-111">**Element**</span></span>|<span data-ttu-id="80b07-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="80b07-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="80b07-113">Wasserzeichen</span><span class="sxs-lookup"><span data-stu-id="80b07-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="80b07-114">Stellt eine Textmarke Ereignis in der Tabelle der Postfach-Ereignisse dar.</span><span class="sxs-lookup"><span data-stu-id="80b07-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="80b07-115">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="80b07-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="80b07-116">Stellt den Zeitstempel der das Eintreffen einer neuen e-Mail-Elements in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="80b07-116">Represents the timestamp of the arrival of a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="80b07-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="80b07-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="80b07-118">Den Bezeichner eines neuen e-Mail-Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="80b07-118">Represents the identifier of a new mail item.</span></span>  <br/> |
|[<span data-ttu-id="80b07-119">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="80b07-119">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="80b07-120">Den Bezeichner des übergeordneten Ordners des neuen e-Mail-Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="80b07-120">Represents the identifier of the parent folder of the new mail item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="80b07-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="80b07-121">Parent elements</span></span>

|<span data-ttu-id="80b07-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="80b07-122">**Element**</span></span>|<span data-ttu-id="80b07-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="80b07-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="80b07-124">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="80b07-124">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="80b07-125">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="80b07-125">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80b07-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="80b07-126">Remarks</span></span>

<span data-ttu-id="80b07-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="80b07-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="80b07-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="80b07-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80b07-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="80b07-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="80b07-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="80b07-130">Schema name</span></span>  <br/> |<span data-ttu-id="80b07-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="80b07-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="80b07-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="80b07-132">Validation file</span></span>  <br/> |<span data-ttu-id="80b07-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="80b07-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="80b07-134">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="80b07-134">Can be empty</span></span>  <br/> |<span data-ttu-id="80b07-135">False</span><span class="sxs-lookup"><span data-stu-id="80b07-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80b07-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80b07-136">See also</span></span>



[<span data-ttu-id="80b07-137">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="80b07-137">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="80b07-138">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="80b07-138">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="80b07-139">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="80b07-139">Unsubscribe operation</span></span>](unsubscribe-operation.md)

