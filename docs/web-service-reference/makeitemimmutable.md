---
title: MakeItemImmutable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de1d2a60-aeeb-4625-8b11-23c42e1e7bae
description: Das MakeItemImmutable-Element gibt einen Boolean-Wert, der angibt, ob ein Element schreibgeschützt hergestellt werden soll.
ms.openlocfilehash: 63c05fd3572c7b4ab93fe098d9165a117849ef02
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830337"
---
# <a name="makeitemimmutable"></a><span data-ttu-id="2d3e3-103">MakeItemImmutable</span><span class="sxs-lookup"><span data-stu-id="2d3e3-103">MakeItemImmutable</span></span>

<span data-ttu-id="2d3e3-104">Das **MakeItemImmutable** -Element gibt einen Boolean-Wert, der angibt, ob ein Element schreibgeschützt hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d3e3-104">The **MakeItemImmutable** element specifies a Boolean value that indicates whether an item should be made read-only.</span></span> 
  
```XML
<MakeItemImmutable>true | false</MakeItemImmutable>
```

 <span data-ttu-id="2d3e3-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2d3e3-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2d3e3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2d3e3-106">Attributes and elements</span></span>

<span data-ttu-id="2d3e3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2d3e3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d3e3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2d3e3-108">Attributes</span></span>

<span data-ttu-id="2d3e3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2d3e3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2d3e3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2d3e3-110">Child elements</span></span>

<span data-ttu-id="2d3e3-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2d3e3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2d3e3-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2d3e3-112">Parent elements</span></span>

[<span data-ttu-id="2d3e3-113">UpdateItemInRecoverableItems</span><span class="sxs-lookup"><span data-stu-id="2d3e3-113">UpdateItemInRecoverableItems</span></span>](updateiteminrecoverableitems.md)
  
## <a name="text-value"></a><span data-ttu-id="2d3e3-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="2d3e3-114">Text value</span></span>

<span data-ttu-id="2d3e3-115">Der Textwert **true** für das **MakeItemImmutable** -Element gibt an, dass das Element als schreibgeschützt festgelegt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="2d3e3-115">A text value of **true** for the **MakeItemImmutable** element indicates that the item should be made read-only.</span></span> <span data-ttu-id="2d3e3-116">Der Wert **false** gibt an, dass das Element Lese-/ Schreibzugriff ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="2d3e3-116">A value of **false** indicates that the item allows read-write access.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2d3e3-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2d3e3-117">Remarks</span></span>

<span data-ttu-id="2d3e3-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2d3e3-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2d3e3-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2d3e3-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2d3e3-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2d3e3-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d3e3-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="2d3e3-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2d3e3-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2d3e3-122">Schema name</span></span>  <br/> |<span data-ttu-id="2d3e3-123">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2d3e3-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2d3e3-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2d3e3-124">Validation file</span></span>  <br/> |<span data-ttu-id="2d3e3-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2d3e3-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2d3e3-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2d3e3-126">Can be empty</span></span>  <br/> ||
   

