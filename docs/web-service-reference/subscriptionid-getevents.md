---
title: Abonnement-Nr (GetEvents)
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
description: Das Subscription-ID-Element stellt den Bezeichner für ein Abonnement dar.
ms.openlocfilehash: e103386f466d65717878b4a6c811f3c3ad6e7c7d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465352"
---
# <a name="subscriptionid-getevents"></a><span data-ttu-id="6798c-103">Abonnement-Nr (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="6798c-103">SubscriptionId (GetEvents)</span></span>

<span data-ttu-id="6798c-104">Das **Subscription** -ID-Element stellt den Bezeichner für ein Abonnement dar.</span><span class="sxs-lookup"><span data-stu-id="6798c-104">The **SubscriptionId** element represents the identifier for a subscription.</span></span> 
  
```xml
<SubscriptionId/>
```

 <span data-ttu-id="6798c-105">**SubscriptionIdType**</span><span class="sxs-lookup"><span data-stu-id="6798c-105">**SubscriptionIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6798c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6798c-106">Attributes and elements</span></span>

<span data-ttu-id="6798c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6798c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6798c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6798c-108">Attributes</span></span>

<span data-ttu-id="6798c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6798c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6798c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6798c-110">Child elements</span></span>

<span data-ttu-id="6798c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="6798c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6798c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6798c-112">Parent elements</span></span>

|<span data-ttu-id="6798c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6798c-113">**Element**</span></span>|<span data-ttu-id="6798c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6798c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6798c-115">GetEvents</span><span class="sxs-lookup"><span data-stu-id="6798c-115">GetEvents</span></span>](getevents.md) <br/> |<span data-ttu-id="6798c-116">Stellt den Vorgang dar, der von Pull-Clients zum Anfordern von Benachrichtigungen vom Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6798c-116">Represents the operation used by pull clients to request notifications from the server.</span></span>  <br/> |
|[<span data-ttu-id="6798c-117">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="6798c-117">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="6798c-118">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="6798c-118">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
|[<span data-ttu-id="6798c-119">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6798c-119">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md) <br/> |<span data-ttu-id="6798c-120">Enthält den Status und das Ergebnis einer subscribe-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6798c-120">Contains the status and result of a Subscribe request.</span></span>  <br/> |
|[<span data-ttu-id="6798c-121">Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="6798c-121">Unsubscribe</span></span>](unsubscribe.md) <br/> |<span data-ttu-id="6798c-122">Enthält die Eigenschaften, mit denen das Abonnement eines Abonnements gekündigt wird.</span><span class="sxs-lookup"><span data-stu-id="6798c-122">Contains the properties used to unsubscribe from a subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6798c-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="6798c-123">Text value</span></span>

<span data-ttu-id="6798c-124">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6798c-124">A text value is required.</span></span> <span data-ttu-id="6798c-125">Der Textwert ist eine GUID.</span><span class="sxs-lookup"><span data-stu-id="6798c-125">The text value is a GUID.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6798c-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6798c-126">Remarks</span></span>

<span data-ttu-id="6798c-127">Die GUID, die die Abonnement-ID darstellt, wird vom Client Zugriffsserver generiert, wenn das Abonnement erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6798c-127">The GUID that represents the subscription identifier is generated by the Client Access server when the subscription is created.</span></span>
  
<span data-ttu-id="6798c-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="6798c-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6798c-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6798c-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6798c-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="6798c-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6798c-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6798c-131">Schema name</span></span>  <br/> |<span data-ttu-id="6798c-132">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="6798c-132">messages schema</span></span>  <br/> |
|<span data-ttu-id="6798c-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6798c-133">Validation file</span></span>  <br/> |<span data-ttu-id="6798c-134">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6798c-134">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6798c-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="6798c-135">Can be empty</span></span>  <br/> |<span data-ttu-id="6798c-136">False</span><span class="sxs-lookup"><span data-stu-id="6798c-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6798c-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6798c-137">See also</span></span>



[<span data-ttu-id="6798c-138">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="6798c-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="6798c-139">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6798c-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="6798c-140">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="6798c-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)

