---
title: Itemids (NonEmptyArrayOfItemIdsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemIds
api_type:
- schema
ms.assetid: e895782a-74fe-4216-8ac2-c3c88c4b232d
description: Das itemids-Element enthält ein Array von Element-IDs, mit denen die Elemente identifiziert werden, die aus einem Postfach exportiert werden sollen.
ms.openlocfilehash: 16c2633528e2ecbc863cfdde645e0f431b4c4297
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468593"
---
# <a name="itemids-nonemptyarrayofitemidstype"></a><span data-ttu-id="0c0e1-103">Itemids (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="0c0e1-103">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>

<span data-ttu-id="0c0e1-104">Das **itemids** -Element enthält ein Array von Element-IDs, mit denen die Elemente identifiziert werden, die aus einem Postfach exportiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0c0e1-104">The **ItemIds** element contains an array of item identifiers that identify the items to export from a mailbox.</span></span> 
  
[<span data-ttu-id="0c0e1-105">ExportItems</span><span class="sxs-lookup"><span data-stu-id="0c0e1-105">ExportItems</span></span>](exportitems.md)
  
[<span data-ttu-id="0c0e1-106">Itemids (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="0c0e1-106">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md)
  
```XML
<ItemIds>
   <ItemId/>
</ItemIds>
```

 <span data-ttu-id="0c0e1-107">**NonEmptyArrayOfItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="0c0e1-107">**NonEmptyArrayOfItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0c0e1-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0c0e1-108">Attributes and elements</span></span>

<span data-ttu-id="0c0e1-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0c0e1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c0e1-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0c0e1-110">Attributes</span></span>

<span data-ttu-id="0c0e1-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0c0e1-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0c0e1-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c0e1-112">Child elements</span></span>

|<span data-ttu-id="0c0e1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0c0e1-113">**Element**</span></span>|<span data-ttu-id="0c0e1-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c0e1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0c0e1-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="0c0e1-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="0c0e1-116">Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="0c0e1-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0c0e1-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c0e1-117">Parent elements</span></span>

|<span data-ttu-id="0c0e1-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="0c0e1-118">**Element**</span></span>|<span data-ttu-id="0c0e1-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c0e1-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0c0e1-120">ExportItems</span><span class="sxs-lookup"><span data-stu-id="0c0e1-120">ExportItems</span></span>](exportitems.md) <br/> |<span data-ttu-id="0c0e1-121">Stellt eine Anforderung zum Exportieren von Elementen aus einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="0c0e1-121">Represents a request to export items from a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0c0e1-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="0c0e1-122">Text value</span></span>

<span data-ttu-id="0c0e1-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="0c0e1-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0c0e1-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c0e1-124">Remarks</span></span>

<span data-ttu-id="0c0e1-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0c0e1-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0c0e1-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0c0e1-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c0e1-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c0e1-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0c0e1-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0c0e1-128">Schema Name</span></span>  <br/> |<span data-ttu-id="0c0e1-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="0c0e1-129">Message schema</span></span>  <br/> |
|<span data-ttu-id="0c0e1-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0c0e1-130">Validation File</span></span>  <br/> |<span data-ttu-id="0c0e1-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0c0e1-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0c0e1-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0c0e1-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="0c0e1-133">False</span><span class="sxs-lookup"><span data-stu-id="0c0e1-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c0e1-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c0e1-134">See also</span></span>



[<span data-ttu-id="0c0e1-135">ExportItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0c0e1-135">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="0c0e1-136">UploadItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0c0e1-136">UploadItems operation</span></span>](uploaditems-operation.md)

