---
title: CreateRuleOperation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateRuleOperation
api_type:
- schema
ms.assetid: e9f70726-db08-4089-839e-a41007d0a473
description: Das CreateRuleOperation-Element stellt einen Vorgang zum Erstellen einer neuen Posteingangsregel an.
ms.openlocfilehash: c531f222ffe886e6ef53a99609cfa27e84fd6107
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757796"
---
# <a name="createruleoperation"></a><span data-ttu-id="52b01-103">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="52b01-103">CreateRuleOperation</span></span>

<span data-ttu-id="52b01-104">Das **CreateRuleOperation** -Element stellt einen Vorgang zum Erstellen einer neuen Posteingangsregel an.</span><span class="sxs-lookup"><span data-stu-id="52b01-104">The **CreateRuleOperation** element represents an operation to create a new Inbox rule.</span></span> 
  
[<span data-ttu-id="52b01-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="52b01-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="52b01-106">Betrieb</span><span class="sxs-lookup"><span data-stu-id="52b01-106">Operations</span></span>](operations.md)
  
```xml
<CreateRuleOperation>
    <Rule/>
</CreateRuleOperation>
```

 <span data-ttu-id="52b01-107">**CreateRuleOperationType**</span><span class="sxs-lookup"><span data-stu-id="52b01-107">**CreateRuleOperationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52b01-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="52b01-108">Attributes and elements</span></span>

<span data-ttu-id="52b01-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="52b01-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52b01-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="52b01-110">Attributes</span></span>

<span data-ttu-id="52b01-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="52b01-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="52b01-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="52b01-112">Child elements</span></span>

|<span data-ttu-id="52b01-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="52b01-113">**Element**</span></span>|<span data-ttu-id="52b01-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="52b01-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52b01-115">Regel (RuleType)</span><span class="sxs-lookup"><span data-stu-id="52b01-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="52b01-116">Stellt eine Regel in dem Postfach eines Benutzers erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="52b01-116">Represents a rule to be created in a user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="52b01-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="52b01-117">Parent elements</span></span>

|<span data-ttu-id="52b01-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="52b01-118">**Element**</span></span>|<span data-ttu-id="52b01-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="52b01-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52b01-120">Betrieb</span><span class="sxs-lookup"><span data-stu-id="52b01-120">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="52b01-121">Enthält die Vorgänge, die für ein Postfach ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="52b01-121">Contains the operations that can be performed on an Inbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="52b01-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="52b01-122">Text value</span></span>

<span data-ttu-id="52b01-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="52b01-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52b01-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="52b01-124">Remarks</span></span>

<span data-ttu-id="52b01-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="52b01-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52b01-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="52b01-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52b01-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="52b01-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="52b01-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="52b01-128">Schema Name</span></span>  <br/> |<span data-ttu-id="52b01-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="52b01-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="52b01-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="52b01-130">Validation File</span></span>  <br/> |<span data-ttu-id="52b01-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="52b01-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="52b01-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="52b01-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="52b01-133">False</span><span class="sxs-lookup"><span data-stu-id="52b01-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52b01-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52b01-134">See also</span></span>



[<span data-ttu-id="52b01-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="52b01-135">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="52b01-136">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="52b01-136">SetRuleOperation</span></span>](setruleoperation.md)
  
[<span data-ttu-id="52b01-137">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="52b01-137">DeleteRuleOperation</span></span>](deleteruleoperation.md)


- [<span data-ttu-id="52b01-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="52b01-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

