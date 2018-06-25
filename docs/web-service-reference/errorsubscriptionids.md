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
description: Das ErrorSubscriptionIds-Element enthält ein Array von Ungültiges Abonnement IDs.
ms.openlocfilehash: 5cdbbeb1083754510f431bc092bb67dc0addecab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758276"
---
# <a name="errorsubscriptionids"></a><span data-ttu-id="66dcc-103">ErrorSubscriptionIds</span><span class="sxs-lookup"><span data-stu-id="66dcc-103">ErrorSubscriptionIds</span></span>

<span data-ttu-id="66dcc-104">Das **ErrorSubscriptionIds** -Element enthält ein Array von Ungültiges Abonnement IDs.</span><span class="sxs-lookup"><span data-stu-id="66dcc-104">The **ErrorSubscriptionIds** element contains an array of invalid subscription IDs.</span></span> 
  
```xml
<ErrorSubscriptionIds>
   <SubscriptionId/>
</ErrorSubscriptionIds>
```

 <span data-ttu-id="66dcc-105">**NonEmptyArrayOfSubscriptionIdsType**</span><span class="sxs-lookup"><span data-stu-id="66dcc-105">**NonEmptyArrayOfSubscriptionIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="66dcc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="66dcc-106">Attributes and elements</span></span>

<span data-ttu-id="66dcc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="66dcc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66dcc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="66dcc-108">Attributes</span></span>

<span data-ttu-id="66dcc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="66dcc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="66dcc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66dcc-110">Child elements</span></span>

|<span data-ttu-id="66dcc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="66dcc-111">**Element**</span></span>|<span data-ttu-id="66dcc-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66dcc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66dcc-113">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="66dcc-113">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="66dcc-114">Stellt den Bezeichner für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66dcc-114">Represents the identifier for a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="66dcc-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66dcc-115">Parent elements</span></span>

|<span data-ttu-id="66dcc-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="66dcc-116">**Element**</span></span>|<span data-ttu-id="66dcc-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66dcc-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66dcc-118">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="66dcc-118">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md) <br/> |<span data-ttu-id="66dcc-119">Enthält den Status und das Ergebnis einer einzelnen Anforderung [GetStreamingEvents Vorgang](getstreamingevents-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="66dcc-119">Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="66dcc-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="66dcc-120">Text value</span></span>

<span data-ttu-id="66dcc-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="66dcc-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="66dcc-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="66dcc-122">Remarks</span></span>

<span data-ttu-id="66dcc-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="66dcc-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66dcc-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="66dcc-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66dcc-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="66dcc-125">Namespace</span></span>  <br/> |<span data-ttu-id="66dcc-126">http://schemas.microsoft.com/exchange/services/2006/messages und http://schemas.microsoft.com/exchange/services/2006/types</span><span class="sxs-lookup"><span data-stu-id="66dcc-126">http://schemas.microsoft.com/exchange/services/2006/messages and http://schemas.microsoft.com/exchange/services/2006/types</span></span>  <br/> |
|<span data-ttu-id="66dcc-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="66dcc-127">Schema Name</span></span>  <br/> |<span data-ttu-id="66dcc-128">Nachrichten-schema Typen-schema</span><span class="sxs-lookup"><span data-stu-id="66dcc-128">Messages schema; Types schema</span></span>  <br/> |
|<span data-ttu-id="66dcc-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="66dcc-129">Validation File</span></span>  <br/> |<span data-ttu-id="66dcc-130">Messages.xsd; Types.xsd</span><span class="sxs-lookup"><span data-stu-id="66dcc-130">Messages.xsd; Types.xsd</span></span>  <br/> |
|<span data-ttu-id="66dcc-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="66dcc-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="66dcc-132">False</span><span class="sxs-lookup"><span data-stu-id="66dcc-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="66dcc-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66dcc-133">See also</span></span>



[<span data-ttu-id="66dcc-134">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="66dcc-134">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)


- [<span data-ttu-id="66dcc-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="66dcc-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

