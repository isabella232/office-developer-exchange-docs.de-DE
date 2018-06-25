---
title: DisableReason
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f41b5be6-9b79-4e83-8cdb-aa779e13cb3f
description: Das DisableReason-Element gibt den Grund für die Deaktivierung einer app.
ms.openlocfilehash: f900bd1b98b294900f767c778b9c5f87f74042ca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758011"
---
# <a name="disablereason"></a><span data-ttu-id="b82ae-103">DisableReason</span><span class="sxs-lookup"><span data-stu-id="b82ae-103">DisableReason</span></span>

<span data-ttu-id="b82ae-104">Das **DisableReason** -Element gibt den Grund für die Deaktivierung einer app.</span><span class="sxs-lookup"><span data-stu-id="b82ae-104">The **DisableReason** element specifies the reason for disabling an app.</span></span> 
  
```XML
<DisableReason> NoReason | OutlookClientPerformance | OWAClientPerformance | MobileClientPerformance </DisableReason>
```

 <span data-ttu-id="b82ae-105">**DisableReasonType**</span><span class="sxs-lookup"><span data-stu-id="b82ae-105">**DisableReasonType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b82ae-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b82ae-106">Attributes and elements</span></span>

<span data-ttu-id="b82ae-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b82ae-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b82ae-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b82ae-108">Attributes</span></span>

<span data-ttu-id="b82ae-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b82ae-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b82ae-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b82ae-110">Child elements</span></span>

<span data-ttu-id="b82ae-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b82ae-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b82ae-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b82ae-112">Parent elements</span></span>

|<span data-ttu-id="b82ae-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b82ae-113">**Element**</span></span>|<span data-ttu-id="b82ae-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b82ae-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b82ae-115">DisableApp</span><span class="sxs-lookup"><span data-stu-id="b82ae-115">DisableApp</span></span>](disableapp.md) <br/> |<span data-ttu-id="b82ae-116">Gibt eine Anforderung an eine app zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b82ae-116">Specifies a request to disable an app.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b82ae-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="b82ae-117">Text value</span></span>

<span data-ttu-id="b82ae-118">**DisableReason Elementwert text**</span><span class="sxs-lookup"><span data-stu-id="b82ae-118">**DisableReason element text value**</span></span>

|<span data-ttu-id="b82ae-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b82ae-119">**Value**</span></span>|<span data-ttu-id="b82ae-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b82ae-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b82ae-121">NoReason</span><span class="sxs-lookup"><span data-stu-id="b82ae-121">NoReason</span></span>  <br/> |<span data-ttu-id="b82ae-122">Kein Grund angegeben</span><span class="sxs-lookup"><span data-stu-id="b82ae-122">No reason given</span></span>  <br/> |
|<span data-ttu-id="b82ae-123">OutlookClientPerformance</span><span class="sxs-lookup"><span data-stu-id="b82ae-123">OutlookClientPerformance</span></span>  <br/> |<span data-ttu-id="b82ae-124">Zum Verbessern der Leistung der e-Mail-Client.</span><span class="sxs-lookup"><span data-stu-id="b82ae-124">To improve email client performance.</span></span>  <br/> |
|<span data-ttu-id="b82ae-125">OWAClientPerformance</span><span class="sxs-lookup"><span data-stu-id="b82ae-125">OWAClientPerformance</span></span>  <br/> |<span data-ttu-id="b82ae-126">Zur Verbesserung der Leistung von Web app-Client.</span><span class="sxs-lookup"><span data-stu-id="b82ae-126">To improve Web app client performance.</span></span>  <br/> |
|<span data-ttu-id="b82ae-127">MobileClientPerformance</span><span class="sxs-lookup"><span data-stu-id="b82ae-127">MobileClientPerformance</span></span>  <br/> |<span data-ttu-id="b82ae-128">Zum Verbessern der Leistung von mobilen Clients.</span><span class="sxs-lookup"><span data-stu-id="b82ae-128">To improve mobile client performance.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b82ae-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b82ae-129">Remarks</span></span>

<span data-ttu-id="b82ae-130">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b82ae-130">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b82ae-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b82ae-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b82ae-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b82ae-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b82ae-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="b82ae-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b82ae-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b82ae-134">Schema Name</span></span>  <br/> |<span data-ttu-id="b82ae-135">Typschema</span><span class="sxs-lookup"><span data-stu-id="b82ae-135">Type schema</span></span>  <br/> |
|<span data-ttu-id="b82ae-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b82ae-136">Validation File</span></span>  <br/> |<span data-ttu-id="b82ae-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b82ae-137">types.xsd</span></span>  <br/> |
|<span data-ttu-id="b82ae-138">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b82ae-138">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="b82ae-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b82ae-139">See also</span></span>

- [<span data-ttu-id="b82ae-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b82ae-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

