---
title: Und (ProtectionRuleAndType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- And
api_type:
- schema
ms.assetid: 7fafd1c8-cd29-43a0-b383-f6595f934f48
description: Das Element und gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, damit zu True ausgewertet werden.
ms.openlocfilehash: 9e0128ee3fa2b6ffdc5975946694475afec53c25
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757263"
---
# <a name="and-protectionruleandtype"></a><span data-ttu-id="e3129-103">Und (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="e3129-103">And (ProtectionRuleAndType)</span></span>

<span data-ttu-id="e3129-104">Das Element **und** gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, damit zu **true**ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="e3129-104">The **And** element specifies that all child elements must match to evaluate to **true**.</span></span>
  
```xml
<And>
   <AllInternal/>
   <And/>
   <RecipientIs/>
   <SenderDepartments/>
   <True/>
</And>
```

 <span data-ttu-id="e3129-105">**ProtectionRuleAndType**</span><span class="sxs-lookup"><span data-stu-id="e3129-105">**ProtectionRuleAndType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e3129-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e3129-106">Attributes and elements</span></span>

<span data-ttu-id="e3129-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e3129-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3129-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e3129-108">Attributes</span></span>

<span data-ttu-id="e3129-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e3129-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e3129-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e3129-110">Child elements</span></span>

|<span data-ttu-id="e3129-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e3129-111">**Element**</span></span>|<span data-ttu-id="e3129-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e3129-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3129-113">AllInternal</span><span class="sxs-lookup"><span data-stu-id="e3129-113">AllInternal</span></span>](allinternal.md) <br/> |<span data-ttu-id="e3129-114">Ergibt **true** , wenn alle Empfänger einer e-Mail-Nachricht für die Organisation des Absenders intern sind.</span><span class="sxs-lookup"><span data-stu-id="e3129-114">Evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span>  <br/> |
|<span data-ttu-id="e3129-115">**Und**</span><span class="sxs-lookup"><span data-stu-id="e3129-115">**And**</span></span> <br/> |<span data-ttu-id="e3129-116">Gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, damit zu **true**ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="e3129-116">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
|[<span data-ttu-id="e3129-117">RecipientIs</span><span class="sxs-lookup"><span data-stu-id="e3129-117">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="e3129-118">Gibt an, dass alle Empfänger der E-mail-Nachricht mit der angegebenen Empfänger im untergeordneten [Wert (ProtectionRuleValueType)](value-protectionrulevaluetype.md) entspricht.</span><span class="sxs-lookup"><span data-stu-id="e3129-118">Specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="e3129-119">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="e3129-119">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="e3129-120">Gibt an, dass die Abteilung des Absenders einer der angegebenen Abteilungen im untergeordneten [Wert (ProtectionRuleValueType)](value-protectionrulevaluetype.md) übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="e3129-120">Specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="e3129-121">True</span><span class="sxs-lookup"><span data-stu-id="e3129-121">True</span></span>](true.md) <br/> |<span data-ttu-id="e3129-122">Gibt eine Bedingung, die immer entspricht.</span><span class="sxs-lookup"><span data-stu-id="e3129-122">Specifies a condition that always matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e3129-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e3129-123">Parent elements</span></span>

|<span data-ttu-id="e3129-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="e3129-124">**Element**</span></span>|<span data-ttu-id="e3129-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e3129-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3129-126">Bedingung</span><span class="sxs-lookup"><span data-stu-id="e3129-126">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="e3129-127">Gibt die Bedingung, die erfüllt sein muss, für die Aktionsteil der Regel ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e3129-127">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|<span data-ttu-id="e3129-128">**Und**</span><span class="sxs-lookup"><span data-stu-id="e3129-128">**And**</span></span> <br/> |<span data-ttu-id="e3129-129">Gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, damit zu **true**ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="e3129-129">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e3129-130">Textwert</span><span class="sxs-lookup"><span data-stu-id="e3129-130">Text value</span></span>

<span data-ttu-id="e3129-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="e3129-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e3129-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e3129-132">Remarks</span></span>

<span data-ttu-id="e3129-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e3129-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e3129-134">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e3129-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3129-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="e3129-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e3129-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e3129-136">Schema Name</span></span>  <br/> |<span data-ttu-id="e3129-137">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e3129-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="e3129-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e3129-138">Validation File</span></span>  <br/> |<span data-ttu-id="e3129-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e3129-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e3129-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e3129-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="e3129-141">False</span><span class="sxs-lookup"><span data-stu-id="e3129-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3129-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3129-142">See also</span></span>

- [<span data-ttu-id="e3129-143">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e3129-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

