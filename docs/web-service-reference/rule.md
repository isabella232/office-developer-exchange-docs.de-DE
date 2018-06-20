---
title: Regel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Rule
api_type:
- schema
ms.assetid: c30f3851-bd56-4473-9106-dc85e9619486
description: Rule-Element enthält eine einzelne Schutzregel.
ms.openlocfilehash: 9abbb70381c214211172d2d5ba1ed43ee4797f17
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831263"
---
# <a name="rule"></a><span data-ttu-id="fec8b-103">Regel</span><span class="sxs-lookup"><span data-stu-id="fec8b-103">Rule</span></span>

<span data-ttu-id="fec8b-104">**Rule** -Element enthält eine einzelne Schutzregel.</span><span class="sxs-lookup"><span data-stu-id="fec8b-104">The **Rule** element contains a single protection rule.</span></span> 
  
```XML
<Rule Name="" UserOverridable=="" Priority="">
   <Condition/>
   <Action/>
</Rule>
```

 <span data-ttu-id="fec8b-105">**ProtectionRuleType**</span><span class="sxs-lookup"><span data-stu-id="fec8b-105">**ProtectionRuleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fec8b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fec8b-106">Attributes and elements</span></span>

<span data-ttu-id="fec8b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fec8b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fec8b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fec8b-108">Attributes</span></span>

|<span data-ttu-id="fec8b-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fec8b-109">**Attribute**</span></span>|<span data-ttu-id="fec8b-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fec8b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fec8b-111">**Name**</span><span class="sxs-lookup"><span data-stu-id="fec8b-111">**Name**</span></span> <br/> |<span data-ttu-id="fec8b-112">Gibt den Namen der Regel.</span><span class="sxs-lookup"><span data-stu-id="fec8b-112">Identifies the name of the rule.</span></span> <span data-ttu-id="fec8b-113">Ein erforderliches Attribut vom Typ String mit einer Mindestlänge 1.</span><span class="sxs-lookup"><span data-stu-id="fec8b-113">A required attribute of type string with a minimum length of 1.</span></span>  <br/> |
|<span data-ttu-id="fec8b-114">**UserOverridable**</span><span class="sxs-lookup"><span data-stu-id="fec8b-114">**UserOverridable**</span></span> <br/> |<span data-ttu-id="fec8b-115">Gibt an, ob die Regel zwingend erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="fec8b-115">Specifies whether the rule is mandatory.</span></span> <span data-ttu-id="fec8b-116">Wenn die Regel zwingend erforderlich ist, muss der Wert dieses Attributs **false**sein.</span><span class="sxs-lookup"><span data-stu-id="fec8b-116">If the rule is mandatory, this attribute value must be **false**.</span></span> <span data-ttu-id="fec8b-117">Ein erforderliches Attribut vom Typ Boolean.</span><span class="sxs-lookup"><span data-stu-id="fec8b-117">A required attribute of type Boolean.</span></span>  <br/> |
|<span data-ttu-id="fec8b-118">**Priority**</span><span class="sxs-lookup"><span data-stu-id="fec8b-118">**Priority**</span></span> <br/> |<span data-ttu-id="fec8b-119">Gibt die Priorität der Regel an.</span><span class="sxs-lookup"><span data-stu-id="fec8b-119">Specifies the rule priority.</span></span> <span data-ttu-id="fec8b-120">Ein erforderliches Attribut vom Typ Int mit minimalen Wert 1.</span><span class="sxs-lookup"><span data-stu-id="fec8b-120">A required attribute of type int with a minimum value of 1.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fec8b-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fec8b-121">Child elements</span></span>

|<span data-ttu-id="fec8b-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="fec8b-122">**Element**</span></span>|<span data-ttu-id="fec8b-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fec8b-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fec8b-124">Bedingung</span><span class="sxs-lookup"><span data-stu-id="fec8b-124">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="fec8b-125">Gibt die Bedingung, die erfüllt sein muss, für die Aktionsteil der Regel ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fec8b-125">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="fec8b-126">Aktion (ProtectionRuleActionType)</span><span class="sxs-lookup"><span data-stu-id="fec8b-126">Action (ProtectionRuleActionType)</span></span>](action-protectionruleactiontype.md) <br/> |<span data-ttu-id="fec8b-127">Gibt an, welche Aktion ausgeführt werden muss, wenn der Bedingungsteil der Regel übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="fec8b-127">Identifies what action must be executed if the condition part of the rule matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fec8b-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fec8b-128">Parent elements</span></span>

|<span data-ttu-id="fec8b-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="fec8b-129">**Element**</span></span>|<span data-ttu-id="fec8b-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fec8b-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fec8b-131">Regeln</span><span class="sxs-lookup"><span data-stu-id="fec8b-131">Rules </span></span>](rules-ex15websvcsotherref.md) <br/> |<span data-ttu-id="fec8b-132">Enthält ein Array von Regeln für den Schutz.</span><span class="sxs-lookup"><span data-stu-id="fec8b-132">Contains an array of protection rules.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fec8b-133">Textwert</span><span class="sxs-lookup"><span data-stu-id="fec8b-133">Text value</span></span>

<span data-ttu-id="fec8b-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="fec8b-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fec8b-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fec8b-135">Remarks</span></span>

<span data-ttu-id="fec8b-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fec8b-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fec8b-137">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="fec8b-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fec8b-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="fec8b-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fec8b-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fec8b-139">Schema Name</span></span>  <br/> |<span data-ttu-id="fec8b-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="fec8b-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="fec8b-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fec8b-141">Validation File</span></span>  <br/> |<span data-ttu-id="fec8b-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fec8b-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fec8b-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fec8b-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="fec8b-144">False</span><span class="sxs-lookup"><span data-stu-id="fec8b-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fec8b-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fec8b-145">See also</span></span>



- [<span data-ttu-id="fec8b-146">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fec8b-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

