---
title: Flag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b47bc74-a60d-4308-8674-5d52444a1753
description: Das Element Flag gibt ein Flag für ein Postfach-Element an.
ms.openlocfilehash: f30f435e8f064d7165ae52de737bbd75b0546206
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758491"
---
# <a name="flag"></a><span data-ttu-id="0a59f-103">Flag</span><span class="sxs-lookup"><span data-stu-id="0a59f-103">Flag</span></span>

<span data-ttu-id="0a59f-104">Das Element **Flag** gibt ein Flag für ein Postfach-Element an.</span><span class="sxs-lookup"><span data-stu-id="0a59f-104">The **Flag** element specifies a flag on a mailbox item.</span></span> 
  
```XML
<Flag>
    <FlagStatus/>
    <StartDate/>
    <DueDate/>
    <CompleteDate/>
</Flag>
```

 <span data-ttu-id="0a59f-105">**FlagType**</span><span class="sxs-lookup"><span data-stu-id="0a59f-105">**FlagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0a59f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0a59f-106">Attributes and elements</span></span>

<span data-ttu-id="0a59f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0a59f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0a59f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0a59f-108">Attributes</span></span>

<span data-ttu-id="0a59f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0a59f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0a59f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0a59f-110">Child elements</span></span>

|<span data-ttu-id="0a59f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0a59f-111">**Element**</span></span>|<span data-ttu-id="0a59f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0a59f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0a59f-113">FlagStatus</span><span class="sxs-lookup"><span data-stu-id="0a59f-113">FlagStatus</span></span>](flagstatus.md) <br/> |<span data-ttu-id="0a59f-114">Enthält den aggregierten Kennzeichnungsstatus für Elemente im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="0a59f-114">Contains the aggregated flag status for items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="0a59f-115">StartDate</span><span class="sxs-lookup"><span data-stu-id="0a59f-115">StartDate</span></span>](startdate.md) <br/> |<span data-ttu-id="0a59f-116">Den Anfangstermin eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="0a59f-116">Represents the start date of an item.</span></span>  <br/> |
|[<span data-ttu-id="0a59f-117">DueDate</span><span class="sxs-lookup"><span data-stu-id="0a59f-117">DueDate</span></span>](duedate.md) <br/> |<span data-ttu-id="0a59f-118">Stellt das Datum an, wann ein Element fällig ist.</span><span class="sxs-lookup"><span data-stu-id="0a59f-118">Represents the date when an item is due.</span></span>  <br/> |
|[<span data-ttu-id="0a59f-119">"CompleteDate" darf</span><span class="sxs-lookup"><span data-stu-id="0a59f-119">CompleteDate</span></span>](completedate.md) <br/> |<span data-ttu-id="0a59f-120">Stellt das Datum, an dem ein Element abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="0a59f-120">Represents the date on which an item was completed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0a59f-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0a59f-121">Parent elements</span></span>

|<span data-ttu-id="0a59f-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="0a59f-122">**Element**</span></span>|<span data-ttu-id="0a59f-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0a59f-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0a59f-124">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="0a59f-124">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="0a59f-125">Enthält eine einzelne Aktion auf einem einzelnen Gespräch angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a59f-125">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="0a59f-126">Element</span><span class="sxs-lookup"><span data-stu-id="0a59f-126">Item</span></span>](item.md) <br/> |<span data-ttu-id="0a59f-127">Stellt ein generisches Element im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="0a59f-127">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a59f-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0a59f-128">Remarks</span></span>

<span data-ttu-id="0a59f-129">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0a59f-129">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0a59f-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0a59f-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0a59f-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0a59f-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a59f-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="0a59f-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0a59f-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0a59f-133">Schema Name</span></span>  <br/> |<span data-ttu-id="0a59f-134">Typschema</span><span class="sxs-lookup"><span data-stu-id="0a59f-134">Type schema</span></span>  <br/> |
|<span data-ttu-id="0a59f-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0a59f-135">Validation File</span></span>  <br/> |<span data-ttu-id="0a59f-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0a59f-136">types.xsd</span></span>  <br/> |
|<span data-ttu-id="0a59f-137">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="0a59f-137">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0a59f-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a59f-138">See also</span></span>



- [<span data-ttu-id="0a59f-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0a59f-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

