---
title: Wert (ProtectionRuleValueType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Value
api_type:
- schema
ms.assetid: b039bd6e-2198-47cf-9c78-a5e8b9d51c98
description: Das Value-Element identifiziert eine einzelne Empfänger oder Absender Abteilung.
ms.openlocfilehash: 6173f94dcfb83eafd62e35f185a5e8c669d50f6c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839487"
---
# <a name="value-protectionrulevaluetype"></a><span data-ttu-id="20116-103">Wert (ProtectionRuleValueType)</span><span class="sxs-lookup"><span data-stu-id="20116-103">Value (ProtectionRuleValueType)</span></span>

<span data-ttu-id="20116-104">Das **Value** -Element identifiziert eine einzelne Empfänger oder Absender Abteilung.</span><span class="sxs-lookup"><span data-stu-id="20116-104">The **Value** element identifies a single recipient or sender department.</span></span> 
  
```XML
<Value/>
```

<span data-ttu-id="20116-105">**ProtectionRuleValueType**</span><span class="sxs-lookup"><span data-stu-id="20116-105">**ProtectionRuleValueType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="20116-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="20116-106">Attributes and elements</span></span>

<span data-ttu-id="20116-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="20116-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="20116-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="20116-108">Attributes</span></span>

<span data-ttu-id="20116-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="20116-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="20116-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="20116-110">Child elements</span></span>

<span data-ttu-id="20116-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="20116-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="20116-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="20116-112">Parent elements</span></span>

|<span data-ttu-id="20116-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="20116-113">**Element**</span></span>|<span data-ttu-id="20116-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="20116-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="20116-115">RecipientIs</span><span class="sxs-lookup"><span data-stu-id="20116-115">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="20116-116">Gibt an, dass alle Empfänger der e-Mail-Nachricht mit der angegebenen Empfänger im untergeordneten **Wert** übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="20116-116">Specifies that any recipient of the email message matches any of the specified recipients in the child **Value** elements.</span></span>  <br/> |
|[<span data-ttu-id="20116-117">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="20116-117">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="20116-118">Gibt an, dass die Abteilung des Absenders einer der angegebenen Abteilungen im untergeordneten **Wert** übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="20116-118">Specifies that the department of the sender matches any of the specified departments in the child **Value** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="20116-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="20116-119">Text value</span></span>

<span data-ttu-id="20116-120">Dieses Element muss einen nicht leeren Zeichenfolgenwert enthalten.</span><span class="sxs-lookup"><span data-stu-id="20116-120">This element must contain a nonempty string value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20116-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="20116-121">Remarks</span></span>

<span data-ttu-id="20116-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="20116-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="20116-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="20116-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20116-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="20116-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="20116-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="20116-125">Schema Name</span></span>  <br/> |<span data-ttu-id="20116-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="20116-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="20116-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="20116-127">Validation File</span></span>  <br/> |<span data-ttu-id="20116-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="20116-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="20116-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="20116-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="20116-130">False</span><span class="sxs-lookup"><span data-stu-id="20116-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="20116-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20116-131">See also</span></span>

- [<span data-ttu-id="20116-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="20116-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

