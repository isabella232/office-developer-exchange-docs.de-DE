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
description: Das DeleteRuleOperation-Element enthält einen Vorgang zum Löschen einer vorhandenen Posteingangsregel.
ms.openlocfilehash: 6b17f7f99f1fd9b9889db00fdf55fba5eef5aba8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526921"
---
# <a name="deleteruleoperation"></a><span data-ttu-id="3c55c-103">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="3c55c-103">DeleteRuleOperation</span></span>

<span data-ttu-id="3c55c-104">Das **DeleteRuleOperation** -Element enthält einen Vorgang zum Löschen einer vorhandenen Posteingangsregel.</span><span class="sxs-lookup"><span data-stu-id="3c55c-104">The **DeleteRuleOperation** element contains an operation to delete an existing Inbox rule.</span></span> 
  
- [<span data-ttu-id="3c55c-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="3c55c-105">UpdateInboxRules</span></span>](updateinboxrules.md)
- [<span data-ttu-id="3c55c-106">Operations</span><span class="sxs-lookup"><span data-stu-id="3c55c-106">Operations</span></span>](operations.md)
  
```XML
<DeleteRuleOperation>
    <RuleId/>
</DeleteRuleOperation>
```

 <span data-ttu-id="3c55c-107">**DeleteRuleOperationType**</span><span class="sxs-lookup"><span data-stu-id="3c55c-107">**DeleteRuleOperationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3c55c-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3c55c-108">Attributes and elements</span></span>

<span data-ttu-id="3c55c-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3c55c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c55c-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="3c55c-110">Attributes</span></span>

<span data-ttu-id="3c55c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3c55c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3c55c-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c55c-112">Child elements</span></span>

|<span data-ttu-id="3c55c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c55c-113">**Element**</span></span>|<span data-ttu-id="3c55c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c55c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c55c-115">RuleId</span><span class="sxs-lookup"><span data-stu-id="3c55c-115">RuleId</span></span>](ruleid.md) <br/> |<span data-ttu-id="3c55c-116">Gibt den Bezeichner der Regel an, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c55c-116">Specifies the identifier of the rule to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3c55c-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c55c-117">Parent elements</span></span>

|<span data-ttu-id="3c55c-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c55c-118">**Element**</span></span>|<span data-ttu-id="3c55c-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c55c-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c55c-120">Betrieb</span><span class="sxs-lookup"><span data-stu-id="3c55c-120">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="3c55c-121">Enthält ein Array der Regelvorgänge, die für ein Postfach ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="3c55c-121">Contains an array of rule operations that can be performed on an Inbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3c55c-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="3c55c-122">Text value</span></span>

<span data-ttu-id="3c55c-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="3c55c-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3c55c-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c55c-124">Remarks</span></span>

<span data-ttu-id="3c55c-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3c55c-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c55c-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3c55c-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c55c-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c55c-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3c55c-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3c55c-128">Schema Name</span></span>  <br/> |<span data-ttu-id="3c55c-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3c55c-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="3c55c-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3c55c-130">Validation File</span></span>  <br/> |<span data-ttu-id="3c55c-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3c55c-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3c55c-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3c55c-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="3c55c-133">False</span><span class="sxs-lookup"><span data-stu-id="3c55c-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3c55c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c55c-134">See also</span></span>

- [<span data-ttu-id="3c55c-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="3c55c-135">UpdateInboxRules</span></span>](updateinboxrules.md) 
- [<span data-ttu-id="3c55c-136">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="3c55c-136">SetRuleOperation</span></span>](setruleoperation.md) 
- [<span data-ttu-id="3c55c-137">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="3c55c-137">CreateRuleOperation</span></span>](createruleoperation.md)
- [<span data-ttu-id="3c55c-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3c55c-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

