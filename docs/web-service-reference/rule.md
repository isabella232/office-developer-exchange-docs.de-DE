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
description: Das Rule-Element enthält eine einzelne Schutz Regel.
ms.openlocfilehash: 6c18a2bd026893cd333bc7007203abf04a6f0be7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465001"
---
# <a name="rule"></a><span data-ttu-id="05280-103">Regel</span><span class="sxs-lookup"><span data-stu-id="05280-103">Rule</span></span>

<span data-ttu-id="05280-104">Das **rule** -Element enthält eine einzelne Schutz Regel.</span><span class="sxs-lookup"><span data-stu-id="05280-104">The **Rule** element contains a single protection rule.</span></span> 
  
```XML
<Rule Name="" UserOverridable=="" Priority="">
   <Condition/>
   <Action/>
</Rule>
```

 <span data-ttu-id="05280-105">**ProtectionRuleType**</span><span class="sxs-lookup"><span data-stu-id="05280-105">**ProtectionRuleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="05280-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="05280-106">Attributes and elements</span></span>

<span data-ttu-id="05280-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="05280-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="05280-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="05280-108">Attributes</span></span>

|<span data-ttu-id="05280-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="05280-109">**Attribute**</span></span>|<span data-ttu-id="05280-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="05280-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="05280-111">**Name**</span><span class="sxs-lookup"><span data-stu-id="05280-111">**Name**</span></span> <br/> |<span data-ttu-id="05280-112">Gibt den Namen der Regel an.</span><span class="sxs-lookup"><span data-stu-id="05280-112">Identifies the name of the rule.</span></span> <span data-ttu-id="05280-113">Ein erforderliches Attribut vom Typ String mit einer minimalen Länge von 1.</span><span class="sxs-lookup"><span data-stu-id="05280-113">A required attribute of type string with a minimum length of 1.</span></span>  <br/> |
|<span data-ttu-id="05280-114">**UserOverridable**</span><span class="sxs-lookup"><span data-stu-id="05280-114">**UserOverridable**</span></span> <br/> |<span data-ttu-id="05280-115">Gibt an, ob die Regel obligatorisch ist.</span><span class="sxs-lookup"><span data-stu-id="05280-115">Specifies whether the rule is mandatory.</span></span> <span data-ttu-id="05280-116">Wenn die Regel obligatorisch ist, muss dieser Attributwert auf **false festgelegt**sein.</span><span class="sxs-lookup"><span data-stu-id="05280-116">If the rule is mandatory, this attribute value must be **false**.</span></span> <span data-ttu-id="05280-117">Ein erforderliches Attribut vom Typ Boolean.</span><span class="sxs-lookup"><span data-stu-id="05280-117">A required attribute of type Boolean.</span></span>  <br/> |
|<span data-ttu-id="05280-118">**Priority**</span><span class="sxs-lookup"><span data-stu-id="05280-118">**Priority**</span></span> <br/> |<span data-ttu-id="05280-119">Gibt die Regelpriorität an.</span><span class="sxs-lookup"><span data-stu-id="05280-119">Specifies the rule priority.</span></span> <span data-ttu-id="05280-120">Ein erforderliches Attribut vom Typ int mit einem Minimalwert von 1.</span><span class="sxs-lookup"><span data-stu-id="05280-120">A required attribute of type int with a minimum value of 1.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="05280-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="05280-121">Child elements</span></span>

|<span data-ttu-id="05280-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="05280-122">**Element**</span></span>|<span data-ttu-id="05280-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="05280-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05280-124">Bedingung</span><span class="sxs-lookup"><span data-stu-id="05280-124">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="05280-125">Gibt die Bedingung an, die erfüllt sein muss, damit der Aktions Teil der Regel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05280-125">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="05280-126">Action (ProtectionRuleActionType)</span><span class="sxs-lookup"><span data-stu-id="05280-126">Action (ProtectionRuleActionType)</span></span>](action-protectionruleactiontype.md) <br/> |<span data-ttu-id="05280-127">Gibt an, welche Aktion ausgeführt werden muss, wenn der Bedingungsteil der Regel übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="05280-127">Identifies what action must be executed if the condition part of the rule matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="05280-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="05280-128">Parent elements</span></span>

|<span data-ttu-id="05280-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="05280-129">**Element**</span></span>|<span data-ttu-id="05280-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="05280-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05280-131">Regeln</span><span class="sxs-lookup"><span data-stu-id="05280-131">Rules </span></span>](rules-ex15websvcsotherref.md) <br/> |<span data-ttu-id="05280-132">Enthält ein Array von Schutzregeln.</span><span class="sxs-lookup"><span data-stu-id="05280-132">Contains an array of protection rules.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="05280-133">Textwert</span><span class="sxs-lookup"><span data-stu-id="05280-133">Text value</span></span>

<span data-ttu-id="05280-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="05280-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="05280-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05280-135">Remarks</span></span>

<span data-ttu-id="05280-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="05280-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05280-137">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="05280-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05280-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="05280-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="05280-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="05280-139">Schema Name</span></span>  <br/> |<span data-ttu-id="05280-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="05280-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="05280-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="05280-141">Validation File</span></span>  <br/> |<span data-ttu-id="05280-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="05280-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="05280-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="05280-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="05280-144">False</span><span class="sxs-lookup"><span data-stu-id="05280-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05280-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05280-145">See also</span></span>



- [<span data-ttu-id="05280-146">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="05280-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

