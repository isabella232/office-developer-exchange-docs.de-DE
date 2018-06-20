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
description: Das GetItem-Element definiert eine Anforderung zum Abrufen eines Elements aus einem Postfach im Exchange-Speicher.
ms.openlocfilehash: 39db141bad62c34bec5ae6a937ba94c2d1288090
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758722"
---
# <a name="getitem"></a><span data-ttu-id="dfa68-103">GetItem</span><span class="sxs-lookup"><span data-stu-id="dfa68-103">GetItem</span></span>

<span data-ttu-id="dfa68-104">Das **GetItem** -Element definiert eine Anforderung zum Abrufen eines Elements aus einem Postfach im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="dfa68-104">The **GetItem** element defines a request to get an item from a mailbox in the Exchange store.</span></span> 
  
```xml
<GetItem>
   <ItemShape/>
   <ItemIds/>
</GetItem>
```

 <span data-ttu-id="dfa68-105">**GetItemType**</span><span class="sxs-lookup"><span data-stu-id="dfa68-105">**GetItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dfa68-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dfa68-106">Attributes and elements</span></span>

<span data-ttu-id="dfa68-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dfa68-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dfa68-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dfa68-108">Attributes</span></span>

<span data-ttu-id="dfa68-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="dfa68-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dfa68-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dfa68-110">Child elements</span></span>

|<span data-ttu-id="dfa68-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="dfa68-111">**Element**</span></span>|<span data-ttu-id="dfa68-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dfa68-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dfa68-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="dfa68-113">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="dfa68-114">Identifiziert die Elementeigenschaften und den Inhalt in einer Antwort **GetItem** aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="dfa68-114">Identifies the item properties and content to include in a **GetItem** response.</span></span>  <br/> |
|[<span data-ttu-id="dfa68-115">Artikelnummern ein.</span><span class="sxs-lookup"><span data-stu-id="dfa68-115">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="dfa68-116">Enthält die eindeutigen Identitäten der Elemente, Vorkommen Elemente und master Terminserien, die zum Abrufen von Elementen aus dem Exchange-Speicher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dfa68-116">Contains the unique identities of items, occurrence items, and recurring master items that are used to get items from the Exchange store.</span></span> <span data-ttu-id="dfa68-117">Diese Elemente darstellen, Kontakte, Aufgaben, Nachrichten, Kalenderelemente, Besprechungsanfragen und anderen gültigen Elementen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="dfa68-117">These items represent contacts, tasks, messages, calendar items, meeting requests, and other valid items in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dfa68-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dfa68-118">Parent elements</span></span>

<span data-ttu-id="dfa68-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="dfa68-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dfa68-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dfa68-120">Remarks</span></span>

<span data-ttu-id="dfa68-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="dfa68-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dfa68-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="dfa68-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dfa68-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="dfa68-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dfa68-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dfa68-124">Schema Name</span></span>  <br/> |<span data-ttu-id="dfa68-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="dfa68-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="dfa68-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dfa68-126">Validation File</span></span>  <br/> |<span data-ttu-id="dfa68-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dfa68-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dfa68-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="dfa68-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="dfa68-129">False</span><span class="sxs-lookup"><span data-stu-id="dfa68-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dfa68-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfa68-130">See also</span></span>



[<span data-ttu-id="dfa68-131">GetItem Operation</span><span class="sxs-lookup"><span data-stu-id="dfa68-131">GetItem operation</span></span>](getitem-operation.md)

