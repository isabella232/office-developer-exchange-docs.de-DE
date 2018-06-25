---
title: AllInternal
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AllInternal
api_type:
- schema
ms.assetid: b7e5072f-5d9f-4ee0-b58b-4d75d878ea1c
description: Das AllInternal-Element wird zu True ausgewertet, wenn alle Empfänger einer e-Mail-Nachricht für die Organisation des Absenders intern sind.
ms.openlocfilehash: 0ffd4178e711e3117497eed682e3fd3e0594989b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757252"
---
# <a name="allinternal"></a><span data-ttu-id="20939-103">AllInternal</span><span class="sxs-lookup"><span data-stu-id="20939-103">AllInternal</span></span>

<span data-ttu-id="20939-104">Das **AllInternal** -Element ergibt **true** , wenn alle Empfänger einer e-Mail-Nachricht intern für die Organisation des Absenders sind.</span><span class="sxs-lookup"><span data-stu-id="20939-104">The **AllInternal** element evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span> 
  
```xml
<AllInternal/>
```

 <span data-ttu-id="20939-105">**ProtectionRuleAllInternalType**</span><span class="sxs-lookup"><span data-stu-id="20939-105">**ProtectionRuleAllInternalType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="20939-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="20939-106">Attributes and elements</span></span>

<span data-ttu-id="20939-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="20939-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="20939-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="20939-108">Attributes</span></span>

<span data-ttu-id="20939-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="20939-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="20939-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="20939-110">Child elements</span></span>

<span data-ttu-id="20939-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="20939-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="20939-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="20939-112">Parent elements</span></span>

|<span data-ttu-id="20939-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="20939-113">**Element**</span></span>|<span data-ttu-id="20939-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="20939-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="20939-115">Bedingung</span><span class="sxs-lookup"><span data-stu-id="20939-115">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="20939-116">Gibt die Bedingung, die erfüllt sein muss, für die Aktionsteil der Regel ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="20939-116">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="20939-117">Und (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="20939-117">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="20939-118">Gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, damit zu **true**ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="20939-118">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="20939-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="20939-119">Text value</span></span>

<span data-ttu-id="20939-120">Das **AllInternal** -Element muss leer sein.</span><span class="sxs-lookup"><span data-stu-id="20939-120">The **AllInternal** element must be empty.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="20939-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="20939-121">Remarks</span></span>

<span data-ttu-id="20939-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="20939-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="20939-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="20939-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20939-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="20939-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="20939-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="20939-125">Schema Name</span></span>  <br/> |<span data-ttu-id="20939-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="20939-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="20939-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="20939-127">Validation File</span></span>  <br/> |<span data-ttu-id="20939-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="20939-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="20939-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="20939-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="20939-130">False</span><span class="sxs-lookup"><span data-stu-id="20939-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="20939-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20939-131">See also</span></span>

- [<span data-ttu-id="20939-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="20939-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

