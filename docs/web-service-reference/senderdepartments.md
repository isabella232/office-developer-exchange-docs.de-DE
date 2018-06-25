---
title: SenderDepartments
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SenderDepartments
api_type:
- schema
ms.assetid: b016cdde-d597-40ac-87c4-63ca68bd539d
description: Das SenderDepartments-Element gibt an, dass die Abteilung des Absenders einer der angegebenen Abteilungen im untergeordneten Wert (ProtectionRuleValueType) übereinstimmt.
ms.openlocfilehash: d40e6299bd46ede559cc2cce3bcc9d1611e96bd7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831331"
---
# <a name="senderdepartments"></a><span data-ttu-id="544ad-103">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="544ad-103">SenderDepartments</span></span>

<span data-ttu-id="544ad-104">Das **SenderDepartments** -Element gibt an, dass die Abteilung des Absenders einer der angegebenen Abteilungen im untergeordneten [Wert (ProtectionRuleValueType)](value-protectionrulevaluetype.md) übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="544ad-104">The **SenderDepartments** element specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span> 
  
```XML
<SenderDepartments>
   <Value/>
</SenderDepartments>
```

 <span data-ttu-id="544ad-105">**ProtectionRuleSenderDepartmentsType**</span><span class="sxs-lookup"><span data-stu-id="544ad-105">**ProtectionRuleSenderDepartmentsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="544ad-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="544ad-106">Attributes and elements</span></span>

<span data-ttu-id="544ad-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="544ad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="544ad-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="544ad-108">Attributes</span></span>

<span data-ttu-id="544ad-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="544ad-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="544ad-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="544ad-110">Child elements</span></span>

|<span data-ttu-id="544ad-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="544ad-111">**Element**</span></span>|<span data-ttu-id="544ad-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="544ad-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="544ad-113">Wert (ProtectionRuleValueType)</span><span class="sxs-lookup"><span data-stu-id="544ad-113">Value (ProtectionRuleValueType)</span></span>](value-protectionrulevaluetype.md) <br/> |<span data-ttu-id="544ad-114">Eine Abteilung der einzelnen Absender identifiziert.</span><span class="sxs-lookup"><span data-stu-id="544ad-114">Identifies a single sender department.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="544ad-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="544ad-115">Parent elements</span></span>

|<span data-ttu-id="544ad-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="544ad-116">**Element**</span></span>|<span data-ttu-id="544ad-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="544ad-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="544ad-118">Bedingung</span><span class="sxs-lookup"><span data-stu-id="544ad-118">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="544ad-119">Gibt die Bedingung, die erfüllt sein muss, für die Aktionsteil der Regel ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="544ad-119">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="544ad-120">Und (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="544ad-120">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="544ad-121">Gibt an, dass alle untergeordneten Elemente übereinstimmen müssen, damit zu **true**ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="544ad-121">Specifies that all child elements must match to evaluate to **true**.</span></span> <span data-ttu-id="544ad-122">Gibt an, dass mehr als ein Protection untergeordneten regelbedingung sein muss.</span><span class="sxs-lookup"><span data-stu-id="544ad-122">Specifies that there must be more than one protection rule child condition.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="544ad-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="544ad-123">Remarks</span></span>

<span data-ttu-id="544ad-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="544ad-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="544ad-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="544ad-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="544ad-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="544ad-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="544ad-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="544ad-127">Schema Name</span></span>  <br/> |<span data-ttu-id="544ad-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="544ad-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="544ad-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="544ad-129">Validation File</span></span>  <br/> |<span data-ttu-id="544ad-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="544ad-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="544ad-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="544ad-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="544ad-132">False</span><span class="sxs-lookup"><span data-stu-id="544ad-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="544ad-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="544ad-133">See also</span></span>



- [<span data-ttu-id="544ad-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="544ad-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

