---
title: Benachrichtigungen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Notifications
api_type:
- schema
ms.assetid: 153cc420-d2fe-42f1-afb2-9a31ee09a750
description: Das Benachrichtigungen-Element enthält ein Array von Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.
ms.openlocfilehash: f576bf579c91b77dcde8646a6af7fdc47145aef7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830550"
---
# <a name="notifications"></a><span data-ttu-id="36cd5-103">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="36cd5-103">Notifications</span></span>

<span data-ttu-id="36cd5-104">Das **Benachrichtigungen** -Element enthält ein Array von Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="36cd5-104">The **Notifications** element contains an array of information about the subscription and the events that have occurred since the last notification.</span></span> 
  
```xml
<Notifications>
   <Notification/>
</Notifications>
```

 <span data-ttu-id="36cd5-105">**NonEmptyArrayOfNotificationsType**</span><span class="sxs-lookup"><span data-stu-id="36cd5-105">**NonEmptyArrayOfNotificationsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="36cd5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="36cd5-106">Attributes and elements</span></span>

<span data-ttu-id="36cd5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="36cd5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="36cd5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="36cd5-108">Attributes</span></span>

<span data-ttu-id="36cd5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="36cd5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="36cd5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="36cd5-110">Child elements</span></span>

|<span data-ttu-id="36cd5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="36cd5-111">**Element**</span></span>|<span data-ttu-id="36cd5-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="36cd5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36cd5-113">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="36cd5-113">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="36cd5-114">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="36cd5-114">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="36cd5-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="36cd5-115">Parent elements</span></span>

|<span data-ttu-id="36cd5-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="36cd5-116">**Element**</span></span>|<span data-ttu-id="36cd5-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="36cd5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36cd5-118">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="36cd5-118">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md) <br/> |<span data-ttu-id="36cd5-119">Enthält den Status und das Ergebnis einer einzelnen Anforderung [GetStreamingEvents Vorgang](getstreamingevents-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="36cd5-119">Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="36cd5-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="36cd5-120">Text value</span></span>

<span data-ttu-id="36cd5-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="36cd5-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="36cd5-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="36cd5-122">Remarks</span></span>

<span data-ttu-id="36cd5-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="36cd5-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="36cd5-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="36cd5-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36cd5-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="36cd5-125">Namespace</span></span>  <br/> |<span data-ttu-id="36cd5-126">http://schemas.microsoft.com/exchange/services/2006/messages und http://schemas.microsoft.com/exchange/services/2006/types</span><span class="sxs-lookup"><span data-stu-id="36cd5-126">http://schemas.microsoft.com/exchange/services/2006/messages and http://schemas.microsoft.com/exchange/services/2006/types</span></span>  <br/> |
|<span data-ttu-id="36cd5-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="36cd5-127">Schema Name</span></span>  <br/> |<span data-ttu-id="36cd5-128">Nachrichten-schema Typen-schema</span><span class="sxs-lookup"><span data-stu-id="36cd5-128">Messages schema; Types schema</span></span>  <br/> |
|<span data-ttu-id="36cd5-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="36cd5-129">Validation File</span></span>  <br/> |<span data-ttu-id="36cd5-130">Messages.xsd; Types.xsd</span><span class="sxs-lookup"><span data-stu-id="36cd5-130">Messages.xsd; Types.xsd</span></span>  <br/> |
|<span data-ttu-id="36cd5-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="36cd5-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="36cd5-132">False</span><span class="sxs-lookup"><span data-stu-id="36cd5-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36cd5-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36cd5-133">See also</span></span>



[<span data-ttu-id="36cd5-134">GetFolder Operation</span><span class="sxs-lookup"><span data-stu-id="36cd5-134">GetFolder operation</span></span>](getfolder-operation.md)
  
[<span data-ttu-id="36cd5-135">DeleteFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="36cd5-135">DeleteFolder operation</span></span>](deletefolder-operation.md)
  
[<span data-ttu-id="36cd5-136">MoveFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="36cd5-136">MoveFolder operation</span></span>](movefolder-operation.md)
  
[<span data-ttu-id="36cd5-137">CopyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="36cd5-137">CopyFolder operation</span></span>](copyfolder-operation.md)
  
[<span data-ttu-id="36cd5-138">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="36cd5-138">Subscribe operation</span></span>](subscribe-operation.md)

