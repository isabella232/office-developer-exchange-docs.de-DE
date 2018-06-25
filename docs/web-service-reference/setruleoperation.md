---
title: SetRuleOperation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetRuleOperation
api_type:
- schema
ms.assetid: 2106a85b-58fe-49be-b71d-4ca6aa66e060
description: Das Element SetRuleOperation stellt einen Vorgang zum Aktualisieren einer vorhandenen Regel dar.
ms.openlocfilehash: 9c956394d14c510e8dcc95110ef1874ea7010be0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831451"
---
# <a name="setruleoperation"></a><span data-ttu-id="b3929-103">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="b3929-103">SetRuleOperation</span></span>

<span data-ttu-id="b3929-104">Das Element **SetRuleOperation** stellt einen Vorgang zum Aktualisieren einer vorhandenen Regel dar.</span><span class="sxs-lookup"><span data-stu-id="b3929-104">The **SetRuleOperation** element represents an operation to update an existing rule.</span></span> 
  
[<span data-ttu-id="b3929-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="b3929-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="b3929-106">Betrieb</span><span class="sxs-lookup"><span data-stu-id="b3929-106">Operations</span></span>](operations.md)
  
```XML
<SetRuleOperation>
    <Rule/>
</SetRuleOperation>
```

 <span data-ttu-id="b3929-107">**SetRuleOperationType**</span><span class="sxs-lookup"><span data-stu-id="b3929-107">**SetRuleOperationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b3929-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b3929-108">Attributes and elements</span></span>

<span data-ttu-id="b3929-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b3929-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b3929-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="b3929-110">Attributes</span></span>

<span data-ttu-id="b3929-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b3929-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b3929-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b3929-112">Child elements</span></span>

|<span data-ttu-id="b3929-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b3929-113">**Element**</span></span>|<span data-ttu-id="b3929-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b3929-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3929-115">Regel (RuleType)</span><span class="sxs-lookup"><span data-stu-id="b3929-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="b3929-116">Stellt eine Regel in dem Postfach eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="b3929-116">Represents a rule in a user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b3929-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b3929-117">Parent elements</span></span>

|<span data-ttu-id="b3929-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="b3929-118">**Element**</span></span>|<span data-ttu-id="b3929-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b3929-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3929-120">Betrieb</span><span class="sxs-lookup"><span data-stu-id="b3929-120">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="b3929-121">Enthält ein Array der Regelvorgänge, die für ein Postfach ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="b3929-121">Contains an array of rule operations that can be performed on an Inbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b3929-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="b3929-122">Text value</span></span>

<span data-ttu-id="b3929-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="b3929-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b3929-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b3929-124">Remarks</span></span>

<span data-ttu-id="b3929-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b3929-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b3929-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b3929-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3929-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="b3929-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b3929-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b3929-128">Schema Name</span></span>  <br/> |<span data-ttu-id="b3929-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b3929-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="b3929-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b3929-130">Validation File</span></span>  <br/> |<span data-ttu-id="b3929-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b3929-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b3929-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b3929-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="b3929-133">False</span><span class="sxs-lookup"><span data-stu-id="b3929-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b3929-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3929-134">See also</span></span>



[<span data-ttu-id="b3929-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="b3929-135">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="b3929-136">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="b3929-136">DeleteRuleOperation</span></span>](deleteruleoperation.md)
  
[<span data-ttu-id="b3929-137">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="b3929-137">CreateRuleOperation</span></span>](createruleoperation.md)


- [<span data-ttu-id="b3929-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b3929-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

