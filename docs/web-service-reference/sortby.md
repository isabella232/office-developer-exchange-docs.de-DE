---
title: SortBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3dc4ab23-26b0-42b3-8930-f1c7eefecdeb
description: Das SortBy-Element enthält eine Item-Eigenschaft, die zum Sortieren des Suchergebnisses verwendet wird.
ms.openlocfilehash: cf2b1e633bc66e526028078833afade363e4c5e0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468397"
---
# <a name="sortby"></a><span data-ttu-id="66eb2-103">SortBy</span><span class="sxs-lookup"><span data-stu-id="66eb2-103">SortBy</span></span>

<span data-ttu-id="66eb2-104">Das **SortBy** -Element enthält eine Item-Eigenschaft, die zum Sortieren des Suchergebnisses verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="66eb2-104">The **SortBy** element contains an item property used for sorting the search result.</span></span> 
  
```XML
<SortBy Order="">
   <FieldURI/>
   <IndexedFieldURI/>
</SortBy>
```

 <span data-ttu-id="66eb2-105">**FieldOrderType**</span><span class="sxs-lookup"><span data-stu-id="66eb2-105">**FieldOrderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="66eb2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="66eb2-106">Attributes and elements</span></span>

<span data-ttu-id="66eb2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="66eb2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66eb2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="66eb2-108">Attributes</span></span>

|<span data-ttu-id="66eb2-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="66eb2-109">**Attribute**</span></span>|<span data-ttu-id="66eb2-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66eb2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="66eb2-111">Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="66eb2-111">Order</span></span>  <br/> |<span data-ttu-id="66eb2-112">Der Textwert des **Order** -Attributs ist die Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="66eb2-112">The text value of the **Order** attribute is the sort order.</span></span> <span data-ttu-id="66eb2-113">Der Textwert **Aufsteigend** gibt an, dass die Ergebnisse in aufsteigender Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="66eb2-113">A text value of **Ascending** indicates that the results are in ascending order.</span></span> <span data-ttu-id="66eb2-114">Der Textwert **Absteigend** gibt an, dass sich die Ergebnisse in absteigender Reihenfolge befinden.</span><span class="sxs-lookup"><span data-stu-id="66eb2-114">A text value of **Descending** indicates that the results are in descending order.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="66eb2-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66eb2-115">Child elements</span></span>

<span data-ttu-id="66eb2-116">[FieldURI](fielduri.md)  |  [IndexedFieldURI](indexedfielduri.md)</span><span class="sxs-lookup"><span data-stu-id="66eb2-116">[FieldURI](fielduri.md) | [IndexedFieldURI](indexedfielduri.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="66eb2-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66eb2-117">Parent elements</span></span>

[<span data-ttu-id="66eb2-118">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="66eb2-118">SearchMailboxes</span></span>](searchmailboxes.md)
  
## <a name="remarks"></a><span data-ttu-id="66eb2-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66eb2-119">Remarks</span></span>

<span data-ttu-id="66eb2-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="66eb2-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="66eb2-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="66eb2-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66eb2-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="66eb2-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66eb2-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="66eb2-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="66eb2-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="66eb2-124">Schema name</span></span>  <br/> |<span data-ttu-id="66eb2-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="66eb2-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="66eb2-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="66eb2-126">Validation file</span></span>  <br/> |<span data-ttu-id="66eb2-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="66eb2-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="66eb2-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="66eb2-128">Can be empty</span></span>  <br/> ||
   

