---
title: SetTelephoneAccessFolderEmail (um-Webdienst)
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
description: Das SetTelephoneAccessFolderEmail-Element definiert eine Anforderung zum Festlegen des standardmäßigen e-Mail-Ordners, von dem Unified Messaging Nachrichten über das Telefon lesen kann.
ms.openlocfilehash: 806bdb1f0c7930a9e89555192aa32ad997716e7e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467319"
---
# <a name="settelephoneaccessfolderemail-um-web-service"></a><span data-ttu-id="37bf7-103">SetTelephoneAccessFolderEmail (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="37bf7-103">SetTelephoneAccessFolderEmail (UM web service)</span></span>

<span data-ttu-id="37bf7-104">Das **SetTelephoneAccessFolderEmail** -Element definiert eine Anforderung zum Festlegen des standardmäßigen e-Mail-Ordners, von dem Unified Messaging Nachrichten über das Telefon lesen kann.</span><span class="sxs-lookup"><span data-stu-id="37bf7-104">The **SetTelephoneAccessFolderEmail** element defines a request to set the default e-mail folder from which Unified Messaging will read messages over the telephone.</span></span> 
  
[<span data-ttu-id="37bf7-105">SetTelephoneAccessFolderEmail (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="37bf7-105">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md)
  
```xml
<SetTelephoneAccessFolderEmail>
  <base64FolderId>   </base64FolderId>
</SetTelephoneAccessFolderEmail>
```

 <span data-ttu-id="37bf7-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="37bf7-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="37bf7-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="37bf7-107">Attributes and elements</span></span>

<span data-ttu-id="37bf7-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="37bf7-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37bf7-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="37bf7-109">Attributes</span></span>

<span data-ttu-id="37bf7-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="37bf7-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="37bf7-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="37bf7-111">Child elements</span></span>

|<span data-ttu-id="37bf7-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="37bf7-112">**Element**</span></span>|<span data-ttu-id="37bf7-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37bf7-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37bf7-114">base64FolderId (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="37bf7-114">base64FolderId (UM web service)</span></span>](base64folderid-um-web-service.md) <br/> |<span data-ttu-id="37bf7-115">Der Bezeichner des e-Mail-Ordners.</span><span class="sxs-lookup"><span data-stu-id="37bf7-115">The identifier of the e-mail folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="37bf7-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="37bf7-116">Parent elements</span></span>

<span data-ttu-id="37bf7-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="37bf7-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="37bf7-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="37bf7-118">Text value</span></span>

<span data-ttu-id="37bf7-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="37bf7-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="37bf7-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="37bf7-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37bf7-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="37bf7-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="37bf7-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="37bf7-122">Schema Name</span></span>  <br/> |<span data-ttu-id="37bf7-123">Nachrichten</span><span class="sxs-lookup"><span data-stu-id="37bf7-123">Messages</span></span>  <br/> |
|<span data-ttu-id="37bf7-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="37bf7-124">Validation File</span></span>  <br/> |<span data-ttu-id="37bf7-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="37bf7-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="37bf7-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="37bf7-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="37bf7-127">False</span><span class="sxs-lookup"><span data-stu-id="37bf7-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37bf7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37bf7-128">See also</span></span>



[<span data-ttu-id="37bf7-129">SetTelephoneAccessFolderEmail-Vorgang (um-Webdienst)</span><span class="sxs-lookup"><span data-stu-id="37bf7-129">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>](settelephoneaccessfolderemail-operation-um-web-service.md)

