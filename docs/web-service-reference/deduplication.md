---
title: Deduplizierung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a38acc3d-29a8-4466-81a4-73cb30fe5e80
description: Das Element "Deduplizierung" gibt an, ob das Suchergebnis doppelte Elemente entfernen soll.
ms.openlocfilehash: c39f980658aba7036cfabb3b51af5a41005f97b6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463713"
---
# <a name="deduplication"></a><span data-ttu-id="f054e-103">Deduplizierung</span><span class="sxs-lookup"><span data-stu-id="f054e-103">Deduplication</span></span>

<span data-ttu-id="f054e-104">Das Element " **Deduplizierung** " gibt an, ob das Suchergebnis doppelte Elemente entfernen soll.</span><span class="sxs-lookup"><span data-stu-id="f054e-104">The **Deduplication** element indicates whether the search result should remove duplicate items.</span></span> 
  
```XML
<Deduplication> true | false </Deduplication>
```

<span data-ttu-id="f054e-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="f054e-105">**Boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f054e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f054e-106">Attributes and elements</span></span>

<span data-ttu-id="f054e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f054e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f054e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f054e-108">Attributes</span></span>

<span data-ttu-id="f054e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f054e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f054e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f054e-110">Child elements</span></span>

<span data-ttu-id="f054e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f054e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f054e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f054e-112">Parent elements</span></span>

<span data-ttu-id="f054e-113">[SearchMailboxes](searchmailboxes.md)  |  [SetHoldOnMailboxes](setholdonmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="f054e-113">[SearchMailboxes](searchmailboxes.md) | [SetHoldOnMailboxes](setholdonmailboxes.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="f054e-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="f054e-114">Text value</span></span>

<span data-ttu-id="f054e-115">Der Textwert **true** für das Element Deduplizierung gibt an, dass Suchergebnisse möglicherweise keine doppelten Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="f054e-115">A text value of **true** for the Deduplication element indicates that search results may not contain duplicate items.</span></span> <span data-ttu-id="f054e-116">Der Wert **false** gibt an, dass Suchergebnisse doppelte Elemente enthalten können.</span><span class="sxs-lookup"><span data-stu-id="f054e-116">A value of **false** indicates that search results may contain duplicate items.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f054e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f054e-117">Remarks</span></span>

<span data-ttu-id="f054e-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f054e-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f054e-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f054e-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f054e-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f054e-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f054e-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="f054e-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f054e-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f054e-122">Schema name</span></span>  <br/> |<span data-ttu-id="f054e-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f054e-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="f054e-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f054e-124">Validation file</span></span>  <br/> |<span data-ttu-id="f054e-125">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f054e-125">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f054e-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f054e-126">Can be empty</span></span>  <br/> |<span data-ttu-id="f054e-127">false</span><span class="sxs-lookup"><span data-stu-id="f054e-127">false</span></span>  <br/> |
   

