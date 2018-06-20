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
description: Das Argument-Element gibt die Argumente für die Aktion an.
ms.openlocfilehash: ed4e46a8d9897516e9c96bf3930f7d488bc06714
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757380"
---
# <a name="argument"></a><span data-ttu-id="59839-103">Argument</span><span class="sxs-lookup"><span data-stu-id="59839-103">Argument</span></span>

<span data-ttu-id="59839-104">Das **Argument** -Element gibt die Argumente für die Aktion an.</span><span class="sxs-lookup"><span data-stu-id="59839-104">The **Argument** element specifies arguments to the action.</span></span> 
  
```xml
<Argument Value=""/>
```

 <span data-ttu-id="59839-105">**ProtectionRuleArgumentType**</span><span class="sxs-lookup"><span data-stu-id="59839-105">**ProtectionRuleArgumentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="59839-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="59839-106">Attributes and elements</span></span>

<span data-ttu-id="59839-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="59839-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="59839-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="59839-108">Attributes</span></span>

|<span data-ttu-id="59839-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="59839-109">**Attribute**</span></span>|<span data-ttu-id="59839-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="59839-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="59839-111">**Value**</span><span class="sxs-lookup"><span data-stu-id="59839-111">**Value**</span></span> <br/> |<span data-ttu-id="59839-112">Ein nicht leeren Zeichenfolgenwert, der den Wert eines Arguments der Aktionsteil einer Schutzregel darstellt.</span><span class="sxs-lookup"><span data-stu-id="59839-112">A non-empty string value that represents the value of an argument to the action part of a protection rule.</span></span> <span data-ttu-id="59839-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="59839-113">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="59839-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="59839-114">Child elements</span></span>

<span data-ttu-id="59839-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="59839-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="59839-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="59839-116">Parent elements</span></span>

|<span data-ttu-id="59839-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="59839-117">**Element**</span></span>|<span data-ttu-id="59839-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="59839-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59839-119">Aktion (ProtectionRuleActionType)</span><span class="sxs-lookup"><span data-stu-id="59839-119">Action (ProtectionRuleActionType)</span></span>](action-protectionruleactiontype.md) <br/> |<span data-ttu-id="59839-120">Gibt an, welche Aktion ausgeführt werden muss, wenn der Bedingungsteil der Regel übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="59839-120">Identifies what action must be executed if the condition part of the rule matches.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="59839-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="59839-121">Text value</span></span>

<span data-ttu-id="59839-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="59839-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="59839-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="59839-123">Remarks</span></span>

<span data-ttu-id="59839-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="59839-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="59839-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="59839-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59839-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="59839-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="59839-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="59839-127">Schema Name</span></span>  <br/> |<span data-ttu-id="59839-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="59839-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="59839-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="59839-129">Validation File</span></span>  <br/> |<span data-ttu-id="59839-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="59839-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="59839-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="59839-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="59839-132">False</span><span class="sxs-lookup"><span data-stu-id="59839-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="59839-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59839-133">See also</span></span>

- [<span data-ttu-id="59839-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="59839-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

