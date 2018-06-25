---
title: Bedingung (RestrictionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4fdb373e-bf1b-4cb0-bbfb-444c6c6cec50
description: Das Condition-Element gibt die Bedingung, die verwendet wird, um das Ende einer Suche für eine FindItem oder einen FindConversation-Vorgang zu identifizieren.
ms.openlocfilehash: 513fc21be52a90698f1c292d6d20d7cdaab07371
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757588"
---
# <a name="condition-restrictiontype"></a><span data-ttu-id="98be5-103">Bedingung (RestrictionType)</span><span class="sxs-lookup"><span data-stu-id="98be5-103">Condition (RestrictionType)</span></span>

<span data-ttu-id="98be5-104">Das **Condition** -Element gibt die Bedingung, die verwendet wird, um das Ende einer Suche für eine **FindItem** oder einen **FindConversation** -Vorgang zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="98be5-104">The **Condition** element specifies the condition that is used to identify the end of a search for a **FindItem** or a **FindConversation** operation.</span></span> 
  
```XML
<Condition>
    <SearchExpression></SearchExpression>
</Condition>
```

 <span data-ttu-id="98be5-105">**RestrictionType**</span><span class="sxs-lookup"><span data-stu-id="98be5-105">**RestrictionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="98be5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="98be5-106">Attributes and elements</span></span>

<span data-ttu-id="98be5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="98be5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="98be5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="98be5-108">Attributes</span></span>

<span data-ttu-id="98be5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="98be5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="98be5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="98be5-110">Child elements</span></span>

|<span data-ttu-id="98be5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="98be5-111">**Element**</span></span>|<span data-ttu-id="98be5-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="98be5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98be5-113">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="98be5-113">SearchExpression</span></span>](searchexpression.md) <br/> |<span data-ttu-id="98be5-114">Abstrakte Element, das ersetzte Element innerhalb einer Einschränkung darstellt.</span><span class="sxs-lookup"><span data-stu-id="98be5-114">Abstract element that represents the substituted element within a restriction.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="98be5-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="98be5-115">Parent elements</span></span>

|<span data-ttu-id="98be5-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="98be5-116">**Element**</span></span>|<span data-ttu-id="98be5-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="98be5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98be5-118">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="98be5-118">SeekToConditionPageItemView</span></span>](seektoconditionpageitemview.md) <br/> |<span data-ttu-id="98be5-119">Gibt die Bedingung an, die das Ende einer Suche, der Startindex für eine Suche, die maximale Einträge zurückgegeben und die Richtung der Suche für einen **FindItem** oder einen Vorgang **FindConversation** identifiziert.</span><span class="sxs-lookup"><span data-stu-id="98be5-119">Identifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or a **FindConversation** operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98be5-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="98be5-120">Remarks</span></span>

<span data-ttu-id="98be5-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="98be5-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="98be5-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="98be5-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="98be5-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="98be5-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98be5-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="98be5-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="98be5-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="98be5-125">Schema Name</span></span>  <br/> |<span data-ttu-id="98be5-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="98be5-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="98be5-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="98be5-127">Validation File</span></span>  <br/> |<span data-ttu-id="98be5-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="98be5-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="98be5-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="98be5-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="98be5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98be5-130">See also</span></span>



- [<span data-ttu-id="98be5-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="98be5-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

