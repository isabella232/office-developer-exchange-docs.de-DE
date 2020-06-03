---
title: SearchArchiveOnly
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cce5344c-b622-44d4-bc14-a0de346c9335
description: Das SearchArchiveOnly-Element gibt an, ob nur das Archivpostfach nach nicht indizierten Elementen durchsucht wird.
ms.openlocfilehash: 9014044ed06c697cc43dd62103d7a1a907bda5a8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460498"
---
# <a name="searcharchiveonly"></a><span data-ttu-id="3c3c6-103">SearchArchiveOnly</span><span class="sxs-lookup"><span data-stu-id="3c3c6-103">SearchArchiveOnly</span></span>

<span data-ttu-id="3c3c6-104">Das **SearchArchiveOnly** -Element gibt an, ob nur das Archivpostfach nach nicht indizierten Elementen durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="3c3c6-104">The **SearchArchiveOnly** element indicates whether only the archive mailbox is searched for non-indexable items.</span></span> 
  
```xml
<SearchArchiveOnly>true | false</SearchArchiveOnly>
```

 <span data-ttu-id="3c3c6-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="3c3c6-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3c3c6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3c3c6-106">Attributes and elements</span></span>

<span data-ttu-id="3c3c6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3c3c6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c3c6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3c3c6-108">Attributes</span></span>

<span data-ttu-id="3c3c6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3c3c6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3c3c6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c3c6-110">Child elements</span></span>

<span data-ttu-id="3c3c6-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3c3c6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3c3c6-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c3c6-112">Parent elements</span></span>

<span data-ttu-id="3c3c6-113">[GetNonIndexableItemStatistics](getnonindexableitemstatistics.md) │ [GetNonIndexableItemDetails](getnonindexableitemdetails.md)</span><span class="sxs-lookup"><span data-stu-id="3c3c6-113">[GetNonIndexableItemStatistics](getnonindexableitemstatistics.md) │ [GetNonIndexableItemDetails](getnonindexableitemdetails.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="3c3c6-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="3c3c6-114">Text value</span></span>

<span data-ttu-id="3c3c6-115">Der Textwert **true** für das **SearchArchiveOnly** -Element gibt an, dass die Suche nicht indiziert Elemente nur für das Archivpostfach ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c3c6-115">A text value of **true** for the **SearchArchiveOnly** element indicates that non-indexable item search is only performed on the archive mailbox.</span></span> <span data-ttu-id="3c3c6-116">Der Textwert **false** gibt an, dass die Suche für das primäre Postfach und das Archivpostfach ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c3c6-116">A text value of **false** indicates that the search is performed against the primary mailbox and archive mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3c3c6-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c3c6-117">Remarks</span></span>

<span data-ttu-id="3c3c6-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3c3c6-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3c3c6-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3c3c6-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c3c6-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3c3c6-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c3c6-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c3c6-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3c3c6-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3c3c6-122">Schema name</span></span>  <br/> |<span data-ttu-id="3c3c6-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="3c3c6-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3c3c6-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3c3c6-124">Validation file</span></span>  <br/> |<span data-ttu-id="3c3c6-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3c3c6-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3c3c6-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="3c3c6-126">Can be empty</span></span>  <br/> ||
   

