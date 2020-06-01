---
title: ItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemIds
api_type:
- schema
ms.assetid: 6b82122b-5544-4adf-91b7-ef2db7d5046f
description: Das itemids-Element enthält die eindeutigen Identitäten von Elementen, vorkommen und wiederkehrenden Hauptelementen, die zum Löschen, senden, abrufen, verlagern oder Kopieren von Elementen in der Exchange-Informationsspeicher verwendet werden.
ms.openlocfilehash: bbd594ce2610bd625b0e16a0383fda552ee9eb19
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460603"
---
# <a name="itemids"></a><span data-ttu-id="1dd61-103">ItemIds</span><span class="sxs-lookup"><span data-stu-id="1dd61-103">ItemIds</span></span>
  
<span data-ttu-id="1dd61-104">Das **itemids** -Element enthält die eindeutigen Identitäten von Elementen, vorkommen und wiederkehrenden Hauptelementen, die zum Löschen, senden, abrufen, verlagern oder Kopieren von Elementen in der Exchange-Informationsspeicher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1dd61-104">The **ItemIds** element contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span>
  
```xml
<ItemIds>
   <ItemId/>
   <OccurrenceItemId/>
   <RecurringMasterItemId/>
</ItemIds>
```

<span data-ttu-id="1dd61-105">**NonEmptyArrayOfBaseItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="1dd61-105">**NonEmptyArrayOfBaseItemIdsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="1dd61-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1dd61-106">Attributes and elements</span></span>

<span data-ttu-id="1dd61-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1dd61-107">The following sections describe attributes, child elements, and parent elements.</span></span> 
  
### <a name="attributes"></a><span data-ttu-id="1dd61-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1dd61-108">Attributes</span></span>

<span data-ttu-id="1dd61-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1dd61-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1dd61-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1dd61-110">Child elements</span></span>

|<span data-ttu-id="1dd61-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1dd61-111">**Element**</span></span>|<span data-ttu-id="1dd61-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1dd61-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1dd61-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="1dd61-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="1dd61-114">Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1dd61-114">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1dd61-115">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="1dd61-115">OccurrenceItemId</span></span>](occurrenceitemid.md) <br/> |<span data-ttu-id="1dd61-116">Gibt ein einzelnes Vorkommen eines wiederkehrenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="1dd61-116">Identifies a single occurrence of a recurring item.</span></span>  <br/> |
|[<span data-ttu-id="1dd61-117">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="1dd61-117">RecurringMasterItemId</span></span>](recurringmasteritemid.md) <br/> |<span data-ttu-id="1dd61-118">Identifiziert ein Serienmasterelement durch Identifizieren eines der Bezeichner des zugehörigen vorkommen Elements.</span><span class="sxs-lookup"><span data-stu-id="1dd61-118">Identifies a recurrence master item by identifying one of its related occurrence items' identifiers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1dd61-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1dd61-119">Parent elements</span></span>

|<span data-ttu-id="1dd61-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="1dd61-120">**Element**</span></span>|<span data-ttu-id="1dd61-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1dd61-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1dd61-122">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="1dd61-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="1dd61-123">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="1dd61-123">Represents a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="1dd61-124">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="1dd61-124">DeleteItem</span></span>](deleteitem.md) <br/> |<span data-ttu-id="1dd61-125">Definiert eine Anforderung zum Löschen von Elementen im Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1dd61-125">Defines a request to delete items in the Exchange store.</span></span>  <br/> <span data-ttu-id="1dd61-126">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="1dd61-126">The following is the XPath expression to this element:</span></span>  <br/>  `/DeleteItem` <br/> |
|[<span data-ttu-id="1dd61-127">SendItem</span><span class="sxs-lookup"><span data-stu-id="1dd61-127">SendItem</span></span>](senditem.md) <br/> |<span data-ttu-id="1dd61-128">Das Stammelement, das eine Anforderung zum Senden von Elementen im Exchange-Informationsspeicher definiert.</span><span class="sxs-lookup"><span data-stu-id="1dd61-128">The root element that defines a request to send items in the Exchange store.</span></span>  <br/> <span data-ttu-id="1dd61-129">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="1dd61-129">The following is the XPath expression to this element:</span></span>  <br/>  `/SendItem` <br/> |
|[<span data-ttu-id="1dd61-130">GetItem</span><span class="sxs-lookup"><span data-stu-id="1dd61-130">GetItem</span></span>](getitem.md) <br/> |<span data-ttu-id="1dd61-131">Definiert eine Anforderung zum Abrufen von Elementen aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1dd61-131">Defines a request to get items from the Exchange store.</span></span>  <br/> <span data-ttu-id="1dd61-132">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="1dd61-132">The following is the XPath expression to this element:</span></span>  <br/>  `/GetItem` <br/> |
|[<span data-ttu-id="1dd61-133">MoveItem</span><span class="sxs-lookup"><span data-stu-id="1dd61-133">MoveItem</span></span>](moveitem.md) <br/> |<span data-ttu-id="1dd61-134">Definiert eine Anforderung zum verlagern von Elementen im Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1dd61-134">Defines a request to move items in the Exchange store.</span></span>  <br/> <span data-ttu-id="1dd61-135">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="1dd61-135">The following is the XPath expression to this element:</span></span>  <br/>  `/MoveItem` <br/> |
|[<span data-ttu-id="1dd61-136">CopyItem</span><span class="sxs-lookup"><span data-stu-id="1dd61-136">CopyItem</span></span>](copyitem.md) <br/> |<span data-ttu-id="1dd61-137">Definiert eine Anforderung zum Kopieren von Elementen in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1dd61-137">Defines a request to copy items in the Exchange store.</span></span>  <br/> <span data-ttu-id="1dd61-138">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="1dd61-138">The following is the XPath expression to this element:</span></span>  <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1dd61-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1dd61-139">Remarks</span></span>

<span data-ttu-id="1dd61-140">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1dd61-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1dd61-141">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1dd61-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1dd61-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="1dd61-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1dd61-143">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1dd61-143">Schema Name</span></span>  <br/> |<span data-ttu-id="1dd61-144">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="1dd61-144">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1dd61-145">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1dd61-145">Validation File</span></span>  <br/> |<span data-ttu-id="1dd61-146">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="1dd61-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1dd61-147">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1dd61-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="1dd61-148">False</span><span class="sxs-lookup"><span data-stu-id="1dd61-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1dd61-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1dd61-149">See also</span></span>

- [<span data-ttu-id="1dd61-150">DeleteItem-Operation</span><span class="sxs-lookup"><span data-stu-id="1dd61-150">DeleteItem operation</span></span>](deleteitem-operation.md)
- [<span data-ttu-id="1dd61-151">SendItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1dd61-151">SendItem operation</span></span>](senditem-operation.md) 
- [<span data-ttu-id="1dd61-152">GetItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1dd61-152">GetItem operation</span></span>](getitem-operation.md)
- [<span data-ttu-id="1dd61-153">MoveItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1dd61-153">MoveItem operation</span></span>](moveitem-operation.md)
- [<span data-ttu-id="1dd61-154">CopyItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1dd61-154">CopyItem operation</span></span>](copyitem-operation.md)
- [<span data-ttu-id="1dd61-155">FindConversation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1dd61-155">FindConversation operation</span></span>](findconversation-operation.md)

