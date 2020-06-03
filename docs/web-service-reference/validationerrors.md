---
title: ValidationErrors
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ValidationErrors
api_type:
- schema
ms.assetid: 009526aa-22e7-4f5c-be88-079175aa9122
description: Das ValidationErrors -Element stellt ein Array der Regel Validierungsfehler auf jede Regel dar, die einen Fehler aufweist.
ms.openlocfilehash: 0861425b04e03a3e2e54a47a5027d0a11264392d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530275"
---
# <a name="validationerrors"></a><span data-ttu-id="d366d-103">ValidationErrors</span><span class="sxs-lookup"><span data-stu-id="d366d-103">ValidationErrors</span></span>

<span data-ttu-id="d366d-104">Das **ValidationErrors** -Element stellt ein Array der Regel Validierungsfehler auf jede Regel dar, die einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="d366d-104">The **ValidationErrors** element represents an array of rule validation errors on each rule field that has an error.</span></span> 
  
```XML
<VaidationErrors>
   <Error/>
</ValidationErrors>
```

 <span data-ttu-id="d366d-105">**ArrayOfRuleValidationErrorsType**</span><span class="sxs-lookup"><span data-stu-id="d366d-105">**ArrayOfRuleValidationErrorsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d366d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d366d-106">Attributes and elements</span></span>

<span data-ttu-id="d366d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d366d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d366d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d366d-108">Attributes</span></span>

<span data-ttu-id="d366d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d366d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d366d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d366d-110">Child elements</span></span>

|<span data-ttu-id="d366d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d366d-111">**Element**</span></span>|<span data-ttu-id="d366d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d366d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d366d-113">Fehler</span><span class="sxs-lookup"><span data-stu-id="d366d-113">Error</span></span>](error.md) <br/> |<span data-ttu-id="d366d-114">Stellt einen einzelnen Gültigkeitsprüfungsfehler auf eine bestimmte Regel Eigenschaftswert, Prädikat Eigenschaftswert oder Aktionswert-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d366d-114">Represents a single validation error on a particular rule property value, predicate property value, or action property value</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d366d-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d366d-115">Parent elements</span></span>

|<span data-ttu-id="d366d-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d366d-116">**Element**</span></span>|<span data-ttu-id="d366d-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d366d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d366d-118">RuleOperationError</span><span class="sxs-lookup"><span data-stu-id="d366d-118">RuleOperationError</span></span>](ruleoperationerror.md) <br/> |<span data-ttu-id="d366d-119">Stellt einen Regel Vorgang-Fehler dar.</span><span class="sxs-lookup"><span data-stu-id="d366d-119">Represents a rule operation error.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d366d-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="d366d-120">Text value</span></span>

<span data-ttu-id="d366d-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="d366d-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d366d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d366d-122">Remarks</span></span>

<span data-ttu-id="d366d-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d366d-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d366d-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d366d-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d366d-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="d366d-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d366d-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d366d-126">Schema Name</span></span>  <br/> |<span data-ttu-id="d366d-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d366d-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d366d-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d366d-128">Validation File</span></span>  <br/> |<span data-ttu-id="d366d-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d366d-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d366d-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d366d-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="d366d-131">True</span><span class="sxs-lookup"><span data-stu-id="d366d-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d366d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d366d-132">See also</span></span>



- [<span data-ttu-id="d366d-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d366d-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

