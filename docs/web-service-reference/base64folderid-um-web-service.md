---
title: base64FolderId (UM-Webdienst)
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
description: Das base64FolderId-Element enthält den Bezeichner des Ordners, der als e-Mail-Standardordner angeben aus der Unified Messaging Nachrichten über das Telefon in einer SetTelephoneAccessFolderEmail-Vorgang (UM-Webdienst) Anforderung liest.
ms.openlocfilehash: 7d710542418a717c6fcad243a22682e5840ebbd2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757430"
---
# <a name="base64folderid-um-web-service"></a><span data-ttu-id="3af97-103">base64FolderId (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="3af97-103">base64FolderId (UM web service)</span></span>

<span data-ttu-id="3af97-104">Das **base64FolderId** -Element enthält den Bezeichner des Ordners, der als e-Mail-Standardordner angeben aus der Unified Messaging Nachrichten über das Telefon in einer Anforderung [SetTelephoneAccessFolderEmail-Vorgang (UM-Webdienst)](settelephoneaccessfolderemail-operation-um-web-service.md) liest.</span><span class="sxs-lookup"><span data-stu-id="3af97-104">The **base64FolderId** element contains the identifier of the folder to specify as the default e-mail folder from which Unified Messaging reads messages over the telephone in a [SetTelephoneAccessFolderEmail operation (UM web service)](settelephoneaccessfolderemail-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="3af97-105">SetTelephoneAccessFolderEmail (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="3af97-105">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md)
  
[<span data-ttu-id="3af97-106">base64FolderId (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="3af97-106">base64FolderId (UM web service)</span></span>](base64folderid-um-web-service.md)
  
```xml
<base64FolderId/>
```

 <span data-ttu-id="3af97-107">**string**</span><span class="sxs-lookup"><span data-stu-id="3af97-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3af97-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3af97-108">Attributes and elements</span></span>

<span data-ttu-id="3af97-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3af97-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3af97-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="3af97-110">Attributes</span></span>

<span data-ttu-id="3af97-111">Keine</span><span class="sxs-lookup"><span data-stu-id="3af97-111">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3af97-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3af97-112">Child elements</span></span>

<span data-ttu-id="3af97-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="3af97-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3af97-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3af97-114">Parent elements</span></span>

|<span data-ttu-id="3af97-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="3af97-115">**Element**</span></span>|<span data-ttu-id="3af97-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3af97-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3af97-117">SetTelephoneAccessFolderEmail (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="3af97-117">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md) <br/> |<span data-ttu-id="3af97-118">Definiert die Anforderung an den Telefon Zugriff auf e-Mail-Ordner festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3af97-118">Defines request to set the telephone access e-mail folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3af97-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="3af97-119">Text value</span></span>

<span data-ttu-id="3af97-120">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3af97-120">A text value is required.</span></span> <span data-ttu-id="3af97-121">Der Textwert stellt die MAPI-ID des Ordners.</span><span class="sxs-lookup"><span data-stu-id="3af97-121">The text value represents the MAPI ID of the folder.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3af97-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3af97-122">Remarks</span></span>

<span data-ttu-id="3af97-123">Wenn den Telefon Zugriff e-Mail-Ordner festlegen möchten, verwenden Sie die [SetTelephoneAccessFolderEmail-Vorgang (UM-Webdienst)](settelephoneaccessfolderemail-operation-um-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="3af97-123">To set the telephone access e-mail folder, use the [SetTelephoneAccessFolderEmail operation (UM web service)](settelephoneaccessfolderemail-operation-um-web-service.md).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3af97-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3af97-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3af97-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="3af97-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3af97-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3af97-126">Schema Name</span></span>  <br/> |<span data-ttu-id="3af97-127">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="3af97-127">Messages</span></span>  <br/> |
|<span data-ttu-id="3af97-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3af97-128">Validation File</span></span>  <br/> |<span data-ttu-id="3af97-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3af97-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3af97-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3af97-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="3af97-131">False</span><span class="sxs-lookup"><span data-stu-id="3af97-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3af97-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3af97-132">See also</span></span>



[<span data-ttu-id="3af97-133">SetTelephoneAccessFolderEmail (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="3af97-133">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md)
  
[<span data-ttu-id="3af97-134">SetTelephoneAccessFolderEmail-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="3af97-134">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>](settelephoneaccessfolderemail-operation-um-web-service.md)
  
[<span data-ttu-id="3af97-135">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="3af97-135">FindFolder operation</span></span>](findfolder-operation.md)
  
[<span data-ttu-id="3af97-136">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3af97-136">FindItem operation</span></span>](finditem-operation.md)

