---
title: ExportItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExportItems
api_type:
- schema
ms.assetid: bbbc56e4-8cc1-43ae-b70a-9a8d6bb0f399
description: Das Export Items-Element stellt eine Anforderung zum Exportieren von Elementen aus einem Postfach dar.
ms.openlocfilehash: 6e4996f62ea5051e6dc235ee7255057f16b3855b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457270"
---
# <a name="exportitems"></a><span data-ttu-id="83173-103">ExportItems</span><span class="sxs-lookup"><span data-stu-id="83173-103">ExportItems</span></span>

<span data-ttu-id="83173-104">Das **Export Items** -Element stellt eine Anforderung zum Exportieren von Elementen aus einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="83173-104">The **ExportItems** element represents a request to export items from a mailbox.</span></span> 
  
[<span data-ttu-id="83173-105">ExportItems</span><span class="sxs-lookup"><span data-stu-id="83173-105">ExportItems</span></span>](exportitems.md)
  
```XML
<ExportItems>
   <ItemIds/>
</ExportItems>
```

 <span data-ttu-id="83173-106">**ExportItemsType**</span><span class="sxs-lookup"><span data-stu-id="83173-106">**ExportItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83173-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="83173-107">Attributes and elements</span></span>

<span data-ttu-id="83173-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="83173-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83173-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="83173-109">Attributes</span></span>

<span data-ttu-id="83173-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="83173-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83173-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83173-111">Child elements</span></span>

|<span data-ttu-id="83173-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="83173-112">**Element**</span></span>|<span data-ttu-id="83173-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="83173-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83173-114">Itemids (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="83173-114">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md) <br/> |<span data-ttu-id="83173-115">Enthält ein Array von Element-IDs, mit denen die Elemente identifiziert werden, die aus einem Postfach exportiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="83173-115">Contains an array of item identifiers that identify the items to export from a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="83173-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83173-116">Parent elements</span></span>

<span data-ttu-id="83173-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="83173-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="83173-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="83173-118">Text value</span></span>

<span data-ttu-id="83173-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="83173-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="83173-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83173-120">Remarks</span></span>

<span data-ttu-id="83173-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="83173-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83173-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="83173-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83173-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="83173-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="83173-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="83173-124">Schema Name</span></span>  <br/> |<span data-ttu-id="83173-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="83173-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="83173-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="83173-126">Validation File</span></span>  <br/> |<span data-ttu-id="83173-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="83173-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="83173-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="83173-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="83173-129">False</span><span class="sxs-lookup"><span data-stu-id="83173-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83173-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83173-130">See also</span></span>



[<span data-ttu-id="83173-131">ExportItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="83173-131">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="83173-132">UploadItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="83173-132">UploadItems operation</span></span>](uploaditems-operation.md)

