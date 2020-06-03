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
ms.openlocfilehash: d547155f3cbf9eedd0f9bfac7bf3768b3630b50e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464952"
---
# <a name="ruleoperationerrors"></a><span data-ttu-id="574a6-103">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="574a6-103">RuleOperationErrors</span></span>

<span data-ttu-id="574a6-104">Das **RuleOperationErrors** -Element stellt ein Array der Regel Validierungsfehler auf jede Regel dar, die einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="574a6-104">The **RuleOperationErrors** element represents an array of rule validation errors on each rule field that has an error.</span></span> 
  
[<span data-ttu-id="574a6-105">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="574a6-105">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
  
[<span data-ttu-id="574a6-106">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="574a6-106">RuleOperationErrors</span></span>](ruleoperationerrors.md)
  
```XML
<RuleOperationErrors>
    <RuleOperationError>
</RuleOperationErrors>
```

 <span data-ttu-id="574a6-107">**ArrayOfRuleOperationErrorsType**</span><span class="sxs-lookup"><span data-stu-id="574a6-107">**ArrayOfRuleOperationErrorsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="574a6-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="574a6-108">Attributes and elements</span></span>

<span data-ttu-id="574a6-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="574a6-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="574a6-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="574a6-110">Attributes</span></span>

<span data-ttu-id="574a6-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="574a6-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="574a6-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="574a6-112">Child elements</span></span>

|<span data-ttu-id="574a6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="574a6-113">**Element**</span></span>|<span data-ttu-id="574a6-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="574a6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="574a6-115">RuleOperationError</span><span class="sxs-lookup"><span data-stu-id="574a6-115">RuleOperationError</span></span>](ruleoperationerror.md) <br/> |<span data-ttu-id="574a6-116">Stellt einen Regel Vorgang-Fehler dar.</span><span class="sxs-lookup"><span data-stu-id="574a6-116">Represents a rule operation error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="574a6-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="574a6-117">Parent elements</span></span>

|<span data-ttu-id="574a6-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="574a6-118">**Element**</span></span>|<span data-ttu-id="574a6-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="574a6-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="574a6-120">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="574a6-120">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md) <br/> |<span data-ttu-id="574a6-121">Definiert eine Antwort auf eine Anforderung [UpdateInboxRules](updateinboxrules.md) .</span><span class="sxs-lookup"><span data-stu-id="574a6-121">Defines a response to an [UpdateInboxRules](updateinboxrules.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="574a6-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="574a6-122">Text value</span></span>

<span data-ttu-id="574a6-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="574a6-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="574a6-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="574a6-124">Remarks</span></span>

<span data-ttu-id="574a6-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="574a6-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="574a6-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="574a6-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="574a6-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="574a6-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="574a6-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="574a6-128">Schema name</span></span>  <br/> |<span data-ttu-id="574a6-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="574a6-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="574a6-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="574a6-130">Validation file</span></span>  <br/> |<span data-ttu-id="574a6-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="574a6-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="574a6-132">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="574a6-132">Can be empty</span></span>  <br/> |<span data-ttu-id="574a6-133">True</span><span class="sxs-lookup"><span data-stu-id="574a6-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="574a6-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="574a6-134">See also</span></span>



[<span data-ttu-id="574a6-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="574a6-135">UpdateInboxRules</span></span>](updateinboxrules.md)


- [<span data-ttu-id="574a6-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="574a6-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

