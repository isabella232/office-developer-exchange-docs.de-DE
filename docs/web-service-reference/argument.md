---
title: Argument
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Argument
api_type:
- schema
ms.assetid: 15b0bfb8-2448-4ceb-aeac-965115e0fb72
description: Das Argument-Element gibt Argumente für die Aktion an.
ms.openlocfilehash: 41e3b1d891610669b0cc93f3daf6e8ee98c48396
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464756"
---
# <a name="argument"></a><span data-ttu-id="29298-103">Argument</span><span class="sxs-lookup"><span data-stu-id="29298-103">Argument</span></span>

<span data-ttu-id="29298-104">Das **Argument** -Element gibt Argumente für die Aktion an.</span><span class="sxs-lookup"><span data-stu-id="29298-104">The **Argument** element specifies arguments to the action.</span></span> 
  
```xml
<Argument Value=""/>
```

 <span data-ttu-id="29298-105">**ProtectionRuleArgumentType**</span><span class="sxs-lookup"><span data-stu-id="29298-105">**ProtectionRuleArgumentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="29298-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="29298-106">Attributes and elements</span></span>

<span data-ttu-id="29298-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="29298-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="29298-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="29298-108">Attributes</span></span>

|<span data-ttu-id="29298-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="29298-109">**Attribute**</span></span>|<span data-ttu-id="29298-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="29298-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="29298-111">**Wert**</span><span class="sxs-lookup"><span data-stu-id="29298-111">**Value**</span></span> <br/> |<span data-ttu-id="29298-112">Ein nicht leerer String-Wert, der den Wert eines Arguments für den Aktions Teil einer Schutz Regel darstellt.</span><span class="sxs-lookup"><span data-stu-id="29298-112">A non-empty string value that represents the value of an argument to the action part of a protection rule.</span></span> <span data-ttu-id="29298-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="29298-113">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="29298-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="29298-114">Child elements</span></span>

<span data-ttu-id="29298-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="29298-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="29298-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="29298-116">Parent elements</span></span>

|<span data-ttu-id="29298-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="29298-117">**Element**</span></span>|<span data-ttu-id="29298-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="29298-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="29298-119">Action (ProtectionRuleActionType)</span><span class="sxs-lookup"><span data-stu-id="29298-119">Action (ProtectionRuleActionType)</span></span>](action-protectionruleactiontype.md) <br/> |<span data-ttu-id="29298-120">Gibt an, welche Aktion ausgeführt werden muss, wenn der Bedingungsteil der Regel übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="29298-120">Identifies what action must be executed if the condition part of the rule matches.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="29298-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="29298-121">Text value</span></span>

<span data-ttu-id="29298-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="29298-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="29298-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29298-123">Remarks</span></span>

<span data-ttu-id="29298-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="29298-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="29298-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="29298-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="29298-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="29298-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="29298-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="29298-127">Schema Name</span></span>  <br/> |<span data-ttu-id="29298-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="29298-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="29298-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="29298-129">Validation File</span></span>  <br/> |<span data-ttu-id="29298-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="29298-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="29298-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="29298-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="29298-132">False</span><span class="sxs-lookup"><span data-stu-id="29298-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="29298-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29298-133">See also</span></span>

- [<span data-ttu-id="29298-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="29298-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

