---
title: IncludeNonIndexableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: af7f202b-2889-447e-bdeb-aaad18ce6b46
description: Das IncludeNonIndexableItems-Element enthält einen booleschen Wert, um anzugeben, ob Elemente enthalten, die nicht indiziert werden kann.
ms.openlocfilehash: ae91a3c6db82aea1d45940603d0ff2064d29f43f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829904"
---
# <a name="includenonindexableitems"></a><span data-ttu-id="3d122-103">IncludeNonIndexableItems</span><span class="sxs-lookup"><span data-stu-id="3d122-103">IncludeNonIndexableItems</span></span>

<span data-ttu-id="3d122-104">Das **IncludeNonIndexableItems** -Element enthält einen **booleschen** Wert, um anzugeben, ob Elemente enthalten, die nicht indiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3d122-104">The **IncludeNonIndexableItems** element contains a **Boolean** value to indicate whether to include items that cannot be indexed.</span></span> 
  
```XML
<IncludeNonIndexableItems>true | false</IncludeNonIndexableItems>
```

 <span data-ttu-id="3d122-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3d122-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3d122-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3d122-106">Attributes and elements</span></span>

<span data-ttu-id="3d122-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3d122-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3d122-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3d122-108">Attributes</span></span>

<span data-ttu-id="3d122-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3d122-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3d122-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3d122-110">Child elements</span></span>

<span data-ttu-id="3d122-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3d122-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3d122-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3d122-112">Parent elements</span></span>

[<span data-ttu-id="3d122-113">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="3d122-113">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="3d122-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="3d122-114">Text value</span></span>

<span data-ttu-id="3d122-115">Der Textwert **true** für das **IncludeNonIndexableItems** -Element gibt an, dass Elemente, die nicht indiziert werden in Postfach Haltestatus enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="3d122-115">A text value of **true** for the **IncludeNonIndexableItems** element indicates that items that cannot be indexed are included with mailbox holds.</span></span> <span data-ttu-id="3d122-116">Der Wert **false** gibt an, dass die Elemente, die nicht indiziert werden nicht im Postfach Haltestatus enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="3d122-116">A value of **false** indicates that the items that cannot be indexed are not included in mailbox holds.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3d122-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3d122-117">Remarks</span></span>

<span data-ttu-id="3d122-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3d122-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3d122-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3d122-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3d122-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3d122-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3d122-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="3d122-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3d122-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3d122-122">Schema name</span></span>  <br/> |<span data-ttu-id="3d122-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="3d122-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3d122-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3d122-124">Validation file</span></span>  <br/> |<span data-ttu-id="3d122-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3d122-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3d122-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="3d122-126">Can be empty</span></span>  <br/> |<span data-ttu-id="3d122-127">false</span><span class="sxs-lookup"><span data-stu-id="3d122-127">false</span></span>  <br/> |
   

