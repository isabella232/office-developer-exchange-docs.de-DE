---
title: SortBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3dc4ab23-26b0-42b3-8930-f1c7eefecdeb
description: Das SortBy-Element enthält eine Item-Eigenschaft für die Sortierung der Suchergebnisses verwendet.
ms.openlocfilehash: 357958e393ba9331d23ee48661f21e2afe00cf01
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831518"
---
# <a name="sortby"></a><span data-ttu-id="cd7dd-103">SortBy</span><span class="sxs-lookup"><span data-stu-id="cd7dd-103">SortBy</span></span>

<span data-ttu-id="cd7dd-104">Das **SortBy** -Element enthält eine Item-Eigenschaft für die Sortierung der Suchergebnisses verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd7dd-104">The **SortBy** element contains an item property used for sorting the search result.</span></span> 
  
```XML
<SortBy Order="">
   <FieldURI/>
   <IndexedFieldURI/>
</SortBy>
```

 <span data-ttu-id="cd7dd-105">**FieldOrderType**</span><span class="sxs-lookup"><span data-stu-id="cd7dd-105">**FieldOrderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cd7dd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cd7dd-106">Attributes and elements</span></span>

<span data-ttu-id="cd7dd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cd7dd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd7dd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cd7dd-108">Attributes</span></span>

|<span data-ttu-id="cd7dd-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="cd7dd-109">**Attribute**</span></span>|<span data-ttu-id="cd7dd-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cd7dd-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd7dd-111">Order</span><span class="sxs-lookup"><span data-stu-id="cd7dd-111">Order</span></span>  <br/> |<span data-ttu-id="cd7dd-112">Der Textwert der **Reihenfolge** -Attribut ist die Sortierreihenfolge an.</span><span class="sxs-lookup"><span data-stu-id="cd7dd-112">The text value of the **Order** attribute is the sort order.</span></span> <span data-ttu-id="cd7dd-113">Ein Textwert der **Aufsteigend** gibt an, dass die Ergebnisse werden in aufsteigender Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="cd7dd-113">A text value of **Ascending** indicates that the results are in ascending order.</span></span> <span data-ttu-id="cd7dd-114">Der Textwert **Absteigend** gibt an, dass die Ergebnisse in absteigender Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="cd7dd-114">A text value of **Descending** indicates that the results are in descending order.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cd7dd-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cd7dd-115">Child elements</span></span>

<span data-ttu-id="cd7dd-116">[FieldURI](fielduri.md) | [IndexedFieldURI](indexedfielduri.md)</span><span class="sxs-lookup"><span data-stu-id="cd7dd-116">[FieldURI](fielduri.md) | [IndexedFieldURI](indexedfielduri.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cd7dd-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cd7dd-117">Parent elements</span></span>

[<span data-ttu-id="cd7dd-118">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="cd7dd-118">SearchMailboxes</span></span>](searchmailboxes.md)
  
## <a name="remarks"></a><span data-ttu-id="cd7dd-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cd7dd-119">Remarks</span></span>

<span data-ttu-id="cd7dd-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="cd7dd-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="cd7dd-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="cd7dd-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd7dd-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="cd7dd-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd7dd-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd7dd-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cd7dd-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cd7dd-124">Schema name</span></span>  <br/> |<span data-ttu-id="cd7dd-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="cd7dd-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cd7dd-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cd7dd-126">Validation file</span></span>  <br/> |<span data-ttu-id="cd7dd-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cd7dd-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cd7dd-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="cd7dd-128">Can be empty</span></span>  <br/> ||
   

