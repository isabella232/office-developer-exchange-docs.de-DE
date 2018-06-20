---
title: SetTelephoneAccessFolderEmail (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetTelephoneAccessFolderEmail
api_type:
- schema
ms.assetid: 90759da7-6dba-499e-b8c8-e44a016b3198
description: Das SetTelephoneAccessFolderEmail-Element definiert eine Anforderung an den e-Mail-Standardordner festlegen aus dem Unified Messaging Nachrichten über das Telefon gelesen werden.
ms.openlocfilehash: e19f151e364411717d5129cbef8c5cc097689f89
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831461"
---
# <a name="settelephoneaccessfolderemail-um-web-service"></a><span data-ttu-id="2cf01-103">SetTelephoneAccessFolderEmail (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="2cf01-103">SetTelephoneAccessFolderEmail (UM web service)</span></span>

<span data-ttu-id="2cf01-104">Das **SetTelephoneAccessFolderEmail** -Element definiert eine Anforderung an den e-Mail-Standardordner festlegen aus dem Unified Messaging Nachrichten über das Telefon gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="2cf01-104">The **SetTelephoneAccessFolderEmail** element defines a request to set the default e-mail folder from which Unified Messaging will read messages over the telephone.</span></span> 
  
[<span data-ttu-id="2cf01-105">SetTelephoneAccessFolderEmail (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="2cf01-105">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md)
  
```xml
<SetTelephoneAccessFolderEmail>
  <base64FolderId>   </base64FolderId>
</SetTelephoneAccessFolderEmail>
```

 <span data-ttu-id="2cf01-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="2cf01-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2cf01-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2cf01-107">Attributes and elements</span></span>

<span data-ttu-id="2cf01-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2cf01-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2cf01-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="2cf01-109">Attributes</span></span>

<span data-ttu-id="2cf01-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="2cf01-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2cf01-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2cf01-111">Child elements</span></span>

|<span data-ttu-id="2cf01-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="2cf01-112">**Element**</span></span>|<span data-ttu-id="2cf01-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2cf01-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2cf01-114">base64FolderId (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="2cf01-114">base64FolderId (UM web service)</span></span>](base64folderid-um-web-service.md) <br/> |<span data-ttu-id="2cf01-115">Der Bezeichner des e-Mail-Ordners.</span><span class="sxs-lookup"><span data-stu-id="2cf01-115">The identifier of the e-mail folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2cf01-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2cf01-116">Parent elements</span></span>

<span data-ttu-id="2cf01-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="2cf01-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="2cf01-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="2cf01-118">Text value</span></span>

<span data-ttu-id="2cf01-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="2cf01-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2cf01-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2cf01-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2cf01-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="2cf01-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2cf01-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2cf01-122">Schema Name</span></span>  <br/> |<span data-ttu-id="2cf01-123">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="2cf01-123">Messages</span></span>  <br/> |
|<span data-ttu-id="2cf01-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2cf01-124">Validation File</span></span>  <br/> |<span data-ttu-id="2cf01-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2cf01-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2cf01-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2cf01-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="2cf01-127">False</span><span class="sxs-lookup"><span data-stu-id="2cf01-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2cf01-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cf01-128">See also</span></span>



[<span data-ttu-id="2cf01-129">SetTelephoneAccessFolderEmail-Vorgang (UM-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="2cf01-129">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>](settelephoneaccessfolderemail-operation-um-web-service.md)

