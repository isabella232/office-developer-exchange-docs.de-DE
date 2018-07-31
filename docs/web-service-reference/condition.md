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
description: Das Condition-Element identifiziert die Bedingung, die erfüllt sein muss, für die Aktionsteil der Regel ausgeführt werden.
ms.openlocfilehash: d49f2984799b15c0499af59abecbb34abe15f7c3
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353560"
---
# <a name="condition"></a><span data-ttu-id="94787-103">Bedingung</span><span class="sxs-lookup"><span data-stu-id="94787-103">Condition</span></span>

<span data-ttu-id="94787-104">Das **Condition** -Element identifiziert die Bedingung, die erfüllt sein muss, für die Aktionsteil der Regel ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="94787-104">The **Condition** element identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span> 
  
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

<span data-ttu-id="94787-105">**ProtectionRuleConditionType**</span><span class="sxs-lookup"><span data-stu-id="94787-105">**ProtectionRuleConditionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="94787-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="94787-106">Attributes and elements</span></span>

<span data-ttu-id="94787-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="94787-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="94787-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="94787-108">Attributes</span></span>

<span data-ttu-id="94787-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="94787-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="94787-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="94787-110">Child elements</span></span>

|<span data-ttu-id="94787-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="94787-111">**Element**</span></span>|<span data-ttu-id="94787-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="94787-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="94787-113">AllInternal</span><span class="sxs-lookup"><span data-stu-id="94787-113">AllInternal</span></span>](allinternal.md) <br/> |<span data-ttu-id="94787-114">Ergibt **true** , wenn alle Empfänger einer e-Mail-Nachricht für die Organisation des Absenders intern sind.</span><span class="sxs-lookup"><span data-stu-id="94787-114">Evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span>  <br/> |
|[<span data-ttu-id="94787-115">Und (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="94787-115">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="94787-116">Gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, damit zu **true**ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="94787-116">Specifies that all child elements must match to evaluate to **true**.</span></span> <span data-ttu-id="94787-117">Gibt an, dass mehr als ein Protection untergeordneten regelbedingung sein muss.</span><span class="sxs-lookup"><span data-stu-id="94787-117">Specifies that there must be more than one protection rule child condition.</span></span>  <br/> |
|[<span data-ttu-id="94787-118">RecipientIs</span><span class="sxs-lookup"><span data-stu-id="94787-118">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="94787-119">Gibt an, dass alle Empfänger der E-mail-Nachricht mit der angegebenen Empfänger im untergeordneten [Wert (ProtectionRuleValueType)](value-protectionrulevaluetype.md) entspricht.</span><span class="sxs-lookup"><span data-stu-id="94787-119">Specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="94787-120">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="94787-120">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="94787-121">Gibt an, dass die Abteilung des Absenders einer der angegebenen Abteilungen im untergeordneten [Wert (ProtectionRuleValueType)](value-protectionrulevaluetype.md) übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="94787-121">Specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="94787-122">True</span><span class="sxs-lookup"><span data-stu-id="94787-122">True</span></span>](true.md) <br/> |<span data-ttu-id="94787-123">Gibt eine Bedingung, die immer entspricht.</span><span class="sxs-lookup"><span data-stu-id="94787-123">Specifies a condition that always matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="94787-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="94787-124">Parent elements</span></span>

|<span data-ttu-id="94787-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="94787-125">**Element**</span></span>|<span data-ttu-id="94787-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="94787-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="94787-127">Rule</span><span class="sxs-lookup"><span data-stu-id="94787-127">Rule</span></span>](rule.md) <br/> |<span data-ttu-id="94787-128">Enthält eine einzelne Schutzregel.</span><span class="sxs-lookup"><span data-stu-id="94787-128">Contains a single protection rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="94787-129">Textwert</span><span class="sxs-lookup"><span data-stu-id="94787-129">Text value</span></span>

<span data-ttu-id="94787-130">Keine.</span><span class="sxs-lookup"><span data-stu-id="94787-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94787-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="94787-131">Remarks</span></span>

<span data-ttu-id="94787-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="94787-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="94787-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="94787-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94787-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="94787-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="94787-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="94787-135">Schema Name</span></span>  <br/> |<span data-ttu-id="94787-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="94787-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="94787-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="94787-137">Validation File</span></span>  <br/> |<span data-ttu-id="94787-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="94787-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="94787-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="94787-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="94787-140">False</span><span class="sxs-lookup"><span data-stu-id="94787-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="94787-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94787-141">See also</span></span>

- [<span data-ttu-id="94787-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="94787-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

