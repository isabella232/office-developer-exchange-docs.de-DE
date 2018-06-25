---
title: DeleteRuleOperation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteRuleOperation
api_type:
- schema
ms.assetid: c5e251af-f795-43cc-baaf-95d84475677c
description: Das DeleteRuleOperation-Element enthält einen Vorgang, um eine vorhandene Posteingangsregel zu löschen.
ms.openlocfilehash: 3410361e0b896fb0ef01c1873c9f8b0ac99afe58
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757935"
---
# <a name="deleteruleoperation"></a><span data-ttu-id="0c35f-103">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="0c35f-103">DeleteRuleOperation</span></span>

<span data-ttu-id="0c35f-104">Das **DeleteRuleOperation** -Element enthält einen Vorgang, um eine vorhandene Posteingangsregel zu löschen.</span><span class="sxs-lookup"><span data-stu-id="0c35f-104">The **DeleteRuleOperation** element contains an operation to delete an existing Inbox rule.</span></span> 
  
- [<span data-ttu-id="0c35f-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="0c35f-105">UpdateInboxRules</span></span>](updateinboxrules.md)
- [<span data-ttu-id="0c35f-106">Betrieb</span><span class="sxs-lookup"><span data-stu-id="0c35f-106">Operations</span></span>](operations.md)
  
```XML
<DeleteRuleOperation>
    <RuleId/>
</DeleteRuleOperation>
```

 <span data-ttu-id="0c35f-107">**DeleteRuleOperationType**</span><span class="sxs-lookup"><span data-stu-id="0c35f-107">**DeleteRuleOperationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0c35f-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0c35f-108">Attributes and elements</span></span>

<span data-ttu-id="0c35f-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0c35f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c35f-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0c35f-110">Attributes</span></span>

<span data-ttu-id="0c35f-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0c35f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0c35f-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c35f-112">Child elements</span></span>

|<span data-ttu-id="0c35f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0c35f-113">**Element**</span></span>|<span data-ttu-id="0c35f-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c35f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0c35f-115">Regel-ID</span><span class="sxs-lookup"><span data-stu-id="0c35f-115">RuleId</span></span>](ruleid.md) <br/> |<span data-ttu-id="0c35f-116">Gibt den Bezeichner der die zu löschende Regel.</span><span class="sxs-lookup"><span data-stu-id="0c35f-116">Specifies the identifier of the rule to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0c35f-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c35f-117">Parent elements</span></span>

|<span data-ttu-id="0c35f-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="0c35f-118">**Element**</span></span>|<span data-ttu-id="0c35f-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c35f-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0c35f-120">Betrieb</span><span class="sxs-lookup"><span data-stu-id="0c35f-120">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="0c35f-121">Enthält ein Array der Regelvorgänge, die für ein Postfach ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="0c35f-121">Contains an array of rule operations that can be performed on an Inbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0c35f-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="0c35f-122">Text value</span></span>

<span data-ttu-id="0c35f-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="0c35f-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0c35f-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0c35f-124">Remarks</span></span>

<span data-ttu-id="0c35f-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0c35f-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0c35f-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0c35f-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c35f-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c35f-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0c35f-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0c35f-128">Schema Name</span></span>  <br/> |<span data-ttu-id="0c35f-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0c35f-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="0c35f-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0c35f-130">Validation File</span></span>  <br/> |<span data-ttu-id="0c35f-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0c35f-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0c35f-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0c35f-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="0c35f-133">False</span><span class="sxs-lookup"><span data-stu-id="0c35f-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c35f-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c35f-134">See also</span></span>

- [<span data-ttu-id="0c35f-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="0c35f-135">UpdateInboxRules</span></span>](updateinboxrules.md) 
- [<span data-ttu-id="0c35f-136">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="0c35f-136">SetRuleOperation</span></span>](setruleoperation.md) 
- [<span data-ttu-id="0c35f-137">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="0c35f-137">CreateRuleOperation</span></span>](createruleoperation.md)
- [<span data-ttu-id="0c35f-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0c35f-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

