---
title: RootAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RootAddress
api_type:
- schema
ms.assetid: 1dbb130a-e4eb-4baf-ae07-2568a8375bff
description: Das Element RootAddress stellt die erste Adresse, die das Ereignis für ein Ereignis RecipientTrackingEvent beginnt.
ms.openlocfilehash: afe544d6ee8dea4cb416ad033ed2cd68976ec087
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831250"
---
# <a name="rootaddress"></a><span data-ttu-id="6ed61-103">RootAddress</span><span class="sxs-lookup"><span data-stu-id="6ed61-103">RootAddress</span></span>

<span data-ttu-id="6ed61-104">Das Element **RootAddress** stellt die erste Adresse, die das Ereignis für ein Ereignis [RecipientTrackingEvent](recipienttrackingevent.md) beginnt.</span><span class="sxs-lookup"><span data-stu-id="6ed61-104">The **RootAddress** element represents the first address that starts the event for a [RecipientTrackingEvent](recipienttrackingevent.md) event.</span></span> 
  
```xml
<RootAddress/>
```

 <span data-ttu-id="6ed61-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="6ed61-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6ed61-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6ed61-106">Attributes and elements</span></span>

<span data-ttu-id="6ed61-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6ed61-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6ed61-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6ed61-108">Attributes</span></span>

<span data-ttu-id="6ed61-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6ed61-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6ed61-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6ed61-110">Child elements</span></span>

<span data-ttu-id="6ed61-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="6ed61-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6ed61-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6ed61-112">Parent elements</span></span>

|<span data-ttu-id="6ed61-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6ed61-113">**Element**</span></span>|<span data-ttu-id="6ed61-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ed61-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ed61-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="6ed61-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="6ed61-116">Enthält Informationen für ein einzelnes Ereignis für einen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="6ed61-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6ed61-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="6ed61-117">Text value</span></span>

<span data-ttu-id="6ed61-118">Der Textwert ist die Adresse, die das Ereignis Tracking beginnt.</span><span class="sxs-lookup"><span data-stu-id="6ed61-118">The text value is the address that starts the tracking event.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6ed61-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6ed61-119">Remarks</span></span>

<span data-ttu-id="6ed61-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6ed61-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6ed61-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6ed61-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ed61-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ed61-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6ed61-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6ed61-123">Schema Name</span></span>  <br/> |<span data-ttu-id="6ed61-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6ed61-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="6ed61-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6ed61-125">Validation File</span></span>  <br/> |<span data-ttu-id="6ed61-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6ed61-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6ed61-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6ed61-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="6ed61-128">False</span><span class="sxs-lookup"><span data-stu-id="6ed61-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ed61-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ed61-129">See also</span></span>



[<span data-ttu-id="6ed61-130">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6ed61-130">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="6ed61-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6ed61-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

