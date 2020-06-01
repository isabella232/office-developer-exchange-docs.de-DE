---
title: Bedingung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Condition
api_type:
- schema
ms.assetid: 0790a3f2-cb31-4036-a757-7821aa0722cb
description: Das Condition-Element gibt die Bedingung an, die erfüllt sein muss, damit der Aktions Teil der Regel ausgeführt wird.
ms.openlocfilehash: 2aea11197f072a4dbe21292bb47075d6f273d31b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463223"
---
# <a name="condition"></a><span data-ttu-id="be4fc-103">Bedingung</span><span class="sxs-lookup"><span data-stu-id="be4fc-103">Condition</span></span>

<span data-ttu-id="be4fc-104">Das **Condition** -Element gibt die Bedingung an, die erfüllt sein muss, damit der Aktions Teil der Regel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be4fc-104">The **Condition** element identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span> 
  
```xml
<Condition>
   <AllInternal/>
</Condition>
```

```xml
<Condition> 
    <SenderDepartments/> 
</Condition>
```

```xml
<Condition> 
    <True/> 
</Condition>
```

```xml
<Condition> 
    <Recipients/> 
</Condition>
```

```xml
<Condition> 
    <And/> 
</Condition>
```

<span data-ttu-id="be4fc-105">**ProtectionRuleConditionType**</span><span class="sxs-lookup"><span data-stu-id="be4fc-105">**ProtectionRuleConditionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="be4fc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="be4fc-106">Attributes and elements</span></span>

<span data-ttu-id="be4fc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="be4fc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="be4fc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="be4fc-108">Attributes</span></span>

<span data-ttu-id="be4fc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="be4fc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="be4fc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="be4fc-110">Child elements</span></span>

|<span data-ttu-id="be4fc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="be4fc-111">**Element**</span></span>|<span data-ttu-id="be4fc-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="be4fc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be4fc-113">AllInternal</span><span class="sxs-lookup"><span data-stu-id="be4fc-113">AllInternal</span></span>](allinternal.md) <br/> |<span data-ttu-id="be4fc-114">Ergibt **true** , wenn alle Empfänger einer e-Mail-Nachricht für die Organisation des Absenders intern sind.</span><span class="sxs-lookup"><span data-stu-id="be4fc-114">Evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span>  <br/> |
|[<span data-ttu-id="be4fc-115">Und (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="be4fc-115">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="be4fc-116">Gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, damit Sie zu **true**ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="be4fc-116">Specifies that all child elements must match to evaluate to **true**.</span></span> <span data-ttu-id="be4fc-117">Gibt an, dass mehr als eine untergeordnete Schutz Regelbedingung vorhanden sein muss.</span><span class="sxs-lookup"><span data-stu-id="be4fc-117">Specifies that there must be more than one protection rule child condition.</span></span>  <br/> |
|[<span data-ttu-id="be4fc-118">Empfängerist</span><span class="sxs-lookup"><span data-stu-id="be4fc-118">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="be4fc-119">Gibt an, dass jeder Empfänger der e-Mail-Nachricht mit einem der angegebenen Empfänger in den untergeordneten [Wert (ProtectionRuleValueType)](value-protectionrulevaluetype.md) -Elementen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="be4fc-119">Specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="be4fc-120">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="be4fc-120">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="be4fc-121">Gibt an, dass die Abteilung des Absenders mit einer der angegebenen Abteilungen in den untergeordneten [Wertelementen (ProtectionRuleValueType)](value-protectionrulevaluetype.md) übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="be4fc-121">Specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="be4fc-122">True</span><span class="sxs-lookup"><span data-stu-id="be4fc-122">True</span></span>](true.md) <br/> |<span data-ttu-id="be4fc-123">Gibt eine Bedingung an, die immer übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="be4fc-123">Specifies a condition that always matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="be4fc-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="be4fc-124">Parent elements</span></span>

|<span data-ttu-id="be4fc-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="be4fc-125">**Element**</span></span>|<span data-ttu-id="be4fc-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="be4fc-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be4fc-127">Rule</span><span class="sxs-lookup"><span data-stu-id="be4fc-127">Rule</span></span>](rule.md) <br/> |<span data-ttu-id="be4fc-128">Enthält eine einzelne Schutz Regel.</span><span class="sxs-lookup"><span data-stu-id="be4fc-128">Contains a single protection rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="be4fc-129">Textwert</span><span class="sxs-lookup"><span data-stu-id="be4fc-129">Text value</span></span>

<span data-ttu-id="be4fc-130">Keine.</span><span class="sxs-lookup"><span data-stu-id="be4fc-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="be4fc-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be4fc-131">Remarks</span></span>

<span data-ttu-id="be4fc-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="be4fc-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="be4fc-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="be4fc-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be4fc-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="be4fc-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="be4fc-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="be4fc-135">Schema Name</span></span>  <br/> |<span data-ttu-id="be4fc-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="be4fc-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="be4fc-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="be4fc-137">Validation File</span></span>  <br/> |<span data-ttu-id="be4fc-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="be4fc-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="be4fc-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="be4fc-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="be4fc-140">False</span><span class="sxs-lookup"><span data-stu-id="be4fc-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="be4fc-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be4fc-141">See also</span></span>

- [<span data-ttu-id="be4fc-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="be4fc-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

