---
title: Kündigen eines Abonnements
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Unsubscribe
api_type:
- schema
ms.assetid: 5584db5f-553a-47ce-85fb-f9902c9990ab
description: Das Abonnement-Element enthält die Eigenschaften verwendet, um ein Abonnement zu kündigen.
ms.openlocfilehash: bab797ff74a921e3e93c993229bc6d6d289e0c5c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839331"
---
# <a name="unsubscribe"></a><span data-ttu-id="47663-103">Kündigen eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="47663-103">Unsubscribe</span></span>

<span data-ttu-id="47663-104">Das **Abonnement** -Element enthält die Eigenschaften verwendet, um ein Abonnement zu kündigen.</span><span class="sxs-lookup"><span data-stu-id="47663-104">The **Unsubscribe** element contains the properties used to unsubscribe from a subscription.</span></span> 
  
[<span data-ttu-id="47663-105">Melden Sie sich ab</span><span class="sxs-lookup"><span data-stu-id="47663-105">Unsubscribe</span></span>](unsubscribe.md)
  
```xml
<Unsubscribe>
   <SubscriptionId/>
</Unsubscribe>
```

 <span data-ttu-id="47663-106">**UnsubscribeType**</span><span class="sxs-lookup"><span data-stu-id="47663-106">**UnsubscribeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="47663-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="47663-107">Attributes and elements</span></span>

<span data-ttu-id="47663-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="47663-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="47663-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="47663-109">Attributes</span></span>

<span data-ttu-id="47663-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="47663-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="47663-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="47663-111">Child elements</span></span>

|<span data-ttu-id="47663-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="47663-112">**Element**</span></span>|<span data-ttu-id="47663-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="47663-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="47663-114">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="47663-114">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="47663-115">Stellt den Bezeichner für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="47663-115">Represents the identifier for a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="47663-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="47663-116">Parent elements</span></span>

<span data-ttu-id="47663-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="47663-117">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="47663-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="47663-118">Remarks</span></span>

<span data-ttu-id="47663-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="47663-119">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="47663-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="47663-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47663-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="47663-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="47663-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="47663-122">Schema name</span></span>  <br/> |<span data-ttu-id="47663-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="47663-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="47663-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="47663-124">Validation file</span></span>  <br/> |<span data-ttu-id="47663-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="47663-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="47663-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="47663-126">Can be empty</span></span>  <br/> |<span data-ttu-id="47663-127">False</span><span class="sxs-lookup"><span data-stu-id="47663-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="47663-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47663-128">See also</span></span>



[<span data-ttu-id="47663-129">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="47663-129">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="47663-130">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="47663-130">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="47663-131">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="47663-131">Unsubscribe operation</span></span>](unsubscribe-operation.md)

