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
description: Das RuleOperationError-Element stellt einen Regel Vorgangs Fehler dar.
ms.openlocfilehash: b5e0105a1fdb1564b3115a4c3a8411019f725483
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464959"
---
# <a name="ruleoperationerror"></a><span data-ttu-id="4f765-103">RuleOperationError</span><span class="sxs-lookup"><span data-stu-id="4f765-103">RuleOperationError</span></span>

<span data-ttu-id="4f765-104">Das **RuleOperationError** -Element stellt einen Regel Vorgangs Fehler dar.</span><span class="sxs-lookup"><span data-stu-id="4f765-104">The **RuleOperationError** element represents a rule operation error.</span></span> 
  
```XML
<RuleOperationError>
    <OperationIndex/>
    <ValidationErrors/>
</RuleOperationError>
```

 <span data-ttu-id="4f765-105">**RuleOperationErrorType**</span><span class="sxs-lookup"><span data-stu-id="4f765-105">**RuleOperationErrorType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4f765-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4f765-106">Attributes and elements</span></span>

<span data-ttu-id="4f765-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4f765-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f765-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4f765-108">Attributes</span></span>

<span data-ttu-id="4f765-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4f765-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4f765-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f765-110">Child elements</span></span>

|<span data-ttu-id="4f765-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f765-111">**Element**</span></span>|<span data-ttu-id="4f765-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f765-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f765-113">OperationIndex</span><span class="sxs-lookup"><span data-stu-id="4f765-113">OperationIndex</span></span>](operationindex.md) <br/> |<span data-ttu-id="4f765-114">Gibt den Index des Vorgangs in der Anforderung an, der den Regel Vorgangs Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="4f765-114">Indicates the index of the operation in the request that caused the rule operation error.</span></span>  <br/> |
|[<span data-ttu-id="4f765-115">ValidationErrors</span><span class="sxs-lookup"><span data-stu-id="4f765-115">ValidationErrors</span></span>](validationerrors.md) <br/> |<span data-ttu-id="4f765-116">Stellt ein Array von Regel Validierungsfehlern für jedes Regel Feld dar, das einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="4f765-116">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4f765-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f765-117">Parent elements</span></span>

|<span data-ttu-id="4f765-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f765-118">**Element**</span></span>|<span data-ttu-id="4f765-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f765-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f765-120">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="4f765-120">RuleOperationErrors</span></span>](ruleoperationerrors.md) <br/> |<span data-ttu-id="4f765-121">Stellt ein Array von Regel Validierungsfehlern für jedes Regel Feld dar, das einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="4f765-121">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4f765-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="4f765-122">Text value</span></span>

<span data-ttu-id="4f765-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="4f765-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4f765-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f765-124">Remarks</span></span>

<span data-ttu-id="4f765-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4f765-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f765-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4f765-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f765-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="4f765-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4f765-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4f765-128">Schema Name</span></span>  <br/> |<span data-ttu-id="4f765-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4f765-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4f765-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4f765-130">Validation File</span></span>  <br/> |<span data-ttu-id="4f765-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4f765-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4f765-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4f765-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="4f765-133">True</span><span class="sxs-lookup"><span data-stu-id="4f765-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4f765-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f765-134">See also</span></span>



- [<span data-ttu-id="4f765-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4f765-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

