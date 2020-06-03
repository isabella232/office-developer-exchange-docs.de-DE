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
description: Das Value-Element identifiziert eine einzelne Empfänger-oder Absender Abteilung.
ms.openlocfilehash: 908ea451800abc343fb6e4d4a4ed98d57223bd23
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465240"
---
# <a name="value-protectionrulevaluetype"></a><span data-ttu-id="3f4f9-103">Wert (ProtectionRuleValueType)</span><span class="sxs-lookup"><span data-stu-id="3f4f9-103">Value (ProtectionRuleValueType)</span></span>

<span data-ttu-id="3f4f9-104">Das **value** -Element identifiziert eine einzelne Empfänger-oder Absender Abteilung.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-104">The **Value** element identifies a single recipient or sender department.</span></span> 
  
```XML
<Value/>
```

<span data-ttu-id="3f4f9-105">**ProtectionRuleValueType**</span><span class="sxs-lookup"><span data-stu-id="3f4f9-105">**ProtectionRuleValueType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3f4f9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3f4f9-106">Attributes and elements</span></span>

<span data-ttu-id="3f4f9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3f4f9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3f4f9-108">Attributes</span></span>

<span data-ttu-id="3f4f9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3f4f9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3f4f9-110">Child elements</span></span>

<span data-ttu-id="3f4f9-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3f4f9-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3f4f9-112">Parent elements</span></span>

|<span data-ttu-id="3f4f9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3f4f9-113">**Element**</span></span>|<span data-ttu-id="3f4f9-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3f4f9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f4f9-115">Empfängerist</span><span class="sxs-lookup"><span data-stu-id="3f4f9-115">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="3f4f9-116">Gibt an, dass jeder Empfänger der e-Mail-Nachricht mit einem der angegebenen Empfänger in den untergeordneten **value** -Elementen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-116">Specifies that any recipient of the email message matches any of the specified recipients in the child **Value** elements.</span></span>  <br/> |
|[<span data-ttu-id="3f4f9-117">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="3f4f9-117">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="3f4f9-118">Gibt an, dass die Abteilung des Absenders mit einer der angegebenen Abteilungen in den untergeordneten **value** -Elementen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-118">Specifies that the department of the sender matches any of the specified departments in the child **Value** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3f4f9-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="3f4f9-119">Text value</span></span>

<span data-ttu-id="3f4f9-120">Dieses Element muss einen nicht leeren Zeichenfolgenwert enthalten.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-120">This element must contain a nonempty string value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3f4f9-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f4f9-121">Remarks</span></span>

<span data-ttu-id="3f4f9-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3f4f9-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3f4f9-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f4f9-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="3f4f9-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3f4f9-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3f4f9-125">Schema Name</span></span>  <br/> |<span data-ttu-id="3f4f9-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3f4f9-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="3f4f9-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3f4f9-127">Validation File</span></span>  <br/> |<span data-ttu-id="3f4f9-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3f4f9-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3f4f9-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3f4f9-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="3f4f9-130">False</span><span class="sxs-lookup"><span data-stu-id="3f4f9-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f4f9-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f4f9-131">See also</span></span>

- [<span data-ttu-id="3f4f9-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3f4f9-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

