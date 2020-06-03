---
title: GetEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetEvents
api_type:
- schema
ms.assetid: 22d4da6b-d8a8-484f-82c4-3e4b8f5431cd
description: Das GetEvents-Element stellt den Vorgang dar, der von Pull-Clients zum Anfordern von Benachrichtigungen vom Server verwendet wird.
ms.openlocfilehash: 004f782ccd32b3c5e501080bfc59419a6e7d9ce4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462500"
---
# <a name="getevents"></a><span data-ttu-id="ff6cd-103">GetEvents</span><span class="sxs-lookup"><span data-stu-id="ff6cd-103">GetEvents</span></span>

<span data-ttu-id="ff6cd-104">Das **GetEvents** -Element stellt den Vorgang dar, der von Pull-Clients zum Anfordern von Benachrichtigungen vom Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-104">The **GetEvents** element represents the operation used by pull clients to request notifications from the server.</span></span> 
  
[<span data-ttu-id="ff6cd-105">GetEvents</span><span class="sxs-lookup"><span data-stu-id="ff6cd-105">GetEvents</span></span>](getevents.md)
  
```xml
<GetEvents>
   <SubscriptionId/>
   <Watermark/>
</GetEvents>
```

 <span data-ttu-id="ff6cd-106">**Geteventstype**</span><span class="sxs-lookup"><span data-stu-id="ff6cd-106">**GetEventsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ff6cd-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ff6cd-107">Attributes and elements</span></span>

<span data-ttu-id="ff6cd-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff6cd-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="ff6cd-109">Attributes</span></span>

<span data-ttu-id="ff6cd-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ff6cd-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ff6cd-111">Child elements</span></span>

|<span data-ttu-id="ff6cd-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="ff6cd-112">**Element**</span></span>|<span data-ttu-id="ff6cd-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff6cd-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff6cd-114">Abonnement-Nr (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="ff6cd-114">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="ff6cd-115">Stellt den Bezeichner für ein Abonnement dar, das für Ereignisse abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-115">Represents the identifier for a subscription that is queried for events.</span></span>  <br/> |
|[<span data-ttu-id="ff6cd-116">Watermark</span><span class="sxs-lookup"><span data-stu-id="ff6cd-116">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="ff6cd-117">Stellt das letzte Wasserzeichen dar, das an den Client zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-117">Represents the last watermark returned to the client.</span></span> <span data-ttu-id="ff6cd-118">Wenn GetEvents nicht für dieses Abonnement aufgerufen wurde, verwendet der Client das Wasserzeichen, das von der Subscribe-Anforderung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-118">If GetEvents has not been called for this subscription, the client uses the watermark returned from the Subscribe request.</span></span> <span data-ttu-id="ff6cd-119">Andernfalls wird das Wasserzeichen aus dem letzten Ereignis in der letzten GetEvents-Antwort verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-119">Otherwise, the watermark from the last event in the last GetEvents response is used.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ff6cd-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ff6cd-120">Parent elements</span></span>

<span data-ttu-id="ff6cd-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ff6cd-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff6cd-122">Remarks</span></span>

<span data-ttu-id="ff6cd-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ff6cd-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ff6cd-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ff6cd-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff6cd-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="ff6cd-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ff6cd-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ff6cd-126">Schema name</span></span>  <br/> |<span data-ttu-id="ff6cd-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ff6cd-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ff6cd-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ff6cd-128">Validation file</span></span>  <br/> |<span data-ttu-id="ff6cd-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ff6cd-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ff6cd-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ff6cd-130">Can be empty</span></span>  <br/> |<span data-ttu-id="ff6cd-131">False</span><span class="sxs-lookup"><span data-stu-id="ff6cd-131">false</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff6cd-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff6cd-132">See also</span></span>



[<span data-ttu-id="ff6cd-133">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="ff6cd-133">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="ff6cd-134">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ff6cd-134">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="ff6cd-135">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="ff6cd-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)

