---
title: Abonnement kündigen
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
description: Das unsubscribe-Element enthält die Eigenschaften, mit denen das Abonnement eines Abonnements gekündigt wird.
ms.openlocfilehash: d3d9c3bf9ad97cc0fdabf574c6505c797583838a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467214"
---
# <a name="unsubscribe"></a><span data-ttu-id="f21b0-103">Abonnement kündigen</span><span class="sxs-lookup"><span data-stu-id="f21b0-103">Unsubscribe</span></span>

<span data-ttu-id="f21b0-104">Das **unsubscribe** -Element enthält die Eigenschaften, mit denen das Abonnement eines Abonnements gekündigt wird.</span><span class="sxs-lookup"><span data-stu-id="f21b0-104">The **Unsubscribe** element contains the properties used to unsubscribe from a subscription.</span></span> 
  
[<span data-ttu-id="f21b0-105">Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="f21b0-105">Unsubscribe</span></span>](unsubscribe.md)
  
```xml
<Unsubscribe>
   <SubscriptionId/>
</Unsubscribe>
```

 <span data-ttu-id="f21b0-106">**Unsubscribetype**</span><span class="sxs-lookup"><span data-stu-id="f21b0-106">**UnsubscribeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f21b0-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f21b0-107">Attributes and elements</span></span>

<span data-ttu-id="f21b0-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f21b0-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f21b0-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="f21b0-109">Attributes</span></span>

<span data-ttu-id="f21b0-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="f21b0-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f21b0-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f21b0-111">Child elements</span></span>

|<span data-ttu-id="f21b0-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="f21b0-112">**Element**</span></span>|<span data-ttu-id="f21b0-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f21b0-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f21b0-114">Abonnement-Nr (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="f21b0-114">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="f21b0-115">Stellt den Bezeichner für ein Abonnement dar.</span><span class="sxs-lookup"><span data-stu-id="f21b0-115">Represents the identifier for a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f21b0-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f21b0-116">Parent elements</span></span>

<span data-ttu-id="f21b0-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="f21b0-117">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f21b0-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f21b0-118">Remarks</span></span>

<span data-ttu-id="f21b0-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f21b0-119">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f21b0-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f21b0-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f21b0-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="f21b0-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f21b0-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f21b0-122">Schema name</span></span>  <br/> |<span data-ttu-id="f21b0-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f21b0-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f21b0-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f21b0-124">Validation file</span></span>  <br/> |<span data-ttu-id="f21b0-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f21b0-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f21b0-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f21b0-126">Can be empty</span></span>  <br/> |<span data-ttu-id="f21b0-127">False</span><span class="sxs-lookup"><span data-stu-id="f21b0-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f21b0-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f21b0-128">See also</span></span>



[<span data-ttu-id="f21b0-129">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="f21b0-129">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="f21b0-130">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f21b0-130">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="f21b0-131">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="f21b0-131">Unsubscribe operation</span></span>](unsubscribe-operation.md)

