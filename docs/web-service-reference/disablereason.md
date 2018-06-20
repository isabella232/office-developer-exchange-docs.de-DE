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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758011"
---
# <a name="disablereason"></a><span data-ttu-id="bb64b-103">DisableReason</span><span class="sxs-lookup"><span data-stu-id="bb64b-103">DisableReason</span></span>

<span data-ttu-id="bb64b-104">Das **DisableReason** -Element gibt den Grund für die Deaktivierung einer app.</span><span class="sxs-lookup"><span data-stu-id="bb64b-104">The **DisableReason** element specifies the reason for disabling an app.</span></span> 
  
```XML
<DisableReason> NoReason | OutlookClientPerformance | OWAClientPerformance | MobileClientPerformance </DisableReason>
```

 <span data-ttu-id="bb64b-105">**DisableReasonType**</span><span class="sxs-lookup"><span data-stu-id="bb64b-105">**DisableReasonType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bb64b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bb64b-106">Attributes and elements</span></span>

<span data-ttu-id="bb64b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bb64b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb64b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="bb64b-108">Attributes</span></span>

<span data-ttu-id="bb64b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="bb64b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bb64b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bb64b-110">Child elements</span></span>

<span data-ttu-id="bb64b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="bb64b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bb64b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bb64b-112">Parent elements</span></span>

|<span data-ttu-id="bb64b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bb64b-113">**Element**</span></span>|<span data-ttu-id="bb64b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bb64b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb64b-115">DisableApp</span><span class="sxs-lookup"><span data-stu-id="bb64b-115">DisableApp</span></span>](disableapp.md) <br/> |<span data-ttu-id="bb64b-116">Gibt eine Anforderung an eine app zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="bb64b-116">Specifies a request to disable an app.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bb64b-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="bb64b-117">Text value</span></span>

<span data-ttu-id="bb64b-118">**DisableReason Elementwert text**</span><span class="sxs-lookup"><span data-stu-id="bb64b-118">**DisableReason element text value**</span></span>

|<span data-ttu-id="bb64b-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="bb64b-119">**Value**</span></span>|<span data-ttu-id="bb64b-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bb64b-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bb64b-121">NoReason</span><span class="sxs-lookup"><span data-stu-id="bb64b-121">NoReason</span></span>  <br/> |<span data-ttu-id="bb64b-122">Kein Grund angegeben</span><span class="sxs-lookup"><span data-stu-id="bb64b-122">No reason given</span></span>  <br/> |
|<span data-ttu-id="bb64b-123">OutlookClientPerformance</span><span class="sxs-lookup"><span data-stu-id="bb64b-123">OutlookClientPerformance</span></span>  <br/> |<span data-ttu-id="bb64b-124">Zum Verbessern der Leistung der e-Mail-Client.</span><span class="sxs-lookup"><span data-stu-id="bb64b-124">To improve email client performance.</span></span>  <br/> |
|<span data-ttu-id="bb64b-125">OWAClientPerformance</span><span class="sxs-lookup"><span data-stu-id="bb64b-125">OWAClientPerformance</span></span>  <br/> |<span data-ttu-id="bb64b-126">Zur Verbesserung der Leistung von Web app-Client.</span><span class="sxs-lookup"><span data-stu-id="bb64b-126">To improve Web app client performance.</span></span>  <br/> |
|<span data-ttu-id="bb64b-127">MobileClientPerformance</span><span class="sxs-lookup"><span data-stu-id="bb64b-127">MobileClientPerformance</span></span>  <br/> |<span data-ttu-id="bb64b-128">Zum Verbessern der Leistung von mobilen Clients.</span><span class="sxs-lookup"><span data-stu-id="bb64b-128">To improve mobile client performance.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb64b-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bb64b-129">Remarks</span></span>

<span data-ttu-id="bb64b-130">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bb64b-130">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="bb64b-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="bb64b-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bb64b-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bb64b-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb64b-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="bb64b-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bb64b-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bb64b-134">Schema Name</span></span>  <br/> |<span data-ttu-id="bb64b-135">Typschema</span><span class="sxs-lookup"><span data-stu-id="bb64b-135">Type schema</span></span>  <br/> |
|<span data-ttu-id="bb64b-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bb64b-136">Validation File</span></span>  <br/> |<span data-ttu-id="bb64b-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bb64b-137">types.xsd</span></span>  <br/> |
|<span data-ttu-id="bb64b-138">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="bb64b-138">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="bb64b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb64b-139">See also</span></span>

- [<span data-ttu-id="bb64b-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bb64b-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

