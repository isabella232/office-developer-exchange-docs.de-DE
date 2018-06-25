---
title: ItemClasses (ArrayOfItemClassType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 971784d1-6860-4833-bb26-0e930fa11c21
description: Das ItemClasses-Element enthält eine Liste der Artikelklassen, die die Element-Klassen der Unterhaltungselemente im aktuellen Ordner darstellt.
ms.openlocfilehash: 62ea5b624025b3f012249afd1763e2b393ef5caa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830150"
---
# <a name="itemclasses-arrayofitemclasstype"></a><span data-ttu-id="a7de8-103">ItemClasses (ArrayOfItemClassType)</span><span class="sxs-lookup"><span data-stu-id="a7de8-103">ItemClasses (ArrayOfItemClassType)</span></span>

<span data-ttu-id="a7de8-104">Das **ItemClasses** -Element enthält eine Liste der Artikelklassen, die die Element-Klassen der Unterhaltungselemente im aktuellen Ordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="a7de8-104">The **ItemClasses** element contains a list of item classes that represents all the item classes of the conversation items in the current folder.</span></span> 
  
[<span data-ttu-id="a7de8-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="a7de8-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="a7de8-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="a7de8-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="a7de8-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="a7de8-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="a7de8-108">ItemClasses (ArrayOfItemClassType)</span><span class="sxs-lookup"><span data-stu-id="a7de8-108">ItemClasses (ArrayOfItemClassType)</span></span>](itemclasses-arrayofitemclasstype.md)
  
```XML
<ItemClasses>
    <String/>
</ItemClasses>
```

 <span data-ttu-id="a7de8-109">**ArrayOfItemClassType**</span><span class="sxs-lookup"><span data-stu-id="a7de8-109">**ArrayOfItemClassType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a7de8-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a7de8-110">Attributes and elements</span></span>

<span data-ttu-id="a7de8-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a7de8-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a7de8-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="a7de8-112">Attributes</span></span>

<span data-ttu-id="a7de8-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a7de8-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a7de8-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7de8-114">Child elements</span></span>

|<span data-ttu-id="a7de8-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="a7de8-115">**Element**</span></span>|<span data-ttu-id="a7de8-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7de8-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7de8-117">ItemClass</span><span class="sxs-lookup"><span data-stu-id="a7de8-117">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="a7de8-118">Die Nachrichtenklasse eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="a7de8-118">Represents the message class of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a7de8-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7de8-119">Parent elements</span></span>

|<span data-ttu-id="a7de8-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="a7de8-120">**Element**</span></span>|<span data-ttu-id="a7de8-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7de8-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7de8-122">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="a7de8-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="a7de8-123">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="a7de8-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a7de8-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="a7de8-124">Text value</span></span>

<span data-ttu-id="a7de8-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="a7de8-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a7de8-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a7de8-126">Remarks</span></span>

<span data-ttu-id="a7de8-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a7de8-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a7de8-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a7de8-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7de8-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7de8-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a7de8-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a7de8-130">Schema name</span></span>  <br/> |<span data-ttu-id="a7de8-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a7de8-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="a7de8-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a7de8-132">Validation file</span></span>  <br/> |<span data-ttu-id="a7de8-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a7de8-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a7de8-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a7de8-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="a7de8-135">False</span><span class="sxs-lookup"><span data-stu-id="a7de8-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a7de8-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7de8-136">See also</span></span>



[<span data-ttu-id="a7de8-137">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="a7de8-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="a7de8-138">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a7de8-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="a7de8-139">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="a7de8-139">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

