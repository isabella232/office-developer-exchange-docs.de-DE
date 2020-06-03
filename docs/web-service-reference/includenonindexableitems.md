---
title: IncludeNonIndexableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: af7f202b-2889-447e-bdeb-aaad18ce6b46
description: Das IncludeNonIndexableItems-Element enthält einen booleschen Wert, um anzugeben, ob Elemente eingeschlossen werden sollen, die nicht indiziert werden können.
ms.openlocfilehash: eab559e938f0b949d79626ae5bf61b3d4a838924
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460624"
---
# <a name="includenonindexableitems"></a><span data-ttu-id="cbd79-103">IncludeNonIndexableItems</span><span class="sxs-lookup"><span data-stu-id="cbd79-103">IncludeNonIndexableItems</span></span>

<span data-ttu-id="cbd79-104">Das **IncludeNonIndexableItems** -Element enthält einen **booleschen** Wert, um anzugeben, ob Elemente eingeschlossen werden sollen, die nicht indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="cbd79-104">The **IncludeNonIndexableItems** element contains a **Boolean** value to indicate whether to include items that cannot be indexed.</span></span> 
  
```XML
<IncludeNonIndexableItems>true | false</IncludeNonIndexableItems>
```

 <span data-ttu-id="cbd79-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="cbd79-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cbd79-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cbd79-106">Attributes and elements</span></span>

<span data-ttu-id="cbd79-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cbd79-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cbd79-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cbd79-108">Attributes</span></span>

<span data-ttu-id="cbd79-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="cbd79-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cbd79-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cbd79-110">Child elements</span></span>

<span data-ttu-id="cbd79-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="cbd79-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cbd79-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cbd79-112">Parent elements</span></span>

[<span data-ttu-id="cbd79-113">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="cbd79-113">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="cbd79-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="cbd79-114">Text value</span></span>

<span data-ttu-id="cbd79-115">Der Textwert **true** für das **IncludeNonIndexableItems** -Element gibt an, dass Elemente, die nicht indiziert werden können, in Postfach-Haltebereichen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cbd79-115">A text value of **true** for the **IncludeNonIndexableItems** element indicates that items that cannot be indexed are included with mailbox holds.</span></span> <span data-ttu-id="cbd79-116">Der Wert **false** gibt an, dass die Elemente, die nicht indiziert werden können, nicht in die Postfachaufbewahrung eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="cbd79-116">A value of **false** indicates that the items that cannot be indexed are not included in mailbox holds.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cbd79-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbd79-117">Remarks</span></span>

<span data-ttu-id="cbd79-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="cbd79-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="cbd79-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="cbd79-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cbd79-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="cbd79-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cbd79-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="cbd79-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cbd79-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cbd79-122">Schema name</span></span>  <br/> |<span data-ttu-id="cbd79-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="cbd79-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cbd79-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cbd79-124">Validation file</span></span>  <br/> |<span data-ttu-id="cbd79-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cbd79-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cbd79-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="cbd79-126">Can be empty</span></span>  <br/> |<span data-ttu-id="cbd79-127">False</span><span class="sxs-lookup"><span data-stu-id="cbd79-127">false</span></span>  <br/> |
   

