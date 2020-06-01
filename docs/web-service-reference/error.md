---
title: Fehler (ungefährer Wortlaut)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Error
api_type:
- schema
ms.assetid: b1f54673-578a-496b-99f5-0fde2c669278
description: Das Error-Element stellt einen einzelnen Validierungsfehler für einen bestimmten Regel Eigenschaftswert, einen Prädikateigenschaftswert oder einen Action-Eigenschaftswert dar.
ms.openlocfilehash: 9c28f63aa79446d89152868c81c85ffa7b3a8b39
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460680"
---
# <a name="error"></a><span data-ttu-id="da49f-103">Fehler (ungefährer Wortlaut)</span><span class="sxs-lookup"><span data-stu-id="da49f-103">Error</span></span>

<span data-ttu-id="da49f-104">Das **Error** -Element stellt einen einzelnen Validierungsfehler für einen bestimmten Regel Eigenschaftswert, einen Prädikateigenschaftswert oder einen Action-Eigenschaftswert dar.</span><span class="sxs-lookup"><span data-stu-id="da49f-104">The **Error** element represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span> 
  
```XML
<Error>
   <FieldUri/>
   <ErrorCode/>
   <ErrorMessage/>
   <FieldValue/>
</Error>
```

 <span data-ttu-id="da49f-105">**RuleValidationErrorType**</span><span class="sxs-lookup"><span data-stu-id="da49f-105">**RuleValidationErrorType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="da49f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="da49f-106">Attributes and elements</span></span>

<span data-ttu-id="da49f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="da49f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da49f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="da49f-108">Attributes</span></span>

<span data-ttu-id="da49f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="da49f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="da49f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da49f-110">Child elements</span></span>

|<span data-ttu-id="da49f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="da49f-111">**Element**</span></span>|<span data-ttu-id="da49f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da49f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da49f-113">FieldUri (Regel)</span><span class="sxs-lookup"><span data-stu-id="da49f-113">FieldUri (Rule)</span></span>](fielduri-rule.md) <br/> |<span data-ttu-id="da49f-114">Gibt den URI für das Regel Feld an, das den Validierungsfehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="da49f-114">Specifies the URI to the rule field that caused the validation error.</span></span>  <br/> |
|[<span data-ttu-id="da49f-115">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="da49f-115">ErrorCode</span></span>](errorcode.md) <br/> |<span data-ttu-id="da49f-116">Stellt einen Fehlercode für die Regelüberprüfung dar, der die fehlgeschlagene Überprüfung der einzelnen Regelprädikate oder Aktionen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="da49f-116">Represents a rule validation error code that describes what failed validation for each rule predicate or action.</span></span>  <br/> |
|[<span data-ttu-id="da49f-117">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="da49f-117">ErrorMessage</span></span>](errormessage.md) <br/> |<span data-ttu-id="da49f-118">Stellt den Grund für die Überprüfungsfehler.</span><span class="sxs-lookup"><span data-stu-id="da49f-118">Represents the reason for the validation error.</span></span>  <br/> |
|[<span data-ttu-id="da49f-119">FieldValue</span><span class="sxs-lookup"><span data-stu-id="da49f-119">FieldValue</span></span>](fieldvalue.md) <br/> |<span data-ttu-id="da49f-120">Stellt den Wert des Felds dar, das den Validierungsfehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="da49f-120">Represents the value of the field that caused the validation error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="da49f-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da49f-121">Parent elements</span></span>

|<span data-ttu-id="da49f-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="da49f-122">**Element**</span></span>|<span data-ttu-id="da49f-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da49f-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da49f-124">ValidationErrors</span><span class="sxs-lookup"><span data-stu-id="da49f-124">ValidationErrors</span></span>](validationerrors.md) <br/> |<span data-ttu-id="da49f-125">Stellt ein Array von Regel Validierungsfehlern für jedes Regel Feld dar, das einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="da49f-125">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="da49f-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="da49f-126">Text value</span></span>

<span data-ttu-id="da49f-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="da49f-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="da49f-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da49f-128">Remarks</span></span>

<span data-ttu-id="da49f-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="da49f-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="da49f-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="da49f-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da49f-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="da49f-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="da49f-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="da49f-132">Schema Name</span></span>  <br/> |<span data-ttu-id="da49f-133">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="da49f-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="da49f-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="da49f-134">Validation File</span></span>  <br/> |<span data-ttu-id="da49f-135">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="da49f-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="da49f-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="da49f-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="da49f-137">True</span><span class="sxs-lookup"><span data-stu-id="da49f-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da49f-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da49f-138">See also</span></span>



- [<span data-ttu-id="da49f-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="da49f-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

