---
title: Regel (RuleType)
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
ms.assetid: 259a1f62-b235-4964-88bf-2d1f1c05a563
description: Das Rule-Element enthält eine einzelne Regel und stellt eine Regel im Postfach eines Benutzers dar.
ms.openlocfilehash: cdbd21df235a62a9e201e1eaae1d82a8ac10cdd2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465079"
---
# <a name="rule-ruletype"></a><span data-ttu-id="890e2-103">Regel (RuleType)</span><span class="sxs-lookup"><span data-stu-id="890e2-103">Rule (RuleType)</span></span>

<span data-ttu-id="890e2-104">Das **rule** -Element enthält eine einzelne Regel und stellt eine Regel im Postfach eines Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="890e2-104">The **Rule** element contains a single rule and represents a rule in a user's mailbox.</span></span> 
  
```XML
<Rule>
    <RuleId>
    <DisplayName>
    <Priority>
    <IsEnabled>
    <IsNotSupported>
    <IsInError>
    <Conditions>
    <Exceptions>
    <Actions>
</Rule>
```

 <span data-ttu-id="890e2-105">**RuleType**</span><span class="sxs-lookup"><span data-stu-id="890e2-105">**RuleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="890e2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="890e2-106">Attributes and elements</span></span>

<span data-ttu-id="890e2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="890e2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="890e2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="890e2-108">Attributes</span></span>

<span data-ttu-id="890e2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="890e2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="890e2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="890e2-110">Child elements</span></span>

|<span data-ttu-id="890e2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="890e2-111">**Element**</span></span>|<span data-ttu-id="890e2-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="890e2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="890e2-113">RuleId</span><span class="sxs-lookup"><span data-stu-id="890e2-113">RuleId</span></span>](ruleid.md) <br/> |<span data-ttu-id="890e2-114">Gibt die Regel-ID an.</span><span class="sxs-lookup"><span data-stu-id="890e2-114">Specifies the rule identifier.</span></span>  <br/> |
|[<span data-ttu-id="890e2-115">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="890e2-115">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="890e2-116">Enthält den Anzeigenamen einer Regel.</span><span class="sxs-lookup"><span data-stu-id="890e2-116">Contains the display name of a rule.</span></span>  <br/> |
|[<span data-ttu-id="890e2-117">Priority</span><span class="sxs-lookup"><span data-stu-id="890e2-117">Priority</span></span>](priority.md) <br/> |<span data-ttu-id="890e2-118">Gibt die Reihenfolge an, in der eine Regel ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="890e2-118">Indicates the order in which a rule is to be run.</span></span>  <br/> |
|[<span data-ttu-id="890e2-119">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="890e2-119">IsEnabled</span></span>](isenabled.md) <br/> |<span data-ttu-id="890e2-120">Gibt an, ob die Regel aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="890e2-120">Indicates whether the rule is enabled.</span></span>  <br/> |
|[<span data-ttu-id="890e2-121">IsNotSupported</span><span class="sxs-lookup"><span data-stu-id="890e2-121">IsNotSupported</span></span>](isnotsupported.md) <br/> |<span data-ttu-id="890e2-122">Gibt an, ob die Regel mit den APIs für verwalteten Code nicht geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="890e2-122">Indicates whether the rule cannot be modified with the managed code APIs.</span></span>  <br/> |
|[<span data-ttu-id="890e2-123">IsInError</span><span class="sxs-lookup"><span data-stu-id="890e2-123">IsInError</span></span>](isinerror.md) <br/> |<span data-ttu-id="890e2-124">Gibt an, ob sich die Regel in einem Fehlerzustand befindet.</span><span class="sxs-lookup"><span data-stu-id="890e2-124">Indicates whether the rule is in an error condition.</span></span>  <br/> |
|[<span data-ttu-id="890e2-125">Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="890e2-125">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="890e2-126">Gibt die Bedingungen an, die bei der Erfüllung der Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="890e2-126">Identifies the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="890e2-127">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="890e2-127">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="890e2-128">Identifiziert die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für die Posteingangsregel darstellen.</span><span class="sxs-lookup"><span data-stu-id="890e2-128">Identifies the exceptions that represent all the available rule exception conditions for the inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="890e2-129">Aktionen</span><span class="sxs-lookup"><span data-stu-id="890e2-129">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="890e2-130">Stellt die Aktionen dar, die für eine Nachricht ausgeführt werden sollen, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="890e2-130">Represents the actions to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="890e2-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="890e2-131">Parent elements</span></span>

|<span data-ttu-id="890e2-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="890e2-132">**Element**</span></span>|<span data-ttu-id="890e2-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="890e2-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="890e2-134">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="890e2-134">CreateRuleOperation</span></span>](createruleoperation.md) <br/> |<span data-ttu-id="890e2-135">Stellt einen Vorgang zum Erstellen einer neuen Regel dar.</span><span class="sxs-lookup"><span data-stu-id="890e2-135">Represents an operation to create a new rule.</span></span>  <br/> |
|[<span data-ttu-id="890e2-136">InboxRules</span><span class="sxs-lookup"><span data-stu-id="890e2-136">InboxRules</span></span>](inboxrules.md) <br/> |<span data-ttu-id="890e2-137">Stellt ein Array von Regeln im Postfach des Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="890e2-137">Represents an array of rules in the user's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="890e2-138">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="890e2-138">SetRuleOperation</span></span>](setruleoperation.md) <br/> |<span data-ttu-id="890e2-139">Stellt einen Vorgang zum Aktualisieren einer vorhandenen Regel dar.</span><span class="sxs-lookup"><span data-stu-id="890e2-139">Represents an operation to update an existing rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="890e2-140">Textwert</span><span class="sxs-lookup"><span data-stu-id="890e2-140">Text value</span></span>

<span data-ttu-id="890e2-141">Keine.</span><span class="sxs-lookup"><span data-stu-id="890e2-141">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="890e2-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="890e2-142">Remarks</span></span>

<span data-ttu-id="890e2-143">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="890e2-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="890e2-144">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="890e2-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="890e2-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="890e2-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="890e2-146">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="890e2-146">Schema Name</span></span>  <br/> |<span data-ttu-id="890e2-147">Schematypen</span><span class="sxs-lookup"><span data-stu-id="890e2-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="890e2-148">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="890e2-148">Validation File</span></span>  <br/> |<span data-ttu-id="890e2-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="890e2-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="890e2-150">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="890e2-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="890e2-151">True</span><span class="sxs-lookup"><span data-stu-id="890e2-151">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="890e2-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="890e2-152">See also</span></span>



[<span data-ttu-id="890e2-153">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="890e2-153">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="890e2-154">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="890e2-154">SetRuleOperation</span></span>](setruleoperation.md)
  
[<span data-ttu-id="890e2-155">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="890e2-155">CreateRuleOperation</span></span>](createruleoperation.md)


- [<span data-ttu-id="890e2-156">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="890e2-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

