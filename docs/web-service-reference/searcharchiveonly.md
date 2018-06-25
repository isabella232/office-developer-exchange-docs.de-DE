---
title: SearchArchiveOnly
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cce5344c-b622-44d4-bc14-a0de346c9335
description: Das SearchArchiveOnly-Element gibt an, ob nur das Archivpostfach nicht indizierbaren Elemente durchsucht wird.
ms.openlocfilehash: ac9d3262784d8052486c631ef3e99e650d4757c7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831293"
---
# <a name="searcharchiveonly"></a><span data-ttu-id="0aa3b-103">SearchArchiveOnly</span><span class="sxs-lookup"><span data-stu-id="0aa3b-103">SearchArchiveOnly</span></span>

<span data-ttu-id="0aa3b-104">Das **SearchArchiveOnly** -Element gibt an, ob nur das Archivpostfach nicht indizierbaren Elemente durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="0aa3b-104">The **SearchArchiveOnly** element indicates whether only the archive mailbox is searched for non-indexable items.</span></span> 
  
```xml
<SearchArchiveOnly>true | false</SearchArchiveOnly>
```

 <span data-ttu-id="0aa3b-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0aa3b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0aa3b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0aa3b-106">Attributes and elements</span></span>

<span data-ttu-id="0aa3b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0aa3b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0aa3b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0aa3b-108">Attributes</span></span>

<span data-ttu-id="0aa3b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0aa3b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0aa3b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0aa3b-110">Child elements</span></span>

<span data-ttu-id="0aa3b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0aa3b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0aa3b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0aa3b-112">Parent elements</span></span>

<span data-ttu-id="0aa3b-113">[GetNonIndexableItemStatistics](getnonindexableitemstatistics.md) │ [GetNonIndexableItemDetails](getnonindexableitemdetails.md)</span><span class="sxs-lookup"><span data-stu-id="0aa3b-113">[GetNonIndexableItemStatistics](getnonindexableitemstatistics.md) │ [GetNonIndexableItemDetails](getnonindexableitemdetails.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="0aa3b-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="0aa3b-114">Text value</span></span>

<span data-ttu-id="0aa3b-115">Der Textwert **true** für das **SearchArchiveOnly** -Element gibt an, dass die Suche nicht indizierbaren Element nur für das Archivpostfach ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0aa3b-115">A text value of **true** for the **SearchArchiveOnly** element indicates that non-indexable item search is only performed on the archive mailbox.</span></span> <span data-ttu-id="0aa3b-116">Der Textwert **false** gibt an, dass die Suche für das primäre Postfach und Archivpostfach ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0aa3b-116">A text value of **false** indicates that the search is performed against the primary mailbox and archive mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0aa3b-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0aa3b-117">Remarks</span></span>

<span data-ttu-id="0aa3b-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0aa3b-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0aa3b-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0aa3b-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0aa3b-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0aa3b-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0aa3b-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="0aa3b-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0aa3b-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0aa3b-122">Schema name</span></span>  <br/> |<span data-ttu-id="0aa3b-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="0aa3b-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0aa3b-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0aa3b-124">Validation file</span></span>  <br/> |<span data-ttu-id="0aa3b-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0aa3b-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0aa3b-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="0aa3b-126">Can be empty</span></span>  <br/> ||
   

