---
title: ErrorSubscriptionIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrorSubscriptionIds
api_type:
- schema
ms.assetid: e64e76ff-4d98-4082-9acc-a1114ae45f44
description: Das ErrorSubscriptionIds-Element enthält ein Array von ungültigen Abonnement-IDs.
ms.openlocfilehash: bdc5c86560800464d677a9043607bed3f7872e32
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526186"
---
# <a name="errorsubscriptionids"></a><span data-ttu-id="e5463-103">ErrorSubscriptionIds</span><span class="sxs-lookup"><span data-stu-id="e5463-103">ErrorSubscriptionIds</span></span>

<span data-ttu-id="e5463-104">Das **ErrorSubscriptionIds** -Element enthält ein Array von ungültigen Abonnement-IDs.</span><span class="sxs-lookup"><span data-stu-id="e5463-104">The **ErrorSubscriptionIds** element contains an array of invalid subscription IDs.</span></span> 
  
```xml
<ErrorSubscriptionIds>
   <SubscriptionId/>
</ErrorSubscriptionIds>
```

 <span data-ttu-id="e5463-105">**NonEmptyArrayOfSubscriptionIdsType**</span><span class="sxs-lookup"><span data-stu-id="e5463-105">**NonEmptyArrayOfSubscriptionIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e5463-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e5463-106">Attributes and elements</span></span>

<span data-ttu-id="e5463-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e5463-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e5463-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e5463-108">Attributes</span></span>

<span data-ttu-id="e5463-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e5463-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e5463-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e5463-110">Child elements</span></span>

|<span data-ttu-id="e5463-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e5463-111">**Element**</span></span>|<span data-ttu-id="e5463-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e5463-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e5463-113">Abonnement-Nr (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="e5463-113">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="e5463-114">Stellt den Bezeichner für ein Abonnement dar.</span><span class="sxs-lookup"><span data-stu-id="e5463-114">Represents the identifier for a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e5463-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e5463-115">Parent elements</span></span>

|<span data-ttu-id="e5463-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="e5463-116">**Element**</span></span>|<span data-ttu-id="e5463-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e5463-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e5463-118">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e5463-118">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md) <br/> |<span data-ttu-id="e5463-119">Enthält den Status und das Ergebnis einer einzelnen [GetStreamingEvents-Vorgangs](getstreamingevents-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e5463-119">Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e5463-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="e5463-120">Text value</span></span>

<span data-ttu-id="e5463-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="e5463-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e5463-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5463-122">Remarks</span></span>

<span data-ttu-id="e5463-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e5463-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e5463-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e5463-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5463-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5463-125">Namespace</span></span>  <br/> |<span data-ttu-id="e5463-126">https://schemas.microsoft.com/exchange/services/2006/messages und https://schemas.microsoft.com/exchange/services/2006/types</span><span class="sxs-lookup"><span data-stu-id="e5463-126">https://schemas.microsoft.com/exchange/services/2006/messages and https://schemas.microsoft.com/exchange/services/2006/types</span></span>  <br/> |
|<span data-ttu-id="e5463-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e5463-127">Schema Name</span></span>  <br/> |<span data-ttu-id="e5463-128">Nachrichtenschema; Typenschema</span><span class="sxs-lookup"><span data-stu-id="e5463-128">Messages schema; Types schema</span></span>  <br/> |
|<span data-ttu-id="e5463-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e5463-129">Validation File</span></span>  <br/> |<span data-ttu-id="e5463-130">Messages. xsd; Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e5463-130">Messages.xsd; Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e5463-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e5463-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="e5463-132">False</span><span class="sxs-lookup"><span data-stu-id="e5463-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e5463-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5463-133">See also</span></span>



[<span data-ttu-id="e5463-134">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e5463-134">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)


- [<span data-ttu-id="e5463-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e5463-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

