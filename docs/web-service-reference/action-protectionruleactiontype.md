---
title: Aktion (ProtectionRuleActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Action
api_type:
- schema
ms.assetid: ca090dec-e2c5-49c8-a057-8d1f2409147f
description: Das Action-Element gibt an, welche Aktion ausgeführt werden muss, wenn der Bedingungsteil der Regel übereinstimmt.
ms.openlocfilehash: 8f699e698d3159c5ff2636da506542da3b218251
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758388"
---
# <a name="action-protectionruleactiontype"></a><span data-ttu-id="7ad7f-103">Aktion (ProtectionRuleActionType)</span><span class="sxs-lookup"><span data-stu-id="7ad7f-103">Action (ProtectionRuleActionType)</span></span>

<span data-ttu-id="7ad7f-104">Das **Action** -Element gibt an, welche Aktion ausgeführt werden muss, wenn der Bedingungsteil der Regel übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="7ad7f-104">The **Action** element identifies what action must be executed if the condition part of the rule matches.</span></span> 
  
```xml
<Action Name="">
   <Argument/>
</Action>

```

 <span data-ttu-id="7ad7f-105">**ProtectionRuleActionType**</span><span class="sxs-lookup"><span data-stu-id="7ad7f-105">**ProtectionRuleActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7ad7f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7ad7f-106">Attributes and elements</span></span>

<span data-ttu-id="7ad7f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7ad7f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7ad7f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7ad7f-108">Attributes</span></span>

|<span data-ttu-id="7ad7f-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7ad7f-109">**Attribute**</span></span>|<span data-ttu-id="7ad7f-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7ad7f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7ad7f-111">**Name**</span><span class="sxs-lookup"><span data-stu-id="7ad7f-111">**Name**</span></span> <br/> |<span data-ttu-id="7ad7f-112">Gibt den Namen der Aktion.</span><span class="sxs-lookup"><span data-stu-id="7ad7f-112">Identifies the name of the action.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7ad7f-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7ad7f-113">Child elements</span></span>

|<span data-ttu-id="7ad7f-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="7ad7f-114">**Element**</span></span>|<span data-ttu-id="7ad7f-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7ad7f-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ad7f-116">Argument</span><span class="sxs-lookup"><span data-stu-id="7ad7f-116">Argument</span></span>](argument.md) <br/> |<span data-ttu-id="7ad7f-117">Gibt die Argumente für die Aktion an.</span><span class="sxs-lookup"><span data-stu-id="7ad7f-117">Specifies arguments to the action.</span></span> <span data-ttu-id="7ad7f-118">Dieses Element nicht ausgeführt werden, wenn die angegebene Aktion Argumente angegeben werden nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7ad7f-118">This element will not occur if the specified action does not require arguments to be specified.</span></span> <span data-ttu-id="7ad7f-119">Dieses Element kann ein oder mehrere Male auftreten, wenn eine Aktion ein oder mehrere Argumente erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7ad7f-119">This element can occur one or more times if an action requires one or more arguments.</span></span> <span data-ttu-id="7ad7f-120">Die **RightsProtectMessage** -Aktion enthält ein einziges Argument.</span><span class="sxs-lookup"><span data-stu-id="7ad7f-120">The **RightsProtectMessage** action will contain a single argument.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7ad7f-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7ad7f-121">Parent elements</span></span>

|<span data-ttu-id="7ad7f-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="7ad7f-122">**Element**</span></span>|<span data-ttu-id="7ad7f-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7ad7f-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ad7f-124">Rule</span><span class="sxs-lookup"><span data-stu-id="7ad7f-124">Rule</span></span>](rule.md) <br/> |<span data-ttu-id="7ad7f-125">Enthält eine einzelne Schutzregel.</span><span class="sxs-lookup"><span data-stu-id="7ad7f-125">Contains a single protection rule.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ad7f-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7ad7f-126">Remarks</span></span>

<span data-ttu-id="7ad7f-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7ad7f-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7ad7f-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7ad7f-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ad7f-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="7ad7f-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7ad7f-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7ad7f-130">Schema Name</span></span>  <br/> |<span data-ttu-id="7ad7f-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7ad7f-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="7ad7f-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7ad7f-132">Validation File</span></span>  <br/> |<span data-ttu-id="7ad7f-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7ad7f-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7ad7f-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7ad7f-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="7ad7f-135">False</span><span class="sxs-lookup"><span data-stu-id="7ad7f-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ad7f-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ad7f-136">See also</span></span>

- [<span data-ttu-id="7ad7f-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7ad7f-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

