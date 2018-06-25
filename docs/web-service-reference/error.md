---
title: Fehler
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
description: Das Error-Element stellt einen einzelnen Gültigkeitsprüfungsfehler auf eine bestimmte Regel Eigenschaftswert, Prädikat Eigenschaftswert oder Aktionswert-Eigenschaft.
ms.openlocfilehash: adb2de56b7610aa92b5bf5b8d43ac22f35021b64
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758263"
---
# <a name="error"></a><span data-ttu-id="8ccf7-103">Fehler</span><span class="sxs-lookup"><span data-stu-id="8ccf7-103">Error</span></span>

<span data-ttu-id="8ccf7-104">Das **Error** -Element stellt einen einzelnen Gültigkeitsprüfungsfehler auf eine bestimmte Regel Eigenschaftswert, Prädikat Eigenschaftswert oder Aktionswert-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8ccf7-104">The **Error** element represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span> 
  
```XML
<Error>
   <FieldUri/>
   <ErrorCode/>
   <ErrorMessage/>
   <FieldValue/>
</Error>
```

 <span data-ttu-id="8ccf7-105">**RuleValidationErrorType**</span><span class="sxs-lookup"><span data-stu-id="8ccf7-105">**RuleValidationErrorType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8ccf7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8ccf7-106">Attributes and elements</span></span>

<span data-ttu-id="8ccf7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8ccf7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8ccf7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8ccf7-108">Attributes</span></span>

<span data-ttu-id="8ccf7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8ccf7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8ccf7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8ccf7-110">Child elements</span></span>

|<span data-ttu-id="8ccf7-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8ccf7-111">**Element**</span></span>|<span data-ttu-id="8ccf7-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8ccf7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8ccf7-113">FieldUri (Regel)</span><span class="sxs-lookup"><span data-stu-id="8ccf7-113">FieldUri (Rule)</span></span>](fielduri-rule.md) <br/> |<span data-ttu-id="8ccf7-114">Gibt den URI für die Regel dar, das den Validierungsfehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="8ccf7-114">Specifies the URI to the rule field that caused the validation error.</span></span>  <br/> |
|[<span data-ttu-id="8ccf7-115">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="8ccf7-115">ErrorCode</span></span>](errorcode.md) <br/> |<span data-ttu-id="8ccf7-116">Stellt einen Regel Validierung Fehlercode, die beschreibt, welcher Vorgang fehlgeschlagen ist Überprüfung für jede Regel Prädikat oder Aktion.</span><span class="sxs-lookup"><span data-stu-id="8ccf7-116">Represents a rule validation error code that describes what failed validation for each rule predicate or action.</span></span>  <br/> |
|[<span data-ttu-id="8ccf7-117">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="8ccf7-117">ErrorMessage</span></span>](errormessage.md) <br/> |<span data-ttu-id="8ccf7-118">Stellt den Grund für die Überprüfungsfehler.</span><span class="sxs-lookup"><span data-stu-id="8ccf7-118">Represents the reason for the validation error.</span></span>  <br/> |
|[<span data-ttu-id="8ccf7-119">FieldValue</span><span class="sxs-lookup"><span data-stu-id="8ccf7-119">FieldValue</span></span>](fieldvalue.md) <br/> |<span data-ttu-id="8ccf7-120">Stellt den Wert des Felds, das den Validierungsfehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="8ccf7-120">Represents the value of the field that caused the validation error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8ccf7-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8ccf7-121">Parent elements</span></span>

|<span data-ttu-id="8ccf7-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="8ccf7-122">**Element**</span></span>|<span data-ttu-id="8ccf7-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8ccf7-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8ccf7-124">ValidationErrors</span><span class="sxs-lookup"><span data-stu-id="8ccf7-124">ValidationErrors</span></span>](validationerrors.md) <br/> |<span data-ttu-id="8ccf7-125">Stellt ein Array der Regel Validierungsfehler auf jede Regel dar, die einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="8ccf7-125">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8ccf7-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="8ccf7-126">Text value</span></span>

<span data-ttu-id="8ccf7-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="8ccf7-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8ccf7-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8ccf7-128">Remarks</span></span>

<span data-ttu-id="8ccf7-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8ccf7-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8ccf7-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8ccf7-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ccf7-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="8ccf7-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8ccf7-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8ccf7-132">Schema Name</span></span>  <br/> |<span data-ttu-id="8ccf7-133">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8ccf7-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8ccf7-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8ccf7-134">Validation File</span></span>  <br/> |<span data-ttu-id="8ccf7-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8ccf7-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8ccf7-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8ccf7-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="8ccf7-137">True</span><span class="sxs-lookup"><span data-stu-id="8ccf7-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8ccf7-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ccf7-138">See also</span></span>



- [<span data-ttu-id="8ccf7-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8ccf7-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

