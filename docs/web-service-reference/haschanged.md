---
title: HasChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 15ff513d-f39e-44ed-a13f-ab3f86fa37e1
description: Das HasChanged-Element gibt an, ob ein Benutzer Foto geändert wurde.
ms.openlocfilehash: b0129e3d3acb43ada16a824e3d21706999d7053c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829802"
---
# <a name="haschanged"></a><span data-ttu-id="5cb9f-103">HasChanged</span><span class="sxs-lookup"><span data-stu-id="5cb9f-103">HasChanged</span></span>

<span data-ttu-id="5cb9f-104">Das **HasChanged** -Element gibt an, ob ein Benutzer Foto geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-104">The **HasChanged** element indicates whether a user's photo has changed.</span></span> 
  
```XML
<HasChanged> true | false </HasChanged>
```

 ****
## <a name="attributes-and-elements"></a><span data-ttu-id="5cb9f-105">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5cb9f-105">Attributes and elements</span></span>

<span data-ttu-id="5cb9f-106">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5cb9f-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="5cb9f-107">Attributes</span></span>

<span data-ttu-id="5cb9f-108">Keine.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5cb9f-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5cb9f-109">Child elements</span></span>

<span data-ttu-id="5cb9f-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5cb9f-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5cb9f-111">Parent elements</span></span>

[<span data-ttu-id="5cb9f-112">GetUserPhotoResponse</span><span class="sxs-lookup"><span data-stu-id="5cb9f-112">GetUserPhotoResponse</span></span>](getuserphotoresponse.md)
  
## <a name="text-value"></a><span data-ttu-id="5cb9f-113">Textwert</span><span class="sxs-lookup"><span data-stu-id="5cb9f-113">Text value</span></span>

<span data-ttu-id="5cb9f-114">Der Textwert **true** für das **HasChanged** -Element gibt an, dass das Foto seit dem letzten Speichern geändert wurde, die es zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-114">A text value of **true** for the **HasChanged** element indicates that the photo has changed since the last time it was returned.</span></span> <span data-ttu-id="5cb9f-115">Der Wert **false** gibt an, dass das Foto nicht seit dem letzten Speichern geändert wurde, die es zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-115">A value of **false** indicates that the photo has not changed since the last time it was returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5cb9f-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5cb9f-116">Remarks</span></span>

<span data-ttu-id="5cb9f-117">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5cb9f-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5cb9f-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5cb9f-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5cb9f-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="5cb9f-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5cb9f-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5cb9f-121">Schema name</span></span>  <br/> |<span data-ttu-id="5cb9f-122">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5cb9f-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="5cb9f-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5cb9f-123">Validation file</span></span>  <br/> |<span data-ttu-id="5cb9f-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5cb9f-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5cb9f-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="5cb9f-125">Can be empty</span></span>  <br/> ||
   

