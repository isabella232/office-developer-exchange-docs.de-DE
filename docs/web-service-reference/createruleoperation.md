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
description: Das CreateRuleOperation-Element stellt einen Vorgang zum Erstellen einer neuen Posteingangsregel dar.
ms.openlocfilehash: df857544e6d5840a3f738740114195e4c4bb5798
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460771"
---
# <a name="createruleoperation"></a><span data-ttu-id="91b03-103">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="91b03-103">CreateRuleOperation</span></span>

<span data-ttu-id="91b03-104">Das **CreateRuleOperation** -Element stellt einen Vorgang zum Erstellen einer neuen Posteingangsregel dar.</span><span class="sxs-lookup"><span data-stu-id="91b03-104">The **CreateRuleOperation** element represents an operation to create a new Inbox rule.</span></span> 
  
[<span data-ttu-id="91b03-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="91b03-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="91b03-106">Operations</span><span class="sxs-lookup"><span data-stu-id="91b03-106">Operations</span></span>](operations.md)
  
```xml
<CreateRuleOperation>
    <Rule/>
</CreateRuleOperation>
```

 <span data-ttu-id="91b03-107">**CreateRuleOperationType**</span><span class="sxs-lookup"><span data-stu-id="91b03-107">**CreateRuleOperationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="91b03-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="91b03-108">Attributes and elements</span></span>

<span data-ttu-id="91b03-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="91b03-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91b03-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="91b03-110">Attributes</span></span>

<span data-ttu-id="91b03-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="91b03-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="91b03-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91b03-112">Child elements</span></span>

|<span data-ttu-id="91b03-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="91b03-113">**Element**</span></span>|<span data-ttu-id="91b03-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91b03-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91b03-115">Regel (RuleType)</span><span class="sxs-lookup"><span data-stu-id="91b03-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="91b03-116">Stellt eine Regel dar, die im Postfach eines Benutzers erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="91b03-116">Represents a rule to be created in a user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="91b03-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91b03-117">Parent elements</span></span>

|<span data-ttu-id="91b03-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="91b03-118">**Element**</span></span>|<span data-ttu-id="91b03-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91b03-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91b03-120">Operations</span><span class="sxs-lookup"><span data-stu-id="91b03-120">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="91b03-121">Enthält die Vorgänge, die für einen Posteingang ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="91b03-121">Contains the operations that can be performed on an Inbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="91b03-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="91b03-122">Text value</span></span>

<span data-ttu-id="91b03-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="91b03-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="91b03-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91b03-124">Remarks</span></span>

<span data-ttu-id="91b03-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="91b03-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="91b03-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="91b03-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91b03-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="91b03-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="91b03-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="91b03-128">Schema Name</span></span>  <br/> |<span data-ttu-id="91b03-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="91b03-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="91b03-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="91b03-130">Validation File</span></span>  <br/> |<span data-ttu-id="91b03-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="91b03-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="91b03-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="91b03-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="91b03-133">False</span><span class="sxs-lookup"><span data-stu-id="91b03-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91b03-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91b03-134">See also</span></span>



[<span data-ttu-id="91b03-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="91b03-135">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="91b03-136">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="91b03-136">SetRuleOperation</span></span>](setruleoperation.md)
  
[<span data-ttu-id="91b03-137">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="91b03-137">DeleteRuleOperation</span></span>](deleteruleoperation.md)


- [<span data-ttu-id="91b03-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="91b03-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

