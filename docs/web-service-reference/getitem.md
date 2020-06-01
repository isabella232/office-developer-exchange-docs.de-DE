---
title: GetItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: 769df8eb-9c72-48b5-a49f-82c6b86bc5fc
description: Das GetItem-Element definiert eine Anforderung zum Abrufen eines Elements aus einem Postfach im Exchange-Informationsspeicher.
ms.openlocfilehash: a02403ee84195a41387d5dbe1785ae6d12b47da5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458698"
---
# <a name="getitem"></a><span data-ttu-id="4ecee-103">GetItem</span><span class="sxs-lookup"><span data-stu-id="4ecee-103">GetItem</span></span>

<span data-ttu-id="4ecee-104">Das **GetItem** -Element definiert eine Anforderung zum Abrufen eines Elements aus einem Postfach im Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="4ecee-104">The **GetItem** element defines a request to get an item from a mailbox in the Exchange store.</span></span> 
  
```xml
<GetItem>
   <ItemShape/>
   <ItemIds/>
</GetItem>
```

 <span data-ttu-id="4ecee-105">**GetItemType**</span><span class="sxs-lookup"><span data-stu-id="4ecee-105">**GetItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4ecee-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4ecee-106">Attributes and elements</span></span>

<span data-ttu-id="4ecee-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4ecee-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ecee-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4ecee-108">Attributes</span></span>

<span data-ttu-id="4ecee-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4ecee-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4ecee-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ecee-110">Child elements</span></span>

|<span data-ttu-id="4ecee-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4ecee-111">**Element**</span></span>|<span data-ttu-id="4ecee-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ecee-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ecee-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="4ecee-113">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="4ecee-114">Identifiziert die Elementeigenschaften und Inhalte, die in einer **GetItem** -Antwort enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="4ecee-114">Identifies the item properties and content to include in a **GetItem** response.</span></span>  <br/> |
|[<span data-ttu-id="4ecee-115">ItemIds</span><span class="sxs-lookup"><span data-stu-id="4ecee-115">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="4ecee-116">Enthält die eindeutigen Identitäten von Elementen, vorkommen-Elementen und wiederkehrenden Gestaltungsvorlagen, die zum Abrufen von Elementen aus dem Exchange-Informationsspeicher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ecee-116">Contains the unique identities of items, occurrence items, and recurring master items that are used to get items from the Exchange store.</span></span> <span data-ttu-id="4ecee-117">Diese Elemente stellen Kontakte, Aufgaben, Nachrichten, Kalenderelemente, Besprechungsanfragen und andere gültige Elemente in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="4ecee-117">These items represent contacts, tasks, messages, calendar items, meeting requests, and other valid items in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4ecee-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ecee-118">Parent elements</span></span>

<span data-ttu-id="4ecee-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="4ecee-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4ecee-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ecee-120">Remarks</span></span>

<span data-ttu-id="4ecee-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="4ecee-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4ecee-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4ecee-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ecee-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ecee-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4ecee-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4ecee-124">Schema Name</span></span>  <br/> |<span data-ttu-id="4ecee-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4ecee-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="4ecee-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4ecee-126">Validation File</span></span>  <br/> |<span data-ttu-id="4ecee-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4ecee-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4ecee-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4ecee-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="4ecee-129">False</span><span class="sxs-lookup"><span data-stu-id="4ecee-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4ecee-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ecee-130">See also</span></span>



[<span data-ttu-id="4ecee-131">GetItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4ecee-131">GetItem operation</span></span>](getitem-operation.md)

