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
description: Das Timeout-Element stellt die Dauer in Minuten dar, in der das Abonnement im Leerlauf bleiben kann, ohne eine GetEvents-Anforderung vom Client zu erhalten.
ms.openlocfilehash: 6f3228cd480bf0eaf259c4f321bc74d0845b9bba
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459896"
---
# <a name="timeout"></a><span data-ttu-id="a9176-103">Timeout</span><span class="sxs-lookup"><span data-stu-id="a9176-103">Timeout</span></span>

<span data-ttu-id="a9176-104">Das **Timeout** -Element stellt die Dauer in Minuten dar, in der das Abonnement im Leerlauf bleiben kann, ohne eine GetEvents-Anforderung vom Client zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a9176-104">The **Timeout** element represents the duration, in minutes, that the subscription can remain idle without a GetEvents request from the client.</span></span> 
  
```xml
<Timeout/>
```

 <span data-ttu-id="a9176-105">**int**</span><span class="sxs-lookup"><span data-stu-id="a9176-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a9176-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a9176-106">Attributes and elements</span></span>

<span data-ttu-id="a9176-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a9176-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a9176-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a9176-108">Attributes</span></span>

<span data-ttu-id="a9176-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a9176-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a9176-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a9176-110">Child elements</span></span>

<span data-ttu-id="a9176-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="a9176-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a9176-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a9176-112">Parent elements</span></span>

|<span data-ttu-id="a9176-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9176-113">**Element**</span></span>|<span data-ttu-id="a9176-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9176-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9176-115">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="a9176-115">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="a9176-116">Stellt ein Abonnement für ein Pull-basiertes Ereignis Benachrichtigungsabonnement dar.</span><span class="sxs-lookup"><span data-stu-id="a9176-116">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a9176-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="a9176-117">Text value</span></span>

<span data-ttu-id="a9176-118">Ein Textwert, der eine ganze Zahl darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9176-118">A text value that represents an integer is required if this element is used.</span></span> <span data-ttu-id="a9176-119">Die möglichen Werte für dieses Element sind 1 bis 1440, einschließlich.</span><span class="sxs-lookup"><span data-stu-id="a9176-119">The possible values for this element are 1 to 1440, inclusive.</span></span> <span data-ttu-id="a9176-120">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a9176-120">This element is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a9176-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9176-121">Remarks</span></span>

<span data-ttu-id="a9176-122">Der Timeout-Zeitgeber für das Abonnement wird durch eine erfolgreiche GetEvents-Anforderung zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="a9176-122">The timeout timer for the subscription is reset by a successful GetEvents request.</span></span>
  
<span data-ttu-id="a9176-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a9176-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="a9176-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a9176-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9176-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="a9176-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a9176-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a9176-126">Schema name</span></span>  <br/> |<span data-ttu-id="a9176-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a9176-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="a9176-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a9176-128">Validation file</span></span>  <br/> |<span data-ttu-id="a9176-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a9176-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a9176-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a9176-130">Can be empty</span></span>  <br/> |<span data-ttu-id="a9176-131">False</span><span class="sxs-lookup"><span data-stu-id="a9176-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9176-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9176-132">See also</span></span>



[<span data-ttu-id="a9176-133">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="a9176-133">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="a9176-134">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a9176-134">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="a9176-135">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="a9176-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)

