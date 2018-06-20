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
description: Das GetEvents-Element darstellt, den Vorgang von Pull-Clients auf Anforderung-Benachrichtigungen vom Server verwendet.
ms.openlocfilehash: e7b24207bff579a2f5230676d6520452f96fe0ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758646"
---
# <a name="getevents"></a><span data-ttu-id="b331b-103">GetEvents</span><span class="sxs-lookup"><span data-stu-id="b331b-103">GetEvents</span></span>

<span data-ttu-id="b331b-104">Das **GetEvents** -Element darstellt, den Vorgang von Pull-Clients auf Anforderung-Benachrichtigungen vom Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="b331b-104">The **GetEvents** element represents the operation used by pull clients to request notifications from the server.</span></span> 
  
[<span data-ttu-id="b331b-105">GetEvents</span><span class="sxs-lookup"><span data-stu-id="b331b-105">GetEvents</span></span>](getevents.md)
  
```xml
<GetEvents>
   <SubscriptionId/>
   <Watermark/>
</GetEvents>
```

 <span data-ttu-id="b331b-106">**GetEventsType**</span><span class="sxs-lookup"><span data-stu-id="b331b-106">**GetEventsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b331b-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b331b-107">Attributes and elements</span></span>

<span data-ttu-id="b331b-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b331b-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b331b-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="b331b-109">Attributes</span></span>

<span data-ttu-id="b331b-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="b331b-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b331b-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b331b-111">Child elements</span></span>

|<span data-ttu-id="b331b-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="b331b-112">**Element**</span></span>|<span data-ttu-id="b331b-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b331b-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b331b-114">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="b331b-114">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="b331b-115">Stellt den Bezeichner für ein Abonnement, das für Ereignisse abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="b331b-115">Represents the identifier for a subscription that is queried for events.</span></span>  <br/> |
|[<span data-ttu-id="b331b-116">Wasserzeichen</span><span class="sxs-lookup"><span data-stu-id="b331b-116">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="b331b-117">Stellt das letzte Wasserzeichen an den Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b331b-117">Represents the last watermark returned to the client.</span></span> <span data-ttu-id="b331b-118">Wenn GetEvents für dieses Abonnement nicht aufgerufen wurde, verwendet der Client das Wasserzeichen aus der Subscribe-Anforderung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b331b-118">If GetEvents has not been called for this subscription, the client uses the watermark returned from the Subscribe request.</span></span> <span data-ttu-id="b331b-119">Andernfalls wird das Wasserzeichen aus dem letzten Ereignis in der letzten GetEvents Antwort verwendet.</span><span class="sxs-lookup"><span data-stu-id="b331b-119">Otherwise, the watermark from the last event in the last GetEvents response is used.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b331b-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b331b-120">Parent elements</span></span>

<span data-ttu-id="b331b-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="b331b-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b331b-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b331b-122">Remarks</span></span>

<span data-ttu-id="b331b-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="b331b-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b331b-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b331b-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b331b-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="b331b-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b331b-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b331b-126">Schema name</span></span>  <br/> |<span data-ttu-id="b331b-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b331b-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b331b-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b331b-128">Validation file</span></span>  <br/> |<span data-ttu-id="b331b-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b331b-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b331b-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b331b-130">Can be empty</span></span>  <br/> |<span data-ttu-id="b331b-131">false</span><span class="sxs-lookup"><span data-stu-id="b331b-131">false</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b331b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b331b-132">See also</span></span>



[<span data-ttu-id="b331b-133">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="b331b-133">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="b331b-134">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b331b-134">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="b331b-135">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="b331b-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)

