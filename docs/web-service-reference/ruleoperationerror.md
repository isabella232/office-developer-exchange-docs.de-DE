---
title: RuleOperationError
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RuleOperationError
api_type:
- schema
ms.assetid: b447e610-d37c-40d3-9158-aa108a9f248e
description: Das Element RuleOperationError stellt einen Regel Vorgang-Fehler dar.
ms.openlocfilehash: ff42addea0f55b13794e2c910d4d865ad0b17bc3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831265"
---
# <a name="ruleoperationerror"></a><span data-ttu-id="59232-103">RuleOperationError</span><span class="sxs-lookup"><span data-stu-id="59232-103">RuleOperationError</span></span>

<span data-ttu-id="59232-104">Das Element **RuleOperationError** stellt einen Regel Vorgang-Fehler dar.</span><span class="sxs-lookup"><span data-stu-id="59232-104">The **RuleOperationError** element represents a rule operation error.</span></span> 
  
```XML
<RuleOperationError>
    <OperationIndex/>
    <ValidationErrors/>
</RuleOperationError>
```

 <span data-ttu-id="59232-105">**RuleOperationErrorType**</span><span class="sxs-lookup"><span data-stu-id="59232-105">**RuleOperationErrorType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="59232-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="59232-106">Attributes and elements</span></span>

<span data-ttu-id="59232-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="59232-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="59232-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="59232-108">Attributes</span></span>

<span data-ttu-id="59232-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="59232-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="59232-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="59232-110">Child elements</span></span>

|<span data-ttu-id="59232-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="59232-111">**Element**</span></span>|<span data-ttu-id="59232-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="59232-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59232-113">OperationIndex</span><span class="sxs-lookup"><span data-stu-id="59232-113">OperationIndex</span></span>](operationindex.md) <br/> |<span data-ttu-id="59232-114">Gibt den Index des Vorgangs in der Anforderung, die der Regel Vorgang Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="59232-114">Indicates the index of the operation in the request that caused the rule operation error.</span></span>  <br/> |
|[<span data-ttu-id="59232-115">ValidationErrors</span><span class="sxs-lookup"><span data-stu-id="59232-115">ValidationErrors</span></span>](validationerrors.md) <br/> |<span data-ttu-id="59232-116">Stellt ein Array der Regel Validierungsfehler auf jede Regel dar, die einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="59232-116">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="59232-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="59232-117">Parent elements</span></span>

|<span data-ttu-id="59232-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="59232-118">**Element**</span></span>|<span data-ttu-id="59232-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="59232-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59232-120">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="59232-120">RuleOperationErrors</span></span>](ruleoperationerrors.md) <br/> |<span data-ttu-id="59232-121">Stellt ein Array der Regel Validierungsfehler auf jede Regel dar, die einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="59232-121">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="59232-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="59232-122">Text value</span></span>

<span data-ttu-id="59232-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="59232-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="59232-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="59232-124">Remarks</span></span>

<span data-ttu-id="59232-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="59232-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="59232-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="59232-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59232-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="59232-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="59232-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="59232-128">Schema Name</span></span>  <br/> |<span data-ttu-id="59232-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="59232-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="59232-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="59232-130">Validation File</span></span>  <br/> |<span data-ttu-id="59232-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="59232-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="59232-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="59232-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="59232-133">True</span><span class="sxs-lookup"><span data-stu-id="59232-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="59232-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59232-134">See also</span></span>



- [<span data-ttu-id="59232-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="59232-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

