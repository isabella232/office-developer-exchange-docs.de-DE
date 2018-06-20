---
title: GetStreamingEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetStreamingEvents
api_type:
- schema
ms.assetid: dbe83857-c4f8-4d98-813f-e03c289697a1
description: Das GetStreamingEvents-Element darstellt, den Vorgang, der von Clients zum Anfordern von streaming Benachrichtigungen vom Server verwendet wird.
ms.openlocfilehash: b07015541cf9c2fbbbc11ebc9f10421bdb9ee84f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829679"
---
# <a name="getstreamingevents"></a><span data-ttu-id="4d285-103">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="4d285-103">GetStreamingEvents</span></span>

<span data-ttu-id="4d285-104">Das **GetStreamingEvents** -Element darstellt, den Vorgang, der von Clients zum Anfordern von streaming Benachrichtigungen vom Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4d285-104">The **GetStreamingEvents** element represents the operation that is used by clients to request streaming notifications from the server.</span></span> 
  
[<span data-ttu-id="4d285-105">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="4d285-105">GetStreamingEvents</span></span>](getstreamingevents.md)
  
```XML
<GetStreamingEvents>
   <SubscriptionId/>
   <ConnectionTimeout/>
</GetStreamingEvents>
```

 <span data-ttu-id="4d285-106">**GetStreamingEventsType**</span><span class="sxs-lookup"><span data-stu-id="4d285-106">**GetStreamingEventsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4d285-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4d285-107">Attributes and elements</span></span>

<span data-ttu-id="4d285-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4d285-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4d285-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="4d285-109">Attributes</span></span>

<span data-ttu-id="4d285-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="4d285-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4d285-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4d285-111">Child elements</span></span>

|<span data-ttu-id="4d285-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="4d285-112">**Element**</span></span>|<span data-ttu-id="4d285-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4d285-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d285-114">SubscriptionId (GetStreamingEvents)</span><span class="sxs-lookup"><span data-stu-id="4d285-114">SubscriptionId (GetStreamingEvents)</span></span>](subscriptionid-getstreamingevents.md) <br/> |<span data-ttu-id="4d285-115">Stellt den Bezeichner für ein Abonnement, das für Ereignisse abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="4d285-115">Represents the identifier for a subscription that is queried for events.</span></span>  <br/> |
|[<span data-ttu-id="4d285-116">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="4d285-116">ConnectionTimeout</span></span>](connectiontimeout.md) <br/> |<span data-ttu-id="4d285-117">Stellt die Anzahl der Minuten, um eine Verbindung zu halten.</span><span class="sxs-lookup"><span data-stu-id="4d285-117">Represents the number of minutes to keep a connection open.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4d285-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4d285-118">Parent elements</span></span>

<span data-ttu-id="4d285-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="4d285-119">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="4d285-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="4d285-120">Text value</span></span>

<span data-ttu-id="4d285-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="4d285-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4d285-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4d285-122">Remarks</span></span>

<span data-ttu-id="4d285-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4d285-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4d285-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4d285-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4d285-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="4d285-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4d285-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4d285-126">Schema name</span></span>  <br/> |<span data-ttu-id="4d285-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4d285-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4d285-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4d285-128">Validation file</span></span>  <br/> |<span data-ttu-id="4d285-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4d285-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4d285-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="4d285-130">Can be empty</span></span>  <br/> |<span data-ttu-id="4d285-131">False</span><span class="sxs-lookup"><span data-stu-id="4d285-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4d285-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d285-132">See also</span></span>



[<span data-ttu-id="4d285-133">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="4d285-133">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="4d285-134">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4d285-134">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="4d285-135">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="4d285-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="4d285-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4d285-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

