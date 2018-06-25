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
description: Das Element UploadItems stellt eine Anforderung zum Hochladen von Elementen in einem Postfach.
ms.openlocfilehash: d3cd69cdb744431daeede736c2e156c8ab92a79b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839412"
---
# <a name="uploaditems"></a><span data-ttu-id="eb413-103">UploadItems</span><span class="sxs-lookup"><span data-stu-id="eb413-103">UploadItems</span></span>

<span data-ttu-id="eb413-104">Das Element **UploadItems** stellt eine Anforderung zum Hochladen von Elementen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="eb413-104">The **UploadItems** element represents a request to upload items into a mailbox.</span></span> 
  
[<span data-ttu-id="eb413-105">UploadItems</span><span class="sxs-lookup"><span data-stu-id="eb413-105">UploadItems</span></span>](uploaditems.md)
  
```XML
<UploadItems>
   <Items/>
</UploadItems>
```

 <span data-ttu-id="eb413-106">**UploadItemsType**</span><span class="sxs-lookup"><span data-stu-id="eb413-106">**UploadItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb413-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="eb413-107">Attributes and elements</span></span>

<span data-ttu-id="eb413-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="eb413-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb413-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="eb413-109">Attributes</span></span>

<span data-ttu-id="eb413-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="eb413-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eb413-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eb413-111">Child elements</span></span>

|<span data-ttu-id="eb413-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="eb413-112">**Element**</span></span>|<span data-ttu-id="eb413-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eb413-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb413-114">Elemente (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="eb413-114">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md) <br/> |<span data-ttu-id="eb413-115">Enthält ein Array von Elementen in einem Postfach hochladen.</span><span class="sxs-lookup"><span data-stu-id="eb413-115">Contains an array of items to upload into a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="eb413-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eb413-116">Parent elements</span></span>

<span data-ttu-id="eb413-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="eb413-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="eb413-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="eb413-118">Text value</span></span>

<span data-ttu-id="eb413-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="eb413-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb413-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eb413-120">Remarks</span></span>

<span data-ttu-id="eb413-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="eb413-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb413-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="eb413-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb413-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb413-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="eb413-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="eb413-124">Schema Name</span></span>  <br/> |<span data-ttu-id="eb413-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="eb413-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="eb413-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="eb413-126">Validation File</span></span>  <br/> |<span data-ttu-id="eb413-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="eb413-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eb413-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="eb413-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="eb413-129">False</span><span class="sxs-lookup"><span data-stu-id="eb413-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb413-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb413-130">See also</span></span>



[<span data-ttu-id="eb413-131">ExportItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="eb413-131">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="eb413-132">UploadItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="eb413-132">UploadItems operation</span></span>](uploaditems-operation.md)

