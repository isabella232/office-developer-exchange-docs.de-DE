---
title: UploadItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UploadItems
api_type:
- schema
ms.assetid: fd2b9545-7213-4427-95ae-71a155b75971
description: Das UploadItems-Element stellt eine Anforderung zum Hochladen von Elementen in ein Postfach dar.
ms.openlocfilehash: 8fdb7253926e030085374b650e792349e598ee4a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468824"
---
# <a name="uploaditems"></a><span data-ttu-id="5998a-103">UploadItems</span><span class="sxs-lookup"><span data-stu-id="5998a-103">UploadItems</span></span>

<span data-ttu-id="5998a-104">Das **UploadItems** -Element stellt eine Anforderung zum Hochladen von Elementen in ein Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="5998a-104">The **UploadItems** element represents a request to upload items into a mailbox.</span></span> 
  
[<span data-ttu-id="5998a-105">UploadItems</span><span class="sxs-lookup"><span data-stu-id="5998a-105">UploadItems</span></span>](uploaditems.md)
  
```XML
<UploadItems>
   <Items/>
</UploadItems>
```

 <span data-ttu-id="5998a-106">**UploadItemsType**</span><span class="sxs-lookup"><span data-stu-id="5998a-106">**UploadItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5998a-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5998a-107">Attributes and elements</span></span>

<span data-ttu-id="5998a-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5998a-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5998a-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="5998a-109">Attributes</span></span>

<span data-ttu-id="5998a-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="5998a-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5998a-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5998a-111">Child elements</span></span>

|<span data-ttu-id="5998a-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="5998a-112">**Element**</span></span>|<span data-ttu-id="5998a-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5998a-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5998a-114">Elemente (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="5998a-114">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md) <br/> |<span data-ttu-id="5998a-115">Enthält ein Array von Elementen, die in ein Postfach hochgeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5998a-115">Contains an array of items to upload into a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5998a-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5998a-116">Parent elements</span></span>

<span data-ttu-id="5998a-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="5998a-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="5998a-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="5998a-118">Text value</span></span>

<span data-ttu-id="5998a-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="5998a-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5998a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5998a-120">Remarks</span></span>

<span data-ttu-id="5998a-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5998a-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5998a-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5998a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5998a-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="5998a-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5998a-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5998a-124">Schema Name</span></span>  <br/> |<span data-ttu-id="5998a-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="5998a-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="5998a-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5998a-126">Validation File</span></span>  <br/> |<span data-ttu-id="5998a-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="5998a-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5998a-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5998a-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="5998a-129">False</span><span class="sxs-lookup"><span data-stu-id="5998a-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5998a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5998a-130">See also</span></span>



[<span data-ttu-id="5998a-131">ExportItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5998a-131">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="5998a-132">UploadItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5998a-132">UploadItems operation</span></span>](uploaditems-operation.md)

