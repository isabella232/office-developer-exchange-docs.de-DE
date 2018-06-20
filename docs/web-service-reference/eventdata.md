---
title: EventData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EventData
api_type:
- schema
ms.assetid: 74acdbad-d6ee-47e6-82fb-e45ecaaa0500
description: Das Element EventData stellt Daten, die im Verarbeitungsschritt für das Ereignis zugeordnet ist.
ms.openlocfilehash: 2bf38cd4fd956580b31b6e455b947066f07f5593
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758279"
---
# <a name="eventdata"></a><span data-ttu-id="d1f7a-103">EventData</span><span class="sxs-lookup"><span data-stu-id="d1f7a-103">EventData</span></span>

<span data-ttu-id="d1f7a-104">Das Element **EventData** stellt Daten, die im Verarbeitungsschritt für das Ereignis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d1f7a-104">The **EventData** element represents data that is associated with the processing step for the event.</span></span> 
  
```XML
<EventData>
   <String/>
</EventData>
```

 <span data-ttu-id="d1f7a-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="d1f7a-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d1f7a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d1f7a-106">Attributes and elements</span></span>

<span data-ttu-id="d1f7a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d1f7a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d1f7a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d1f7a-108">Attributes</span></span>

<span data-ttu-id="d1f7a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d1f7a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d1f7a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d1f7a-110">Child elements</span></span>

|<span data-ttu-id="d1f7a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d1f7a-111">**Element**</span></span>|<span data-ttu-id="d1f7a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d1f7a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d1f7a-113">String</span><span class="sxs-lookup"><span data-stu-id="d1f7a-113">String</span></span>](string.md) <br/> |<span data-ttu-id="d1f7a-114">Enthält eine Zeichenfolge zur Identifizierung ein Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="d1f7a-114">Contains a string that identifies an event.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d1f7a-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d1f7a-115">Parent elements</span></span>

|<span data-ttu-id="d1f7a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d1f7a-116">**Element**</span></span>|<span data-ttu-id="d1f7a-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d1f7a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d1f7a-118">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="d1f7a-118">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="d1f7a-119">Enthält Informationen für ein einzelnes Ereignis für einen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="d1f7a-119">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d1f7a-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="d1f7a-120">Text value</span></span>

<span data-ttu-id="d1f7a-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="d1f7a-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1f7a-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d1f7a-122">Remarks</span></span>

<span data-ttu-id="d1f7a-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d1f7a-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d1f7a-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d1f7a-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1f7a-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1f7a-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d1f7a-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d1f7a-126">Schema Name</span></span>  <br/> |<span data-ttu-id="d1f7a-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d1f7a-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="d1f7a-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d1f7a-128">Validation File</span></span>  <br/> |<span data-ttu-id="d1f7a-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d1f7a-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d1f7a-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d1f7a-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="d1f7a-131">False</span><span class="sxs-lookup"><span data-stu-id="d1f7a-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d1f7a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1f7a-132">See also</span></span>



- [<span data-ttu-id="d1f7a-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d1f7a-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

