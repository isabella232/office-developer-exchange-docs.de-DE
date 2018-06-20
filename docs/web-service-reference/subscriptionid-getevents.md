---
title: SubscriptionId (GetEvents)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubscriptionId
api_type:
- schema
ms.assetid: 77c0abab-69e8-428e-8c20-22258e4ef71b
description: Das Element SubscriptionId stellt den Bezeichner für ein Abonnement.
ms.openlocfilehash: 8867b7da7c75cfd9d41f708c0481627d5186cc14
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831622"
---
# <a name="subscriptionid-getevents"></a><span data-ttu-id="bb4a9-103">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="bb4a9-103">SubscriptionId (GetEvents)</span></span>

<span data-ttu-id="bb4a9-104">Das Element **SubscriptionId** stellt den Bezeichner für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bb4a9-104">The **SubscriptionId** element represents the identifier for a subscription.</span></span> 
  
```xml
<SubscriptionId/>
```

 <span data-ttu-id="bb4a9-105">**SubscriptionIdType**</span><span class="sxs-lookup"><span data-stu-id="bb4a9-105">**SubscriptionIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bb4a9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bb4a9-106">Attributes and elements</span></span>

<span data-ttu-id="bb4a9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bb4a9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb4a9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="bb4a9-108">Attributes</span></span>

<span data-ttu-id="bb4a9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="bb4a9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bb4a9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bb4a9-110">Child elements</span></span>

<span data-ttu-id="bb4a9-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="bb4a9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bb4a9-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bb4a9-112">Parent elements</span></span>

|<span data-ttu-id="bb4a9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bb4a9-113">**Element**</span></span>|<span data-ttu-id="bb4a9-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bb4a9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb4a9-115">GetEvents</span><span class="sxs-lookup"><span data-stu-id="bb4a9-115">GetEvents</span></span>](getevents.md) <br/> |<span data-ttu-id="bb4a9-116">Stellt die Operation auf Anforderung-Benachrichtigungen vom Server von Pull-Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb4a9-116">Represents the operation used by pull clients to request notifications from the server.</span></span>  <br/> |
|[<span data-ttu-id="bb4a9-117">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="bb4a9-117">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="bb4a9-118">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="bb4a9-118">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
|[<span data-ttu-id="bb4a9-119">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bb4a9-119">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md) <br/> |<span data-ttu-id="bb4a9-120">Enthält den Status und das Ergebnis einer Subscribe-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="bb4a9-120">Contains the status and result of a Subscribe request.</span></span>  <br/> |
|[<span data-ttu-id="bb4a9-121">Melden Sie sich ab</span><span class="sxs-lookup"><span data-stu-id="bb4a9-121">Unsubscribe</span></span>](unsubscribe.md) <br/> |<span data-ttu-id="bb4a9-122">Enthält die Eigenschaften verwendet, um ein Abonnement zu kündigen.</span><span class="sxs-lookup"><span data-stu-id="bb4a9-122">Contains the properties used to unsubscribe from a subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bb4a9-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="bb4a9-123">Text value</span></span>

<span data-ttu-id="bb4a9-124">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bb4a9-124">A text value is required.</span></span> <span data-ttu-id="bb4a9-125">Der Textwert ist eine GUID.</span><span class="sxs-lookup"><span data-stu-id="bb4a9-125">The text value is a GUID.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bb4a9-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bb4a9-126">Remarks</span></span>

<span data-ttu-id="bb4a9-127">Die GUID, die die Abonnement-ID darstellt wird vom Client Access Server generiert, wenn das Abonnement erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bb4a9-127">The GUID that represents the subscription identifier is generated by the Client Access server when the subscription is created.</span></span>
  
<span data-ttu-id="bb4a9-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="bb4a9-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bb4a9-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bb4a9-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb4a9-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="bb4a9-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bb4a9-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bb4a9-131">Schema name</span></span>  <br/> |<span data-ttu-id="bb4a9-132">Nachrichten-schema</span><span class="sxs-lookup"><span data-stu-id="bb4a9-132">messages schema</span></span>  <br/> |
|<span data-ttu-id="bb4a9-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bb4a9-133">Validation file</span></span>  <br/> |<span data-ttu-id="bb4a9-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bb4a9-134">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bb4a9-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="bb4a9-135">Can be empty</span></span>  <br/> |<span data-ttu-id="bb4a9-136">False</span><span class="sxs-lookup"><span data-stu-id="bb4a9-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb4a9-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb4a9-137">See also</span></span>



[<span data-ttu-id="bb4a9-138">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="bb4a9-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="bb4a9-139">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bb4a9-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="bb4a9-140">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="bb4a9-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)

