---
title: ItemClasses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemClasses
api_type:
- schema
ms.assetid: f95430cc-2860-47c1-af2d-8c4156c9b281
description: Das ItemClasses-Element stellt die Elementklassen dar, die für eingehende Nachrichten gestempelt werden müssen, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 56b99cad2abef0a9953e1793e5b633acca83a9eb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460113"
---
# <a name="itemclasses"></a><span data-ttu-id="52f83-103">ItemClasses</span><span class="sxs-lookup"><span data-stu-id="52f83-103">ItemClasses</span></span>

<span data-ttu-id="52f83-104">Das **ItemClasses** -Element stellt die Elementklassen dar, die für eingehende Nachrichten gestempelt werden müssen, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="52f83-104">The **ItemClasses** element represents the item classes that must be stamped on incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ItemClasses>
    <String/>
</ItemClasses>
```

 <span data-ttu-id="52f83-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="52f83-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52f83-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="52f83-106">Attributes and elements</span></span>

<span data-ttu-id="52f83-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="52f83-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52f83-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="52f83-108">Attributes</span></span>

<span data-ttu-id="52f83-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="52f83-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="52f83-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="52f83-110">Child elements</span></span>

|<span data-ttu-id="52f83-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="52f83-111">**Element**</span></span>|<span data-ttu-id="52f83-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="52f83-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52f83-113">String</span><span class="sxs-lookup"><span data-stu-id="52f83-113">String</span></span>](string.md) <br/> |<span data-ttu-id="52f83-114">Stellt eine einzelne Elementklasse dar.</span><span class="sxs-lookup"><span data-stu-id="52f83-114">Represents a single item class.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="52f83-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="52f83-115">Parent elements</span></span>

|<span data-ttu-id="52f83-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="52f83-116">**Element**</span></span>|<span data-ttu-id="52f83-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="52f83-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52f83-118">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="52f83-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="52f83-119">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="52f83-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="52f83-120">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="52f83-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="52f83-121">Stellt die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen.</span><span class="sxs-lookup"><span data-stu-id="52f83-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="52f83-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="52f83-122">Text value</span></span>

<span data-ttu-id="52f83-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="52f83-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52f83-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52f83-124">Remarks</span></span>

<span data-ttu-id="52f83-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="52f83-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52f83-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="52f83-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52f83-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="52f83-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="52f83-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="52f83-128">Schema name</span></span>  <br/> |<span data-ttu-id="52f83-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="52f83-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="52f83-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="52f83-130">Validation file</span></span>  <br/> |<span data-ttu-id="52f83-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="52f83-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="52f83-132">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="52f83-132">Can be empty</span></span>  <br/> |<span data-ttu-id="52f83-133">False</span><span class="sxs-lookup"><span data-stu-id="52f83-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52f83-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52f83-134">See also</span></span>



- [<span data-ttu-id="52f83-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="52f83-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

