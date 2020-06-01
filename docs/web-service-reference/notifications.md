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
description: Das Notifications-Element enthält ein Array von Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.
ms.openlocfilehash: 88fc56ba6e672e3dea7a1d31f7cc1fda018b9a15
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462619"
---
# <a name="notifications"></a><span data-ttu-id="24d4e-103">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="24d4e-103">Notifications</span></span>

<span data-ttu-id="24d4e-104">Das **Notifications** -Element enthält ein Array von Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="24d4e-104">The **Notifications** element contains an array of information about the subscription and the events that have occurred since the last notification.</span></span> 
  
```xml
<Notifications>
   <Notification/>
</Notifications>
```

 <span data-ttu-id="24d4e-105">**NonEmptyArrayOfNotificationsType**</span><span class="sxs-lookup"><span data-stu-id="24d4e-105">**NonEmptyArrayOfNotificationsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="24d4e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="24d4e-106">Attributes and elements</span></span>

<span data-ttu-id="24d4e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="24d4e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="24d4e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="24d4e-108">Attributes</span></span>

<span data-ttu-id="24d4e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="24d4e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="24d4e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="24d4e-110">Child elements</span></span>

|<span data-ttu-id="24d4e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="24d4e-111">**Element**</span></span>|<span data-ttu-id="24d4e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24d4e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="24d4e-113">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="24d4e-113">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="24d4e-114">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="24d4e-114">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="24d4e-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="24d4e-115">Parent elements</span></span>

|<span data-ttu-id="24d4e-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="24d4e-116">**Element**</span></span>|<span data-ttu-id="24d4e-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24d4e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="24d4e-118">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="24d4e-118">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md) <br/> |<span data-ttu-id="24d4e-119">Enthält den Status und das Ergebnis einer einzelnen [GetStreamingEvents-Vorgangs](getstreamingevents-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="24d4e-119">Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="24d4e-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="24d4e-120">Text value</span></span>

<span data-ttu-id="24d4e-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="24d4e-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="24d4e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24d4e-122">Remarks</span></span>

<span data-ttu-id="24d4e-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="24d4e-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="24d4e-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="24d4e-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24d4e-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="24d4e-125">Namespace</span></span>  <br/> |<span data-ttu-id="24d4e-126">https://schemas.microsoft.com/exchange/services/2006/messages und https://schemas.microsoft.com/exchange/services/2006/types</span><span class="sxs-lookup"><span data-stu-id="24d4e-126">https://schemas.microsoft.com/exchange/services/2006/messages and https://schemas.microsoft.com/exchange/services/2006/types</span></span>  <br/> |
|<span data-ttu-id="24d4e-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="24d4e-127">Schema Name</span></span>  <br/> |<span data-ttu-id="24d4e-128">Nachrichtenschema; Typenschema</span><span class="sxs-lookup"><span data-stu-id="24d4e-128">Messages schema; Types schema</span></span>  <br/> |
|<span data-ttu-id="24d4e-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="24d4e-129">Validation File</span></span>  <br/> |<span data-ttu-id="24d4e-130">Messages. xsd; Types. xsd</span><span class="sxs-lookup"><span data-stu-id="24d4e-130">Messages.xsd; Types.xsd</span></span>  <br/> |
|<span data-ttu-id="24d4e-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="24d4e-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="24d4e-132">False</span><span class="sxs-lookup"><span data-stu-id="24d4e-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24d4e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24d4e-133">See also</span></span>



[<span data-ttu-id="24d4e-134">GetFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="24d4e-134">GetFolder operation</span></span>](getfolder-operation.md)
  
[<span data-ttu-id="24d4e-135">DeleteFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="24d4e-135">DeleteFolder operation</span></span>](deletefolder-operation.md)
  
[<span data-ttu-id="24d4e-136">MoveFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="24d4e-136">MoveFolder operation</span></span>](movefolder-operation.md)
  
[<span data-ttu-id="24d4e-137">CopyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="24d4e-137">CopyFolder operation</span></span>](copyfolder-operation.md)
  
[<span data-ttu-id="24d4e-138">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="24d4e-138">Subscribe operation</span></span>](subscribe-operation.md)

