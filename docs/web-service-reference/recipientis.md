---
title: RecipientIs
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientIs
api_type:
- schema
ms.assetid: 5d2fd7ce-6137-4b3c-a716-c0218dcc8a09
description: Das RecipientIs-Element gibt an, dass alle Empfänger der E-mail-Nachricht mit der angegebenen Empfänger im untergeordneten Wert (ProtectionRuleValueType) entspricht.
ms.openlocfilehash: b6d5c150cd874d1aced7f2d83ff36409e0738728
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830975"
---
# <a name="recipientis"></a><span data-ttu-id="77a49-103">RecipientIs</span><span class="sxs-lookup"><span data-stu-id="77a49-103">RecipientIs</span></span>

<span data-ttu-id="77a49-104">Das **RecipientIs** -Element gibt an, dass alle Empfänger der E-mail-Nachricht mit der angegebenen Empfänger im untergeordneten [Wert (ProtectionRuleValueType)](value-protectionrulevaluetype.md) entspricht.</span><span class="sxs-lookup"><span data-stu-id="77a49-104">The **RecipientIs** element specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span> 
  
```xml
<RecipientIs>   <Value/></RecipientIs>
```

 <span data-ttu-id="77a49-105">**ProtectionRuleRecipientIsType**</span><span class="sxs-lookup"><span data-stu-id="77a49-105">**ProtectionRuleRecipientIsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="77a49-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="77a49-106">Attributes and elements</span></span>

<span data-ttu-id="77a49-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="77a49-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="77a49-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="77a49-108">Attributes</span></span>

<span data-ttu-id="77a49-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="77a49-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="77a49-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="77a49-110">Child elements</span></span>

|<span data-ttu-id="77a49-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="77a49-111">**Element**</span></span>|<span data-ttu-id="77a49-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="77a49-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77a49-113">Wert (ProtectionRuleValueType)</span><span class="sxs-lookup"><span data-stu-id="77a49-113">Value (ProtectionRuleValueType)</span></span>](value-protectionrulevaluetype.md) <br/> |<span data-ttu-id="77a49-114">Gibt einen Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="77a49-114">Identifies a recipient.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="77a49-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="77a49-115">Parent elements</span></span>

|<span data-ttu-id="77a49-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="77a49-116">**Element**</span></span>|<span data-ttu-id="77a49-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="77a49-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77a49-118">Bedingung</span><span class="sxs-lookup"><span data-stu-id="77a49-118">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="77a49-119">Gibt die Bedingung, die erfüllt sein muss, für die Aktionsteil der Regel ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="77a49-119">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="77a49-120">Und (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="77a49-120">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="77a49-121">Gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, damit zu **true**ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="77a49-121">Indicates that all child elements must match to evaluate to **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77a49-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="77a49-122">Remarks</span></span>

<span data-ttu-id="77a49-123">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="77a49-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="77a49-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="77a49-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77a49-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="77a49-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="77a49-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="77a49-126">Schema Name</span></span>  <br/> |<span data-ttu-id="77a49-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="77a49-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="77a49-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="77a49-128">Validation File</span></span>  <br/> |<span data-ttu-id="77a49-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="77a49-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="77a49-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="77a49-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="77a49-131">False</span><span class="sxs-lookup"><span data-stu-id="77a49-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="77a49-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77a49-132">See also</span></span>



- [<span data-ttu-id="77a49-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="77a49-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

