---
title: Empfängerist
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
description: Das recipientis-Element gibt an, dass jeder Empfänger der e-Mail-Nachricht mit einem der angegebenen Empfänger in den untergeordneten Wert (ProtectionRuleValueType)-Elementen übereinstimmt.
ms.openlocfilehash: 8f27c4484ce310c62f9bab0e6ffeea2bfac1d3ef
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463881"
---
# <a name="recipientis"></a><span data-ttu-id="d200d-103">Empfängerist</span><span class="sxs-lookup"><span data-stu-id="d200d-103">RecipientIs</span></span>

<span data-ttu-id="d200d-104">Das **recipientis** -Element gibt an, dass jeder Empfänger der e-Mail-Nachricht mit einem der angegebenen Empfänger in den untergeordneten [Wert (ProtectionRuleValueType)](value-protectionrulevaluetype.md) -Elementen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="d200d-104">The **RecipientIs** element specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span> 
  
```xml
<RecipientIs>   <Value/></RecipientIs>
```

 <span data-ttu-id="d200d-105">**ProtectionRuleRecipientIsType**</span><span class="sxs-lookup"><span data-stu-id="d200d-105">**ProtectionRuleRecipientIsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d200d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d200d-106">Attributes and elements</span></span>

<span data-ttu-id="d200d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d200d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d200d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d200d-108">Attributes</span></span>

<span data-ttu-id="d200d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d200d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d200d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d200d-110">Child elements</span></span>

|<span data-ttu-id="d200d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d200d-111">**Element**</span></span>|<span data-ttu-id="d200d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d200d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d200d-113">Wert (ProtectionRuleValueType)</span><span class="sxs-lookup"><span data-stu-id="d200d-113">Value (ProtectionRuleValueType)</span></span>](value-protectionrulevaluetype.md) <br/> |<span data-ttu-id="d200d-114">Identifiziert einen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="d200d-114">Identifies a recipient.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d200d-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d200d-115">Parent elements</span></span>

|<span data-ttu-id="d200d-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d200d-116">**Element**</span></span>|<span data-ttu-id="d200d-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d200d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d200d-118">Bedingung</span><span class="sxs-lookup"><span data-stu-id="d200d-118">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="d200d-119">Gibt die Bedingung an, die erfüllt sein muss, damit der Aktions Teil der Regel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d200d-119">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="d200d-120">Und (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="d200d-120">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="d200d-121">Gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, damit Sie zu **true**ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="d200d-121">Indicates that all child elements must match to evaluate to **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d200d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d200d-122">Remarks</span></span>

<span data-ttu-id="d200d-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d200d-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d200d-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d200d-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d200d-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="d200d-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d200d-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d200d-126">Schema Name</span></span>  <br/> |<span data-ttu-id="d200d-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d200d-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="d200d-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d200d-128">Validation File</span></span>  <br/> |<span data-ttu-id="d200d-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d200d-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d200d-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d200d-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="d200d-131">False</span><span class="sxs-lookup"><span data-stu-id="d200d-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d200d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d200d-132">See also</span></span>



- [<span data-ttu-id="d200d-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d200d-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

