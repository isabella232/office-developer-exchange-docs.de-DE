---
title: RuleOperationErrors
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f15c7b9e-a670-4a11-bb62-2a298c91f142
description: Das RuleOperationErrors -Element stellt ein Array der Regel Validierungsfehler auf jede Regel dar, die einen Fehler aufweist.
ms.openlocfilehash: 7dc85b5cd84af5ad00511a3df2b31ee3541e12b7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831261"
---
# <a name="ruleoperationerrors"></a><span data-ttu-id="4fe26-103">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="4fe26-103">RuleOperationErrors</span></span>

<span data-ttu-id="4fe26-104">Das **RuleOperationErrors** -Element stellt ein Array der Regel Validierungsfehler auf jede Regel dar, die einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="4fe26-104">The **RuleOperationErrors** element represents an array of rule validation errors on each rule field that has an error.</span></span> 
  
[<span data-ttu-id="4fe26-105">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="4fe26-105">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
  
[<span data-ttu-id="4fe26-106">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="4fe26-106">RuleOperationErrors</span></span>](ruleoperationerrors.md)
  
```XML
<RuleOperationErrors>
    <RuleOperationError>
</RuleOperationErrors>
```

 <span data-ttu-id="4fe26-107">**ArrayOfRuleOperationErrorsType**</span><span class="sxs-lookup"><span data-stu-id="4fe26-107">**ArrayOfRuleOperationErrorsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4fe26-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4fe26-108">Attributes and elements</span></span>

<span data-ttu-id="4fe26-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4fe26-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4fe26-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="4fe26-110">Attributes</span></span>

<span data-ttu-id="4fe26-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="4fe26-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4fe26-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4fe26-112">Child elements</span></span>

|<span data-ttu-id="4fe26-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4fe26-113">**Element**</span></span>|<span data-ttu-id="4fe26-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4fe26-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4fe26-115">RuleOperationError</span><span class="sxs-lookup"><span data-stu-id="4fe26-115">RuleOperationError</span></span>](ruleoperationerror.md) <br/> |<span data-ttu-id="4fe26-116">Stellt einen Regel Vorgang-Fehler dar.</span><span class="sxs-lookup"><span data-stu-id="4fe26-116">Represents a rule operation error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4fe26-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4fe26-117">Parent elements</span></span>

|<span data-ttu-id="4fe26-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="4fe26-118">**Element**</span></span>|<span data-ttu-id="4fe26-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4fe26-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4fe26-120">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="4fe26-120">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md) <br/> |<span data-ttu-id="4fe26-121">Definiert eine Antwort auf eine Anforderung [UpdateInboxRules](updateinboxrules.md) .</span><span class="sxs-lookup"><span data-stu-id="4fe26-121">Defines a response to an [UpdateInboxRules](updateinboxrules.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4fe26-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="4fe26-122">Text value</span></span>

<span data-ttu-id="4fe26-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="4fe26-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4fe26-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4fe26-124">Remarks</span></span>

<span data-ttu-id="4fe26-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4fe26-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4fe26-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4fe26-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4fe26-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="4fe26-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4fe26-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4fe26-128">Schema name</span></span>  <br/> |<span data-ttu-id="4fe26-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4fe26-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4fe26-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4fe26-130">Validation file</span></span>  <br/> |<span data-ttu-id="4fe26-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4fe26-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4fe26-132">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="4fe26-132">Can be empty</span></span>  <br/> |<span data-ttu-id="4fe26-133">True</span><span class="sxs-lookup"><span data-stu-id="4fe26-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4fe26-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fe26-134">See also</span></span>



[<span data-ttu-id="4fe26-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="4fe26-135">UpdateInboxRules</span></span>](updateinboxrules.md)


- [<span data-ttu-id="4fe26-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4fe26-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

