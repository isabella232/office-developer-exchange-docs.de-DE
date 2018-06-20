---
title: GetNonIndexableItemDetails
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3994c1-3bb4-4571-b026-34a6c5705410
description: Das GetNonIndexableItemDetails-Element gibt eine Anforderung zum Abrufen von Nonindexable Elementdetails.
ms.openlocfilehash: 0aeda85973aa78eff240a017db58ffb57fc0de06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758734"
---
# <a name="getnonindexableitemdetails"></a><span data-ttu-id="4d07b-103">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="4d07b-103">GetNonIndexableItemDetails</span></span>

<span data-ttu-id="4d07b-104">Das **GetNonIndexableItemDetails** -Element gibt eine Anforderung zum Abrufen von Nonindexable Elementdetails.</span><span class="sxs-lookup"><span data-stu-id="4d07b-104">The **GetNonIndexableItemDetails** element specifies a request to retrieve nonindexable item details.</span></span> 
  
```XML
<GetNonIndexableItemDetails>
    <Mailboxes/>
    <PageSize/>
    <PageItemReference/>
    <PageDirection/>
</GetNonIndexableItemDetails>
```

 <span data-ttu-id="4d07b-105">**GetNonIndexableItemDetailsType**</span><span class="sxs-lookup"><span data-stu-id="4d07b-105">**GetNonIndexableItemDetailsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4d07b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4d07b-106">Attributes and elements</span></span>

<span data-ttu-id="4d07b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4d07b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4d07b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4d07b-108">Attributes</span></span>

<span data-ttu-id="4d07b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4d07b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4d07b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4d07b-110">Child elements</span></span>

|<span data-ttu-id="4d07b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4d07b-111">**Element**</span></span>|<span data-ttu-id="4d07b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4d07b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d07b-113">Postfächer (NonEmptyArrayOfLegacyDNsType)</span><span class="sxs-lookup"><span data-stu-id="4d07b-113">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md) <br/> |<span data-ttu-id="4d07b-114">Gibt ein Array von Elementen des **Postfachs** an.</span><span class="sxs-lookup"><span data-stu-id="4d07b-114">Specifies an array of **Mailbox** elements.</span></span>  <br/> |
|[<span data-ttu-id="4d07b-115">PageSize</span><span class="sxs-lookup"><span data-stu-id="4d07b-115">PageSize</span></span>](pagesize.md) <br/> |<span data-ttu-id="4d07b-116">Enthält die Anzahl der Elemente in einer einzelnen Seite für ein Suchergebnis zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d07b-116">Contains the number of items to be returned in a single page for a search result.</span></span>  <br/> |
|[<span data-ttu-id="4d07b-117">PageItemReference</span><span class="sxs-lookup"><span data-stu-id="4d07b-117">PageItemReference</span></span>](pageitemreference.md) <br/> |<span data-ttu-id="4d07b-118">Gibt den Verweis für ein Seitenelement.</span><span class="sxs-lookup"><span data-stu-id="4d07b-118">Specifies the reference for a page item.</span></span>  <br/> |
|[<span data-ttu-id="4d07b-119">PageDirection</span><span class="sxs-lookup"><span data-stu-id="4d07b-119">PageDirection</span></span>](pagedirection.md) <br/> |<span data-ttu-id="4d07b-120">Enthält die Richtung für die Paginierung in das Suchergebnis.</span><span class="sxs-lookup"><span data-stu-id="4d07b-120">Contains the direction for pagination in the search result.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4d07b-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4d07b-121">Parent elements</span></span>

<span data-ttu-id="4d07b-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="4d07b-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4d07b-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4d07b-123">Remarks</span></span>

<span data-ttu-id="4d07b-124">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4d07b-124">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4d07b-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4d07b-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4d07b-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4d07b-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4d07b-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="4d07b-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4d07b-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4d07b-128">Schema Name</span></span>  <br/> |<span data-ttu-id="4d07b-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4d07b-129">Message schema</span></span>  <br/> |
|<span data-ttu-id="4d07b-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4d07b-130">Validation File</span></span>  <br/> |<span data-ttu-id="4d07b-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4d07b-131">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4d07b-132">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="4d07b-132">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="4d07b-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d07b-133">See also</span></span>



- [<span data-ttu-id="4d07b-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4d07b-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

