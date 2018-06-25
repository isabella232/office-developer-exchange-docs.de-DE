---
title: Timeout
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Timeout
api_type:
- schema
ms.assetid: c2e1ca5a-6667-4f6f-aac4-89de33bddc54
description: Das Timeout-Element stellt die Dauer in Minuten, die das Abonnement ohne GetEvents Anforderung vom Client im Leerlauf sein kann.
ms.openlocfilehash: 0a26002689e131959f09318b01d97ffb73b605f9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839210"
---
# <a name="timeout"></a><span data-ttu-id="bec1f-103">Timeout</span><span class="sxs-lookup"><span data-stu-id="bec1f-103">Timeout</span></span>

<span data-ttu-id="bec1f-104">Das **Timeout** -Element stellt die Dauer in Minuten, die das Abonnement ohne GetEvents Anforderung vom Client im Leerlauf sein kann.</span><span class="sxs-lookup"><span data-stu-id="bec1f-104">The **Timeout** element represents the duration, in minutes, that the subscription can remain idle without a GetEvents request from the client.</span></span> 
  
```xml
<Timeout/>
```

 <span data-ttu-id="bec1f-105">**int**</span><span class="sxs-lookup"><span data-stu-id="bec1f-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bec1f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bec1f-106">Attributes and elements</span></span>

<span data-ttu-id="bec1f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bec1f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bec1f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="bec1f-108">Attributes</span></span>

<span data-ttu-id="bec1f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="bec1f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bec1f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bec1f-110">Child elements</span></span>

<span data-ttu-id="bec1f-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="bec1f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bec1f-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bec1f-112">Parent elements</span></span>

|<span data-ttu-id="bec1f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bec1f-113">**Element**</span></span>|<span data-ttu-id="bec1f-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bec1f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bec1f-115">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="bec1f-115">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="bec1f-116">Stellt ein Abonnement für ein Benachrichtigungsabonnement Pull-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="bec1f-116">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bec1f-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="bec1f-117">Text value</span></span>

<span data-ttu-id="bec1f-118">Ein Textwert, der eine ganze Zahl darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bec1f-118">A text value that represents an integer is required if this element is used.</span></span> <span data-ttu-id="bec1f-119">Die möglichen Werte für dieses Element sind 1 bis 1440, inklusive.</span><span class="sxs-lookup"><span data-stu-id="bec1f-119">The possible values for this element are 1 to 1440, inclusive.</span></span> <span data-ttu-id="bec1f-120">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bec1f-120">This element is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bec1f-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bec1f-121">Remarks</span></span>

<span data-ttu-id="bec1f-122">Der Timeout-Zeitgeber für das Abonnement wird durch eine erfolgreiche GetEvents Anforderung zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="bec1f-122">The timeout timer for the subscription is reset by a successful GetEvents request.</span></span>
  
<span data-ttu-id="bec1f-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="bec1f-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="bec1f-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bec1f-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bec1f-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="bec1f-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bec1f-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bec1f-126">Schema name</span></span>  <br/> |<span data-ttu-id="bec1f-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="bec1f-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="bec1f-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bec1f-128">Validation file</span></span>  <br/> |<span data-ttu-id="bec1f-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bec1f-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bec1f-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="bec1f-130">Can be empty</span></span>  <br/> |<span data-ttu-id="bec1f-131">False</span><span class="sxs-lookup"><span data-stu-id="bec1f-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bec1f-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bec1f-132">See also</span></span>



[<span data-ttu-id="bec1f-133">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="bec1f-133">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="bec1f-134">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bec1f-134">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="bec1f-135">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="bec1f-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)

