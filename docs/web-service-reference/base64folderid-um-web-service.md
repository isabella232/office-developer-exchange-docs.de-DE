---
title: base64FolderId (um-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- base64FolderId
api_type:
- schema
ms.assetid: 662f8f2f-49a7-4c7a-9065-98a02a49cfcd
description: Das base64FolderId-Element enthält den Bezeichner des Ordners, der als Standard-e-Mail-Ordner angegeben wird, aus dem Unified Messaging Nachrichten über das Telefon in einer Anforderung für den SetTelephoneAccessFolderEmail-Vorgang (um-Webdienst) liest.
ms.openlocfilehash: ea31c7a0f93188e563bf95c4a3e6e91f0866746c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458047"
---
# <a name="base64folderid-um-web-service"></a><span data-ttu-id="282c1-103">base64FolderId (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="282c1-103">base64FolderId (UM web service)</span></span>

<span data-ttu-id="282c1-104">Das **base64FolderId** -Element enthält den Bezeichner des Ordners, der als Standard-e-Mail-Ordner angegeben wird, aus dem Unified Messaging Nachrichten über das Telefon in einer Anforderung für den [SetTelephoneAccessFolderEmail-Vorgang (um-Webdienst)](settelephoneaccessfolderemail-operation-um-web-service.md) liest.</span><span class="sxs-lookup"><span data-stu-id="282c1-104">The **base64FolderId** element contains the identifier of the folder to specify as the default e-mail folder from which Unified Messaging reads messages over the telephone in a [SetTelephoneAccessFolderEmail operation (UM web service)](settelephoneaccessfolderemail-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="282c1-105">SetTelephoneAccessFolderEmail (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="282c1-105">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md)
  
[<span data-ttu-id="282c1-106">base64FolderId (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="282c1-106">base64FolderId (UM web service)</span></span>](base64folderid-um-web-service.md)
  
```xml
<base64FolderId/>
```

 <span data-ttu-id="282c1-107">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="282c1-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="282c1-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="282c1-108">Attributes and elements</span></span>

<span data-ttu-id="282c1-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="282c1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="282c1-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="282c1-110">Attributes</span></span>

<span data-ttu-id="282c1-111">Keine</span><span class="sxs-lookup"><span data-stu-id="282c1-111">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="282c1-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="282c1-112">Child elements</span></span>

<span data-ttu-id="282c1-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="282c1-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="282c1-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="282c1-114">Parent elements</span></span>

|<span data-ttu-id="282c1-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="282c1-115">**Element**</span></span>|<span data-ttu-id="282c1-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="282c1-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="282c1-117">SetTelephoneAccessFolderEmail (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="282c1-117">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md) <br/> |<span data-ttu-id="282c1-118">Definiert die Anforderung zum Festlegen des e-Mail-Ordners für den Telefon Zugriff.</span><span class="sxs-lookup"><span data-stu-id="282c1-118">Defines request to set the telephone access e-mail folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="282c1-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="282c1-119">Text value</span></span>

<span data-ttu-id="282c1-120">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="282c1-120">A text value is required.</span></span> <span data-ttu-id="282c1-121">Der Wert Text stellt die MAPI-ID des Ordners dar.</span><span class="sxs-lookup"><span data-stu-id="282c1-121">The text value represents the MAPI ID of the folder.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="282c1-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="282c1-122">Remarks</span></span>

<span data-ttu-id="282c1-123">Verwenden Sie den [SetTelephoneAccessFolderEmail-Vorgang (um-Webdienst)](settelephoneaccessfolderemail-operation-um-web-service.md), um den e-Mail-Ordner für den Telefon Zugriff festzulegen.</span><span class="sxs-lookup"><span data-stu-id="282c1-123">To set the telephone access e-mail folder, use the [SetTelephoneAccessFolderEmail operation (UM web service)](settelephoneaccessfolderemail-operation-um-web-service.md).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="282c1-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="282c1-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="282c1-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="282c1-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="282c1-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="282c1-126">Schema Name</span></span>  <br/> |<span data-ttu-id="282c1-127">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="282c1-127">Messages</span></span>  <br/> |
|<span data-ttu-id="282c1-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="282c1-128">Validation File</span></span>  <br/> |<span data-ttu-id="282c1-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="282c1-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="282c1-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="282c1-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="282c1-131">False</span><span class="sxs-lookup"><span data-stu-id="282c1-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="282c1-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="282c1-132">See also</span></span>



[<span data-ttu-id="282c1-133">SetTelephoneAccessFolderEmail (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="282c1-133">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md)
  
[<span data-ttu-id="282c1-134">SetTelephoneAccessFolderEmail-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="282c1-134">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>](settelephoneaccessfolderemail-operation-um-web-service.md)
  
[<span data-ttu-id="282c1-135">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="282c1-135">FindFolder operation</span></span>](findfolder-operation.md)
  
[<span data-ttu-id="282c1-136">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="282c1-136">FindItem operation</span></span>](finditem-operation.md)

