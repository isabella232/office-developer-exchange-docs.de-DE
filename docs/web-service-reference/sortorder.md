---
title: SortOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SortOrder
api_type:
- schema
ms.assetid: c2413f0b-8c03-46ae-9990-13338b3c53a6
description: Das SortOrder-Element definiert, wie Elemente in einer Anforderung FindItem oder FindConversation sortiert werden.
ms.openlocfilehash: e20e5eab7972616c90079786abd78a0f7fedfebe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831519"
---
# <a name="sortorder"></a><span data-ttu-id="f4f32-103">SortOrder</span><span class="sxs-lookup"><span data-stu-id="f4f32-103">SortOrder</span></span>

<span data-ttu-id="f4f32-104">Das **SortOrder** -Element definiert, wie Elemente in einer Anforderung **FindItem** oder **FindConversation** sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="f4f32-104">The **SortOrder** element defines how items are sorted in a **FindItem** or **FindConversation** request.</span></span> 
  
```xml
<SortOrder>
   <FieldOrder/>
</SortOrder>
```

 <span data-ttu-id="f4f32-105">**NonEmptyArrayOfFieldOrdersType**</span><span class="sxs-lookup"><span data-stu-id="f4f32-105">**NonEmptyArrayOfFieldOrdersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f4f32-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f4f32-106">Attributes and elements</span></span>

<span data-ttu-id="f4f32-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f4f32-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4f32-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f4f32-108">Attributes</span></span>

<span data-ttu-id="f4f32-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f4f32-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f4f32-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f4f32-110">Child elements</span></span>

|<span data-ttu-id="f4f32-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f4f32-111">**Element**</span></span>|<span data-ttu-id="f4f32-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f4f32-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4f32-113">FieldOrder</span><span class="sxs-lookup"><span data-stu-id="f4f32-113">FieldOrder</span></span>](fieldorder.md) <br/> |<span data-ttu-id="f4f32-114">Stellt ein einzelnes Feld dar, nach dem die Ergebnisse durchsucht werden und gibt die Richtung für die Sortierung an.</span><span class="sxs-lookup"><span data-stu-id="f4f32-114">Represents a single field by which to sort results and indicates the direction for the sort.</span></span> <span data-ttu-id="f4f32-115">Eine oder mehrere der folgenden Elemente können enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="f4f32-115">One or more of these elements may be included.</span></span> <span data-ttu-id="f4f32-116">[FieldOrder](fieldorder.md) Elemente werden in der Reihenfolge angegeben, die für die Sortierung angewendet.</span><span class="sxs-lookup"><span data-stu-id="f4f32-116">[FieldOrder](fieldorder.md) elements are applied in the order specified for sorting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f4f32-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f4f32-117">Parent elements</span></span>

|<span data-ttu-id="f4f32-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="f4f32-118">**Element**</span></span>|<span data-ttu-id="f4f32-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f4f32-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4f32-120">FindItem</span><span class="sxs-lookup"><span data-stu-id="f4f32-120">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="f4f32-121">Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="f4f32-121">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="f4f32-122">Es folgt der XPath-Ausdruck, der dieses Element:`/FindItem`</span><span class="sxs-lookup"><span data-stu-id="f4f32-122">The following is the XPath expression to this element:  `/FindItem`</span></span> <br/> |
|[<span data-ttu-id="f4f32-123">FindConversation</span><span class="sxs-lookup"><span data-stu-id="f4f32-123">FindConversation</span></span>](findconversation.md) <br/> |<span data-ttu-id="f4f32-124">Definiert eine Anforderung an Unterhaltungen in einem Postfach suchen.</span><span class="sxs-lookup"><span data-stu-id="f4f32-124">Defines a request to find conversations in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f4f32-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="f4f32-125">Text value</span></span>

<span data-ttu-id="f4f32-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="f4f32-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f4f32-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f4f32-127">Remarks</span></span>

<span data-ttu-id="f4f32-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f4f32-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f4f32-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f4f32-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4f32-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="f4f32-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f4f32-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f4f32-131">Schema Name</span></span>  <br/> |<span data-ttu-id="f4f32-132">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f4f32-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f4f32-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f4f32-133">Validation File</span></span>  <br/> |<span data-ttu-id="f4f32-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f4f32-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f4f32-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f4f32-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="f4f32-136">False</span><span class="sxs-lookup"><span data-stu-id="f4f32-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4f32-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4f32-137">See also</span></span>



[<span data-ttu-id="f4f32-138">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f4f32-138">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="f4f32-139">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="f4f32-139">FindConversation operation</span></span>](findconversation-operation.md)


- [<span data-ttu-id="f4f32-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f4f32-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

