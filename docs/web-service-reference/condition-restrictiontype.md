---
title: Condition (restrictiontype)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4fdb373e-bf1b-4cb0-bbfb-444c6c6cec50
description: Das Condition-Element gibt die Bedingung an, die verwendet wird, um das Ende einer Suche nach einer FindItem oder einer FindConversation-Operation zu identifizieren.
ms.openlocfilehash: 00c5b5e615ed9b253c79dae9dc2b89c797853089
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463937"
---
# <a name="condition-restrictiontype"></a><span data-ttu-id="b6930-103">Condition (restrictiontype)</span><span class="sxs-lookup"><span data-stu-id="b6930-103">Condition (RestrictionType)</span></span>

<span data-ttu-id="b6930-104">Das **Condition** -Element gibt die Bedingung an, die verwendet wird, um das Ende einer Suche nach einer **FindItem** oder einer **FindConversation** -Operation zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b6930-104">The **Condition** element specifies the condition that is used to identify the end of a search for a **FindItem** or a **FindConversation** operation.</span></span> 
  
```XML
<Condition>
    <SearchExpression></SearchExpression>
</Condition>
```

 <span data-ttu-id="b6930-105">**Restrictiontype**</span><span class="sxs-lookup"><span data-stu-id="b6930-105">**RestrictionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b6930-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b6930-106">Attributes and elements</span></span>

<span data-ttu-id="b6930-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b6930-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b6930-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b6930-108">Attributes</span></span>

<span data-ttu-id="b6930-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b6930-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b6930-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b6930-110">Child elements</span></span>

|<span data-ttu-id="b6930-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b6930-111">**Element**</span></span>|<span data-ttu-id="b6930-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b6930-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6930-113">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="b6930-113">SearchExpression</span></span>](searchexpression.md) <br/> |<span data-ttu-id="b6930-114">Abstract-Element, das das ersetzte Element innerhalb einer Einschränkung darstellt.</span><span class="sxs-lookup"><span data-stu-id="b6930-114">Abstract element that represents the substituted element within a restriction.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b6930-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b6930-115">Parent elements</span></span>

|<span data-ttu-id="b6930-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="b6930-116">**Element**</span></span>|<span data-ttu-id="b6930-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b6930-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6930-118">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="b6930-118">SeekToConditionPageItemView</span></span>](seektoconditionpageitemview.md) <br/> |<span data-ttu-id="b6930-119">Gibt die Bedingung an, die verwendet wird, um das Ende einer Suche, den startIndex einer Suche, die maximal zurückzugebenden Einträge und die Suchanweisungen für eine **FindItem** oder einen **FindConversation** -Vorgang zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b6930-119">Identifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or a **FindConversation** operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6930-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6930-120">Remarks</span></span>

<span data-ttu-id="b6930-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b6930-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b6930-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b6930-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b6930-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b6930-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6930-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="b6930-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b6930-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b6930-125">Schema Name</span></span>  <br/> |<span data-ttu-id="b6930-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="b6930-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="b6930-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b6930-127">Validation File</span></span>  <br/> |<span data-ttu-id="b6930-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="b6930-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="b6930-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b6930-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="b6930-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6930-130">See also</span></span>



- [<span data-ttu-id="b6930-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b6930-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

