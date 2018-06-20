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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831265"
---
# <a name="ruleoperationerror"></a><span data-ttu-id="1f855-103">RuleOperationError</span><span class="sxs-lookup"><span data-stu-id="1f855-103">RuleOperationError</span></span>

<span data-ttu-id="1f855-104">Das Element **RuleOperationError** stellt einen Regel Vorgang-Fehler dar.</span><span class="sxs-lookup"><span data-stu-id="1f855-104">The **RuleOperationError** element represents a rule operation error.</span></span> 
  
```XML
<RuleOperationError>
    <OperationIndex/>
    <ValidationErrors/>
</RuleOperationError>
```

 <span data-ttu-id="1f855-105">**RuleOperationErrorType**</span><span class="sxs-lookup"><span data-stu-id="1f855-105">**RuleOperationErrorType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1f855-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1f855-106">Attributes and elements</span></span>

<span data-ttu-id="1f855-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1f855-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f855-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1f855-108">Attributes</span></span>

<span data-ttu-id="1f855-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f855-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1f855-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f855-110">Child elements</span></span>

|<span data-ttu-id="1f855-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1f855-111">**Element**</span></span>|<span data-ttu-id="1f855-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1f855-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1f855-113">OperationIndex</span><span class="sxs-lookup"><span data-stu-id="1f855-113">OperationIndex</span></span>](operationindex.md) <br/> |<span data-ttu-id="1f855-114">Gibt den Index des Vorgangs in der Anforderung, die der Regel Vorgang Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="1f855-114">Indicates the index of the operation in the request that caused the rule operation error.</span></span>  <br/> |
|[<span data-ttu-id="1f855-115">ValidationErrors</span><span class="sxs-lookup"><span data-stu-id="1f855-115">ValidationErrors</span></span>](validationerrors.md) <br/> |<span data-ttu-id="1f855-116">Stellt ein Array der Regel Validierungsfehler auf jede Regel dar, die einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="1f855-116">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1f855-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f855-117">Parent elements</span></span>

|<span data-ttu-id="1f855-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="1f855-118">**Element**</span></span>|<span data-ttu-id="1f855-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1f855-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1f855-120">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="1f855-120">RuleOperationErrors</span></span>](ruleoperationerrors.md) <br/> |<span data-ttu-id="1f855-121">Stellt ein Array der Regel Validierungsfehler auf jede Regel dar, die einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="1f855-121">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1f855-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="1f855-122">Text value</span></span>

<span data-ttu-id="1f855-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f855-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1f855-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1f855-124">Remarks</span></span>

<span data-ttu-id="1f855-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1f855-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1f855-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1f855-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f855-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f855-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1f855-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1f855-128">Schema Name</span></span>  <br/> |<span data-ttu-id="1f855-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="1f855-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1f855-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1f855-130">Validation File</span></span>  <br/> |<span data-ttu-id="1f855-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1f855-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1f855-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1f855-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="1f855-133">True</span><span class="sxs-lookup"><span data-stu-id="1f855-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1f855-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f855-134">See also</span></span>



- [<span data-ttu-id="1f855-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1f855-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

