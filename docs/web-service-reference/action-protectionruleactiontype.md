---
title: Action (ProtectionRuleActionType)
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
ms.openlocfilehash: 220a6fea16abb9ea823ae6239537b8c121702589
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527509"
---
# <a name="action-protectionruleactiontype"></a><span data-ttu-id="4170b-103">Action (ProtectionRuleActionType)</span><span class="sxs-lookup"><span data-stu-id="4170b-103">Action (ProtectionRuleActionType)</span></span>

<span data-ttu-id="4170b-104">Das **Action** -Element gibt an, welche Aktion ausgeführt werden muss, wenn der Bedingungsteil der Regel übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="4170b-104">The **Action** element identifies what action must be executed if the condition part of the rule matches.</span></span> 
  
```xml
<Action Name="">
   <Argument/>
</Action>

```

 <span data-ttu-id="4170b-105">**ProtectionRuleActionType**</span><span class="sxs-lookup"><span data-stu-id="4170b-105">**ProtectionRuleActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4170b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4170b-106">Attributes and elements</span></span>

<span data-ttu-id="4170b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4170b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4170b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4170b-108">Attributes</span></span>

|<span data-ttu-id="4170b-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4170b-109">**Attribute**</span></span>|<span data-ttu-id="4170b-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4170b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4170b-111">**Name**</span><span class="sxs-lookup"><span data-stu-id="4170b-111">**Name**</span></span> <br/> |<span data-ttu-id="4170b-112">Gibt den Namen der Aktion an.</span><span class="sxs-lookup"><span data-stu-id="4170b-112">Identifies the name of the action.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4170b-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4170b-113">Child elements</span></span>

|<span data-ttu-id="4170b-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="4170b-114">**Element**</span></span>|<span data-ttu-id="4170b-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4170b-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4170b-116">Argument</span><span class="sxs-lookup"><span data-stu-id="4170b-116">Argument</span></span>](argument.md) <br/> |<span data-ttu-id="4170b-117">Gibt Argumente für die Aktion an.</span><span class="sxs-lookup"><span data-stu-id="4170b-117">Specifies arguments to the action.</span></span> <span data-ttu-id="4170b-118">Dieses Element wird nicht ausgeführt, wenn für die angegebene Aktion keine Argumente angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="4170b-118">This element will not occur if the specified action does not require arguments to be specified.</span></span> <span data-ttu-id="4170b-119">Dieses Element kann einmal oder mehrmals auftreten, wenn für eine Aktion mindestens ein Argument erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4170b-119">This element can occur one or more times if an action requires one or more arguments.</span></span> <span data-ttu-id="4170b-120">Die **RightsProtectMessage** -Aktion enthält ein einzelnes Argument.</span><span class="sxs-lookup"><span data-stu-id="4170b-120">The **RightsProtectMessage** action will contain a single argument.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4170b-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4170b-121">Parent elements</span></span>

|<span data-ttu-id="4170b-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="4170b-122">**Element**</span></span>|<span data-ttu-id="4170b-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4170b-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4170b-124">Rule</span><span class="sxs-lookup"><span data-stu-id="4170b-124">Rule</span></span>](rule.md) <br/> |<span data-ttu-id="4170b-125">Enthält eine einzelne Schutz Regel.</span><span class="sxs-lookup"><span data-stu-id="4170b-125">Contains a single protection rule.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4170b-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4170b-126">Remarks</span></span>

<span data-ttu-id="4170b-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4170b-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4170b-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4170b-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4170b-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="4170b-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4170b-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4170b-130">Schema Name</span></span>  <br/> |<span data-ttu-id="4170b-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4170b-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="4170b-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4170b-132">Validation File</span></span>  <br/> |<span data-ttu-id="4170b-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4170b-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4170b-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4170b-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="4170b-135">False</span><span class="sxs-lookup"><span data-stu-id="4170b-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4170b-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4170b-136">See also</span></span>

- [<span data-ttu-id="4170b-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4170b-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

