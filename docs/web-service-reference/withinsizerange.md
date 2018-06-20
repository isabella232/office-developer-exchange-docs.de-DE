---
title: WithinSizeRange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WithinSizeRange
api_type:
- schema
ms.assetid: 6f98650e-3399-4f87-9b7f-40bf20cdb821
description: Das WithinSizeRange-Element gibt die minimale und maximale Größe, die eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.
ms.openlocfilehash: 7711db9ca68f972f080c98197e30c7710620119a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839545"
---
# <a name="withinsizerange"></a><span data-ttu-id="35246-103">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="35246-103">WithinSizeRange</span></span>

<span data-ttu-id="35246-104">Das **WithinSizeRange** -Element gibt die minimale und maximale Größe, die eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="35246-104">The **WithinSizeRange** element specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span> 
  
```XML
<WithinSizeRange>
     <MinimumSize/>
     <MaximumSize/>
</WithinSizeRange>
```

 <span data-ttu-id="35246-105">**RulePredicateSizeRangeType**</span><span class="sxs-lookup"><span data-stu-id="35246-105">**RulePredicateSizeRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="35246-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="35246-106">Attributes and elements</span></span>

<span data-ttu-id="35246-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="35246-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="35246-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="35246-108">Attributes</span></span>

<span data-ttu-id="35246-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="35246-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="35246-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="35246-110">Child elements</span></span>

|<span data-ttu-id="35246-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="35246-111">**Element**</span></span>|<span data-ttu-id="35246-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="35246-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="35246-113">MinimumSize</span><span class="sxs-lookup"><span data-stu-id="35246-113">MinimumSize</span></span>](minimumsize.md) <br/> |<span data-ttu-id="35246-114">Gibt die minimale Größe, die eine Nachricht in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="35246-114">Specifies the minimum size that a message must be in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="35246-115">Max</span><span class="sxs-lookup"><span data-stu-id="35246-115">MaximumSize</span></span>](maximumsize.md) <br/> |<span data-ttu-id="35246-116">Gibt die maximale Größe, die eine Nachricht in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="35246-116">Specifies the maximum size that a message must be in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="35246-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="35246-117">Parent elements</span></span>

|<span data-ttu-id="35246-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="35246-118">**Element**</span></span>|<span data-ttu-id="35246-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="35246-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="35246-120">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="35246-120">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="35246-121">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="35246-121">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="35246-122">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="35246-122">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="35246-123">Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel an.</span><span class="sxs-lookup"><span data-stu-id="35246-123">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="35246-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="35246-124">Text value</span></span>

<span data-ttu-id="35246-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="35246-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="35246-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="35246-126">Remarks</span></span>

<span data-ttu-id="35246-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="35246-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="35246-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="35246-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35246-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="35246-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="35246-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="35246-130">Schema Name</span></span>  <br/> |<span data-ttu-id="35246-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="35246-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="35246-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="35246-132">Validation File</span></span>  <br/> |<span data-ttu-id="35246-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="35246-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="35246-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="35246-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="35246-135">True</span><span class="sxs-lookup"><span data-stu-id="35246-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="35246-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35246-136">See also</span></span>



- [<span data-ttu-id="35246-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="35246-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

