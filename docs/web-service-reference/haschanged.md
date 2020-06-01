---
title: HasChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 15ff513d-f39e-44ed-a13f-ab3f86fa37e1
description: Das hasChanged-Element gibt an, ob das Foto eines Benutzers geändert wurde.
ms.openlocfilehash: d777220f55d33cde548d8257cf249b57481a43f8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462787"
---
# <a name="haschanged"></a><span data-ttu-id="f1454-103">HasChanged</span><span class="sxs-lookup"><span data-stu-id="f1454-103">HasChanged</span></span>

<span data-ttu-id="f1454-104">Das **hasChanged** -Element gibt an, ob das Foto eines Benutzers geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="f1454-104">The **HasChanged** element indicates whether a user's photo has changed.</span></span> 
  
```XML
<HasChanged> true | false </HasChanged>
```

 ****
## <a name="attributes-and-elements"></a><span data-ttu-id="f1454-105">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f1454-105">Attributes and elements</span></span>

<span data-ttu-id="f1454-106">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f1454-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1454-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="f1454-107">Attributes</span></span>

<span data-ttu-id="f1454-108">Keine.</span><span class="sxs-lookup"><span data-stu-id="f1454-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f1454-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f1454-109">Child elements</span></span>

<span data-ttu-id="f1454-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="f1454-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f1454-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f1454-111">Parent elements</span></span>

[<span data-ttu-id="f1454-112">GetUserPhotoResponse</span><span class="sxs-lookup"><span data-stu-id="f1454-112">GetUserPhotoResponse</span></span>](getuserphotoresponse.md)
  
## <a name="text-value"></a><span data-ttu-id="f1454-113">Textwert</span><span class="sxs-lookup"><span data-stu-id="f1454-113">Text value</span></span>

<span data-ttu-id="f1454-114">Der Textwert **true** für das **hasChanged** -Element gibt an, dass das Foto seit der letzten Rückgabe geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="f1454-114">A text value of **true** for the **HasChanged** element indicates that the photo has changed since the last time it was returned.</span></span> <span data-ttu-id="f1454-115">Der Wert **false** gibt an, dass das Foto seit der letzten Rückgabe nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="f1454-115">A value of **false** indicates that the photo has not changed since the last time it was returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f1454-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1454-116">Remarks</span></span>

<span data-ttu-id="f1454-117">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f1454-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f1454-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f1454-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f1454-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f1454-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1454-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1454-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f1454-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f1454-121">Schema name</span></span>  <br/> |<span data-ttu-id="f1454-122">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f1454-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="f1454-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f1454-123">Validation file</span></span>  <br/> |<span data-ttu-id="f1454-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f1454-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f1454-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f1454-125">Can be empty</span></span>  <br/> ||
   

