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
description: Das allinternal-Element ergibt true, wenn alle Empfänger einer e-Mail-Nachricht für die Organisation des Absenders intern sind.
ms.openlocfilehash: c5ffe15eca5d680994acb62913ebf5effacce214
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464833"
---
# <a name="allinternal"></a><span data-ttu-id="6dfe6-103">AllInternal</span><span class="sxs-lookup"><span data-stu-id="6dfe6-103">AllInternal</span></span>

<span data-ttu-id="6dfe6-104">Das **allinternal** -Element ergibt **true** , wenn alle Empfänger einer e-Mail-Nachricht für die Organisation des Absenders intern sind.</span><span class="sxs-lookup"><span data-stu-id="6dfe6-104">The **AllInternal** element evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span> 
  
```xml
<AllInternal/>
```

 <span data-ttu-id="6dfe6-105">**ProtectionRuleAllInternalType**</span><span class="sxs-lookup"><span data-stu-id="6dfe6-105">**ProtectionRuleAllInternalType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6dfe6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6dfe6-106">Attributes and elements</span></span>

<span data-ttu-id="6dfe6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6dfe6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6dfe6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6dfe6-108">Attributes</span></span>

<span data-ttu-id="6dfe6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6dfe6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6dfe6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6dfe6-110">Child elements</span></span>

<span data-ttu-id="6dfe6-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="6dfe6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6dfe6-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6dfe6-112">Parent elements</span></span>

|<span data-ttu-id="6dfe6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6dfe6-113">**Element**</span></span>|<span data-ttu-id="6dfe6-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6dfe6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6dfe6-115">Bedingung</span><span class="sxs-lookup"><span data-stu-id="6dfe6-115">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="6dfe6-116">Gibt die Bedingung an, die erfüllt sein muss, damit der Aktions Teil der Regel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6dfe6-116">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="6dfe6-117">Und (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="6dfe6-117">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="6dfe6-118">Gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, damit Sie zu **true**ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="6dfe6-118">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6dfe6-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="6dfe6-119">Text value</span></span>

<span data-ttu-id="6dfe6-120">Das **allinternal** -Element muss leer sein.</span><span class="sxs-lookup"><span data-stu-id="6dfe6-120">The **AllInternal** element must be empty.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6dfe6-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6dfe6-121">Remarks</span></span>

<span data-ttu-id="6dfe6-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6dfe6-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6dfe6-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6dfe6-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6dfe6-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="6dfe6-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6dfe6-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6dfe6-125">Schema Name</span></span>  <br/> |<span data-ttu-id="6dfe6-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6dfe6-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="6dfe6-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6dfe6-127">Validation File</span></span>  <br/> |<span data-ttu-id="6dfe6-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6dfe6-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6dfe6-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6dfe6-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="6dfe6-130">False</span><span class="sxs-lookup"><span data-stu-id="6dfe6-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6dfe6-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6dfe6-131">See also</span></span>

- [<span data-ttu-id="6dfe6-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6dfe6-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

