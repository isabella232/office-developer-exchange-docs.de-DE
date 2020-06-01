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
description: Das and-Element gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, damit Sie zu true ausgewertet werden.
ms.openlocfilehash: ba898ccd77518971afaf713d1c7c7955f46465d5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464735"
---
# <a name="and-protectionruleandtype"></a><span data-ttu-id="7fc1e-103">Und (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="7fc1e-103">And (ProtectionRuleAndType)</span></span>

<span data-ttu-id="7fc1e-104">Das **and-** Element gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, damit Sie zu **true**ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="7fc1e-104">The **And** element specifies that all child elements must match to evaluate to **true**.</span></span>
  
```xml
<And>
   <AllInternal/>
   <And/>
   <RecipientIs/>
   <SenderDepartments/>
   <True/>
</And>
```

 <span data-ttu-id="7fc1e-105">**ProtectionRuleAndType**</span><span class="sxs-lookup"><span data-stu-id="7fc1e-105">**ProtectionRuleAndType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7fc1e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7fc1e-106">Attributes and elements</span></span>

<span data-ttu-id="7fc1e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7fc1e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7fc1e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7fc1e-108">Attributes</span></span>

<span data-ttu-id="7fc1e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7fc1e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7fc1e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7fc1e-110">Child elements</span></span>

|<span data-ttu-id="7fc1e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7fc1e-111">**Element**</span></span>|<span data-ttu-id="7fc1e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7fc1e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fc1e-113">AllInternal</span><span class="sxs-lookup"><span data-stu-id="7fc1e-113">AllInternal</span></span>](allinternal.md) <br/> |<span data-ttu-id="7fc1e-114">Ergibt **true** , wenn alle Empfänger einer e-Mail-Nachricht für die Organisation des Absenders intern sind.</span><span class="sxs-lookup"><span data-stu-id="7fc1e-114">Evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span>  <br/> |
|<span data-ttu-id="7fc1e-115">**Und**</span><span class="sxs-lookup"><span data-stu-id="7fc1e-115">**And**</span></span> <br/> |<span data-ttu-id="7fc1e-116">Gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, damit Sie zu **true**ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="7fc1e-116">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
|[<span data-ttu-id="7fc1e-117">Empfängerist</span><span class="sxs-lookup"><span data-stu-id="7fc1e-117">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="7fc1e-118">Gibt an, dass jeder Empfänger der e-Mail-Nachricht mit einem der angegebenen Empfänger in den untergeordneten [Wert (ProtectionRuleValueType)](value-protectionrulevaluetype.md) -Elementen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="7fc1e-118">Specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="7fc1e-119">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="7fc1e-119">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="7fc1e-120">Gibt an, dass die Abteilung des Absenders mit einer der angegebenen Abteilungen in den untergeordneten [Wertelementen (ProtectionRuleValueType)](value-protectionrulevaluetype.md) übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="7fc1e-120">Specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="7fc1e-121">True</span><span class="sxs-lookup"><span data-stu-id="7fc1e-121">True</span></span>](true.md) <br/> |<span data-ttu-id="7fc1e-122">Gibt eine Bedingung an, die immer übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="7fc1e-122">Specifies a condition that always matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7fc1e-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7fc1e-123">Parent elements</span></span>

|<span data-ttu-id="7fc1e-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="7fc1e-124">**Element**</span></span>|<span data-ttu-id="7fc1e-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7fc1e-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fc1e-126">Bedingung</span><span class="sxs-lookup"><span data-stu-id="7fc1e-126">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="7fc1e-127">Gibt die Bedingung an, die erfüllt sein muss, damit der Aktions Teil der Regel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7fc1e-127">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|<span data-ttu-id="7fc1e-128">**Und**</span><span class="sxs-lookup"><span data-stu-id="7fc1e-128">**And**</span></span> <br/> |<span data-ttu-id="7fc1e-129">Gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, damit Sie zu **true**ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="7fc1e-129">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7fc1e-130">Textwert</span><span class="sxs-lookup"><span data-stu-id="7fc1e-130">Text value</span></span>

<span data-ttu-id="7fc1e-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="7fc1e-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7fc1e-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7fc1e-132">Remarks</span></span>

<span data-ttu-id="7fc1e-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7fc1e-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7fc1e-134">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7fc1e-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fc1e-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="7fc1e-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7fc1e-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7fc1e-136">Schema Name</span></span>  <br/> |<span data-ttu-id="7fc1e-137">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7fc1e-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="7fc1e-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7fc1e-138">Validation File</span></span>  <br/> |<span data-ttu-id="7fc1e-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7fc1e-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7fc1e-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7fc1e-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="7fc1e-141">False</span><span class="sxs-lookup"><span data-stu-id="7fc1e-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7fc1e-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fc1e-142">See also</span></span>

- [<span data-ttu-id="7fc1e-143">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7fc1e-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

