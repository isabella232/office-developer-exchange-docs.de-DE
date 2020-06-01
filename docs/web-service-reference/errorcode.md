---
title: ErrorCode
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0bb00cee-c66b-4f34-b99d-355458f5e83b
description: Das ErrorCode-Element stellt einen Fehlercode für die Regelüberprüfung dar, der beschreibt, welche fehlgeschlagene Validierung für jedes Regelprädikat oder jede Aktion ausgeführt wurde.
ms.openlocfilehash: 6432aeee786d74a9afcb346cb66765f9001257de
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460078"
---
# <a name="errorcode"></a><span data-ttu-id="dccab-103">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="dccab-103">ErrorCode</span></span>

<span data-ttu-id="dccab-104">Das **errorCode** -Element stellt einen Fehlercode für die Regelüberprüfung dar, der beschreibt, welche fehlgeschlagene Validierung für jedes Regelprädikat oder jede Aktion ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="dccab-104">The **ErrorCode** element represents a rule validation error code that describes what failed validation for each rule predicate or action.</span></span> 
  
```XML
<ErrorCode/>
```

 <span data-ttu-id="dccab-105">**RuleValidationErrorCodeType**</span><span class="sxs-lookup"><span data-stu-id="dccab-105">**RuleValidationErrorCodeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dccab-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dccab-106">Attributes and elements</span></span>

<span data-ttu-id="dccab-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dccab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dccab-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dccab-108">Attributes</span></span>

<span data-ttu-id="dccab-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="dccab-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dccab-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dccab-110">Child elements</span></span>

<span data-ttu-id="dccab-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="dccab-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dccab-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dccab-112">Parent elements</span></span>

|<span data-ttu-id="dccab-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="dccab-113">**Element**</span></span>|<span data-ttu-id="dccab-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dccab-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dccab-115">Fehler</span><span class="sxs-lookup"><span data-stu-id="dccab-115">Error</span></span>](error.md) <br/> |<span data-ttu-id="dccab-116">Stellt einen einzelnen Validierungsfehler für einen bestimmten Regel Eigenschaftswert, einen Prädikateigenschaftswert oder einen Action-Eigenschaftswert dar.</span><span class="sxs-lookup"><span data-stu-id="dccab-116">Represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dccab-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="dccab-117">Text value</span></span>

<span data-ttu-id="dccab-118">Der Textwert für dieses Element ist auf eine der folgenden Zeichenfolgen beschränkt:</span><span class="sxs-lookup"><span data-stu-id="dccab-118">The text value for this element is restricted to one of the following strings:</span></span>
  
- <span data-ttu-id="dccab-119">ADOperationFailure</span><span class="sxs-lookup"><span data-stu-id="dccab-119">ADOperationFailure</span></span>
    
- <span data-ttu-id="dccab-120">ConnectedAccountNotFound</span><span class="sxs-lookup"><span data-stu-id="dccab-120">ConnectedAccountNotFound</span></span>
    
- <span data-ttu-id="dccab-121">CreateWithRuleId</span><span class="sxs-lookup"><span data-stu-id="dccab-121">CreateWithRuleId</span></span>
    
- <span data-ttu-id="dccab-122">EmptyValueFound</span><span class="sxs-lookup"><span data-stu-id="dccab-122">EmptyValueFound</span></span>
    
- <span data-ttu-id="dccab-123">DuplicatedPriority</span><span class="sxs-lookup"><span data-stu-id="dccab-123">DuplicatedPriority</span></span>
    
- <span data-ttu-id="dccab-124">DuplicatedOperationOnTheSameRule</span><span class="sxs-lookup"><span data-stu-id="dccab-124">DuplicatedOperationOnTheSameRule</span></span>
    
- <span data-ttu-id="dccab-125">FolderDoesNotExist</span><span class="sxs-lookup"><span data-stu-id="dccab-125">FolderDoesNotExist</span></span>
    
- <span data-ttu-id="dccab-126">InvalidAddress</span><span class="sxs-lookup"><span data-stu-id="dccab-126">InvalidAddress</span></span>
    
- <span data-ttu-id="dccab-127">InvalidDateRange</span><span class="sxs-lookup"><span data-stu-id="dccab-127">InvalidDateRange</span></span>
    
- <span data-ttu-id="dccab-128">InvalidFolderId</span><span class="sxs-lookup"><span data-stu-id="dccab-128">InvalidFolderId</span></span>
    
- <span data-ttu-id="dccab-129">InvalidSizeRange</span><span class="sxs-lookup"><span data-stu-id="dccab-129">InvalidSizeRange</span></span>
    
- <span data-ttu-id="dccab-130">Invalidvalue</span><span class="sxs-lookup"><span data-stu-id="dccab-130">InvalidValue</span></span>
    
- <span data-ttu-id="dccab-131">MessageClassificationNotFound</span><span class="sxs-lookup"><span data-stu-id="dccab-131">MessageClassificationNotFound</span></span>
    
- <span data-ttu-id="dccab-132">Missing</span><span class="sxs-lookup"><span data-stu-id="dccab-132">MissingAction</span></span>
    
- <span data-ttu-id="dccab-133">Missparameter</span><span class="sxs-lookup"><span data-stu-id="dccab-133">MissingParameter</span></span>
    
- <span data-ttu-id="dccab-134">MissingRangeValue</span><span class="sxs-lookup"><span data-stu-id="dccab-134">MissingRangeValue</span></span>
    
- <span data-ttu-id="dccab-135">NotSettable</span><span class="sxs-lookup"><span data-stu-id="dccab-135">NotSettable</span></span>
    
- <span data-ttu-id="dccab-136">RecipientDoesNotExist</span><span class="sxs-lookup"><span data-stu-id="dccab-136">RecipientDoesNotExist</span></span>
    
- <span data-ttu-id="dccab-137">RuleNotFound</span><span class="sxs-lookup"><span data-stu-id="dccab-137">RuleNotFound</span></span>
    
- <span data-ttu-id="dccab-138">SizeLessThanZero</span><span class="sxs-lookup"><span data-stu-id="dccab-138">SizeLessThanZero</span></span>
    
- <span data-ttu-id="dccab-139">StringValueTooBig</span><span class="sxs-lookup"><span data-stu-id="dccab-139">StringValueTooBig</span></span>
    
- <span data-ttu-id="dccab-140">UnsupportedAddress</span><span class="sxs-lookup"><span data-stu-id="dccab-140">UnsupportedAddress</span></span>
    
- <span data-ttu-id="dccab-141">UnexpectedError</span><span class="sxs-lookup"><span data-stu-id="dccab-141">UnexpectedError</span></span>
    
- <span data-ttu-id="dccab-142">UnsupportedRule</span><span class="sxs-lookup"><span data-stu-id="dccab-142">UnsupportedRule</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dccab-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dccab-143">Remarks</span></span>

<span data-ttu-id="dccab-144">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="dccab-144">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dccab-145">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="dccab-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dccab-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="dccab-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dccab-147">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dccab-147">Schema Name</span></span>  <br/> |<span data-ttu-id="dccab-148">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="dccab-148">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dccab-149">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dccab-149">Validation File</span></span>  <br/> |<span data-ttu-id="dccab-150">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="dccab-150">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dccab-151">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="dccab-151">Can be Empty</span></span>  <br/> |<span data-ttu-id="dccab-152">False</span><span class="sxs-lookup"><span data-stu-id="dccab-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dccab-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dccab-153">See also</span></span>



- [<span data-ttu-id="dccab-154">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="dccab-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

