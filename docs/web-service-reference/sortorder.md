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
description: Das Sortierreihenfolge-Element definiert, wie Elemente in einer FindItem-oder FindConversation-Anforderung sortiert werden.
ms.openlocfilehash: b520bb3ca6daadc777e7235b2b7420a12e425048
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468369"
---
# <a name="sortorder"></a><span data-ttu-id="3964b-103">SortOrder</span><span class="sxs-lookup"><span data-stu-id="3964b-103">SortOrder</span></span>

<span data-ttu-id="3964b-104">Das **Sortierreihenfolge** -Element definiert, wie Elemente in einer **FindItem** -oder **FindConversation** -Anforderung sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="3964b-104">The **SortOrder** element defines how items are sorted in a **FindItem** or **FindConversation** request.</span></span> 
  
```xml
<SortOrder>
   <FieldOrder/>
</SortOrder>
```

 <span data-ttu-id="3964b-105">**NonEmptyArrayOfFieldOrdersType**</span><span class="sxs-lookup"><span data-stu-id="3964b-105">**NonEmptyArrayOfFieldOrdersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3964b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3964b-106">Attributes and elements</span></span>

<span data-ttu-id="3964b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3964b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3964b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3964b-108">Attributes</span></span>

<span data-ttu-id="3964b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3964b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3964b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3964b-110">Child elements</span></span>

|<span data-ttu-id="3964b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3964b-111">**Element**</span></span>|<span data-ttu-id="3964b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3964b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3964b-113">FieldOrder</span><span class="sxs-lookup"><span data-stu-id="3964b-113">FieldOrder</span></span>](fieldorder.md) <br/> |<span data-ttu-id="3964b-114">Stellt ein einzelnes Feld dar, nach dem die Ergebnisse durchsucht werden und gibt die Richtung für die Sortierung an.</span><span class="sxs-lookup"><span data-stu-id="3964b-114">Represents a single field by which to sort results and indicates the direction for the sort.</span></span> <span data-ttu-id="3964b-115">Eines oder mehrere dieser Elemente können eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="3964b-115">One or more of these elements may be included.</span></span> <span data-ttu-id="3964b-116">[FieldOrder](fieldorder.md) -Elemente werden in der für die Sortierung angegebenen Reihenfolge angewendet.</span><span class="sxs-lookup"><span data-stu-id="3964b-116">[FieldOrder](fieldorder.md) elements are applied in the order specified for sorting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3964b-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3964b-117">Parent elements</span></span>

|<span data-ttu-id="3964b-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="3964b-118">**Element**</span></span>|<span data-ttu-id="3964b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3964b-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3964b-120">FindItem</span><span class="sxs-lookup"><span data-stu-id="3964b-120">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="3964b-121">Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="3964b-121">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="3964b-122">Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/FindItem`</span><span class="sxs-lookup"><span data-stu-id="3964b-122">The following is the XPath expression to this element:  `/FindItem`</span></span> <br/> |
|[<span data-ttu-id="3964b-123">FindConversation</span><span class="sxs-lookup"><span data-stu-id="3964b-123">FindConversation</span></span>](findconversation.md) <br/> |<span data-ttu-id="3964b-124">Definiert eine Anforderung zum Suchen von Unterhaltungen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="3964b-124">Defines a request to find conversations in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3964b-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="3964b-125">Text value</span></span>

<span data-ttu-id="3964b-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="3964b-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3964b-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3964b-127">Remarks</span></span>

<span data-ttu-id="3964b-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3964b-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3964b-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3964b-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3964b-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="3964b-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3964b-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3964b-131">Schema Name</span></span>  <br/> |<span data-ttu-id="3964b-132">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="3964b-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3964b-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3964b-133">Validation File</span></span>  <br/> |<span data-ttu-id="3964b-134">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3964b-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3964b-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3964b-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="3964b-136">False</span><span class="sxs-lookup"><span data-stu-id="3964b-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3964b-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3964b-137">See also</span></span>



[<span data-ttu-id="3964b-138">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3964b-138">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="3964b-139">FindConversation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3964b-139">FindConversation operation</span></span>](findconversation-operation.md)


- [<span data-ttu-id="3964b-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3964b-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

