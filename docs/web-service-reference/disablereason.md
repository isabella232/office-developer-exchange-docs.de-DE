---
title: DisableReason
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f41b5be6-9b79-4e83-8cdb-aa779e13cb3f
description: Das DisableReason-Element gibt den Grund für das Deaktivieren einer APP an.
ms.openlocfilehash: 1406d69647bde5389dc9bb61adf7537a57d5adfc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463671"
---
# <a name="disablereason"></a><span data-ttu-id="2aea5-103">DisableReason</span><span class="sxs-lookup"><span data-stu-id="2aea5-103">DisableReason</span></span>

<span data-ttu-id="2aea5-104">Das **DisableReason** -Element gibt den Grund für das Deaktivieren einer APP an.</span><span class="sxs-lookup"><span data-stu-id="2aea5-104">The **DisableReason** element specifies the reason for disabling an app.</span></span> 
  
```XML
<DisableReason> NoReason | OutlookClientPerformance | OWAClientPerformance | MobileClientPerformance </DisableReason>
```

 <span data-ttu-id="2aea5-105">**DisableReasonType**</span><span class="sxs-lookup"><span data-stu-id="2aea5-105">**DisableReasonType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2aea5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2aea5-106">Attributes and elements</span></span>

<span data-ttu-id="2aea5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2aea5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2aea5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2aea5-108">Attributes</span></span>

<span data-ttu-id="2aea5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2aea5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2aea5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2aea5-110">Child elements</span></span>

<span data-ttu-id="2aea5-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2aea5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2aea5-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2aea5-112">Parent elements</span></span>

|<span data-ttu-id="2aea5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2aea5-113">**Element**</span></span>|<span data-ttu-id="2aea5-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2aea5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2aea5-115">DisableApp</span><span class="sxs-lookup"><span data-stu-id="2aea5-115">DisableApp</span></span>](disableapp.md) <br/> |<span data-ttu-id="2aea5-116">Gibt eine Anforderung zum Deaktivieren einer APP an.</span><span class="sxs-lookup"><span data-stu-id="2aea5-116">Specifies a request to disable an app.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2aea5-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="2aea5-117">Text value</span></span>

<span data-ttu-id="2aea5-118">**DisableReason-Element Text Wert**</span><span class="sxs-lookup"><span data-stu-id="2aea5-118">**DisableReason element text value**</span></span>

|<span data-ttu-id="2aea5-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2aea5-119">**Value**</span></span>|<span data-ttu-id="2aea5-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2aea5-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2aea5-121">Noreason</span><span class="sxs-lookup"><span data-stu-id="2aea5-121">NoReason</span></span>  <br/> |<span data-ttu-id="2aea5-122">Kein Grund angegeben</span><span class="sxs-lookup"><span data-stu-id="2aea5-122">No reason given</span></span>  <br/> |
|<span data-ttu-id="2aea5-123">OutlookClientPerformance</span><span class="sxs-lookup"><span data-stu-id="2aea5-123">OutlookClientPerformance</span></span>  <br/> |<span data-ttu-id="2aea5-124">Zur Verbesserung der Leistung von e-Mail-Clients.</span><span class="sxs-lookup"><span data-stu-id="2aea5-124">To improve email client performance.</span></span>  <br/> |
|<span data-ttu-id="2aea5-125">OWAClientPerformance</span><span class="sxs-lookup"><span data-stu-id="2aea5-125">OWAClientPerformance</span></span>  <br/> |<span data-ttu-id="2aea5-126">Zur Verbesserung der Leistung von webapp-Clients.</span><span class="sxs-lookup"><span data-stu-id="2aea5-126">To improve Web app client performance.</span></span>  <br/> |
|<span data-ttu-id="2aea5-127">MobileClientPerformance</span><span class="sxs-lookup"><span data-stu-id="2aea5-127">MobileClientPerformance</span></span>  <br/> |<span data-ttu-id="2aea5-128">Um die Leistung des mobilen Clients zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="2aea5-128">To improve mobile client performance.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2aea5-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2aea5-129">Remarks</span></span>

<span data-ttu-id="2aea5-130">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2aea5-130">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2aea5-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2aea5-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2aea5-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2aea5-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2aea5-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="2aea5-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2aea5-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2aea5-134">Schema Name</span></span>  <br/> |<span data-ttu-id="2aea5-135">Typschema</span><span class="sxs-lookup"><span data-stu-id="2aea5-135">Type schema</span></span>  <br/> |
|<span data-ttu-id="2aea5-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2aea5-136">Validation File</span></span>  <br/> |<span data-ttu-id="2aea5-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="2aea5-137">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2aea5-138">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2aea5-138">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2aea5-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2aea5-139">See also</span></span>

- [<span data-ttu-id="2aea5-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2aea5-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

