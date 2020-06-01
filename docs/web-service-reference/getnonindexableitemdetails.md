---
title: GetNonIndexableItemDetails
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3994c1-3bb4-4571-b026-34a6c5705410
description: Das GetNonIndexableItemDetails-Element gibt eine Anforderung zum Abrufen von nicht indizier baren Element Details an.
ms.openlocfilehash: 1c04b4cd7a86183210be869973c9779188fa0adf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458600"
---
# <a name="getnonindexableitemdetails"></a><span data-ttu-id="e067b-103">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="e067b-103">GetNonIndexableItemDetails</span></span>

<span data-ttu-id="e067b-104">Das **GetNonIndexableItemDetails** -Element gibt eine Anforderung zum Abrufen von nicht indizier baren Element Details an.</span><span class="sxs-lookup"><span data-stu-id="e067b-104">The **GetNonIndexableItemDetails** element specifies a request to retrieve nonindexable item details.</span></span> 
  
```XML
<GetNonIndexableItemDetails>
    <Mailboxes/>
    <PageSize/>
    <PageItemReference/>
    <PageDirection/>
</GetNonIndexableItemDetails>
```

 <span data-ttu-id="e067b-105">**GetNonIndexableItemDetailsType**</span><span class="sxs-lookup"><span data-stu-id="e067b-105">**GetNonIndexableItemDetailsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e067b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e067b-106">Attributes and elements</span></span>

<span data-ttu-id="e067b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e067b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e067b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e067b-108">Attributes</span></span>

<span data-ttu-id="e067b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e067b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e067b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e067b-110">Child elements</span></span>

|<span data-ttu-id="e067b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e067b-111">**Element**</span></span>|<span data-ttu-id="e067b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e067b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e067b-113">Postfächer (NonEmptyArrayOfLegacyDNsType)</span><span class="sxs-lookup"><span data-stu-id="e067b-113">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md) <br/> |<span data-ttu-id="e067b-114">Gibt ein Array von **Post Fach** Elementen an.</span><span class="sxs-lookup"><span data-stu-id="e067b-114">Specifies an array of **Mailbox** elements.</span></span>  <br/> |
|[<span data-ttu-id="e067b-115">PageSize</span><span class="sxs-lookup"><span data-stu-id="e067b-115">PageSize</span></span>](pagesize.md) <br/> |<span data-ttu-id="e067b-116">Enthält die Anzahl der Elemente, die auf einer einzelnen Seite für ein Suchergebnis zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e067b-116">Contains the number of items to be returned in a single page for a search result.</span></span>  <br/> |
|[<span data-ttu-id="e067b-117">PageItemReference</span><span class="sxs-lookup"><span data-stu-id="e067b-117">PageItemReference</span></span>](pageitemreference.md) <br/> |<span data-ttu-id="e067b-118">Gibt den Verweis für ein Seitenelement an.</span><span class="sxs-lookup"><span data-stu-id="e067b-118">Specifies the reference for a page item.</span></span>  <br/> |
|[<span data-ttu-id="e067b-119">PageDirection</span><span class="sxs-lookup"><span data-stu-id="e067b-119">PageDirection</span></span>](pagedirection.md) <br/> |<span data-ttu-id="e067b-120">Enthält die Richtung für die Paginierung im Suchergebnis.</span><span class="sxs-lookup"><span data-stu-id="e067b-120">Contains the direction for pagination in the search result.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e067b-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e067b-121">Parent elements</span></span>

<span data-ttu-id="e067b-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="e067b-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e067b-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e067b-123">Remarks</span></span>

<span data-ttu-id="e067b-124">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e067b-124">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e067b-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e067b-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e067b-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e067b-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e067b-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="e067b-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e067b-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e067b-128">Schema Name</span></span>  <br/> |<span data-ttu-id="e067b-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="e067b-129">Message schema</span></span>  <br/> |
|<span data-ttu-id="e067b-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e067b-130">Validation File</span></span>  <br/> |<span data-ttu-id="e067b-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e067b-131">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e067b-132">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e067b-132">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e067b-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e067b-133">See also</span></span>



- [<span data-ttu-id="e067b-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e067b-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

