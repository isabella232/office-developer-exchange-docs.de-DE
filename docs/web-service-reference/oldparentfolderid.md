---
title: OldParentFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OldParentFolderId
api_type:
- schema
ms.assetid: da1b8c88-c650-455d-b749-0cd160b012d8
description: Das OldParentFolderId-Element enthält den Bezeichner des übergeordneten Ordners eines Elements oder Ordners, das kopiert oder verschoben wurde.
ms.openlocfilehash: ad787e95f95b551393878b15783461d93ac08481
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467228"
---
# <a name="oldparentfolderid"></a><span data-ttu-id="66d15-103">OldParentFolderId</span><span class="sxs-lookup"><span data-stu-id="66d15-103">OldParentFolderId</span></span>

<span data-ttu-id="66d15-104">Das **OldParentFolderId** -Element enthält den Bezeichner des übergeordneten Ordners eines Elements oder Ordners, das kopiert oder verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="66d15-104">The **OldParentFolderId** element contains the identifier of the parent folder of an item or folder that was copied or moved.</span></span> 
  
```xml
<OldParentFolderId Id="" ChangeKey=""/>
```

 <span data-ttu-id="66d15-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="66d15-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="66d15-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="66d15-106">Attributes and elements</span></span>

<span data-ttu-id="66d15-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="66d15-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66d15-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="66d15-108">Attributes</span></span>

|<span data-ttu-id="66d15-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="66d15-109">**Attribute**</span></span>|<span data-ttu-id="66d15-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66d15-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="66d15-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="66d15-111">**Id**</span></span> <br/> |<span data-ttu-id="66d15-112">Enthält eine Zeichenfolge, die einen Ordner im Exchange-Informationsspeicher identifiziert.</span><span class="sxs-lookup"><span data-stu-id="66d15-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="66d15-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="66d15-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="66d15-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="66d15-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="66d15-115">Enthält eine Zeichenfolge, die eine Version eines Ordners identifiziert, die durch das ID-Attribut identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="66d15-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="66d15-116">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="66d15-116">This attribute is optional.</span></span> <span data-ttu-id="66d15-117">Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Ordners verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="66d15-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="66d15-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66d15-118">Child elements</span></span>

<span data-ttu-id="66d15-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="66d15-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="66d15-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66d15-120">Parent elements</span></span>

|<span data-ttu-id="66d15-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="66d15-121">**Element**</span></span>|<span data-ttu-id="66d15-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66d15-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66d15-123">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="66d15-123">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="66d15-124">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="66d15-124">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="66d15-125">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="66d15-125">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="66d15-126">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner von einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="66d15-126">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66d15-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66d15-127">Remarks</span></span>

<span data-ttu-id="66d15-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="66d15-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66d15-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="66d15-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66d15-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="66d15-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="66d15-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="66d15-131">Schema Name</span></span>  <br/> |<span data-ttu-id="66d15-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="66d15-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="66d15-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="66d15-133">Validation File</span></span>  <br/> |<span data-ttu-id="66d15-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="66d15-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="66d15-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="66d15-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="66d15-136">False</span><span class="sxs-lookup"><span data-stu-id="66d15-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="66d15-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66d15-137">See also</span></span>



[<span data-ttu-id="66d15-138">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="66d15-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="66d15-139">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="66d15-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="66d15-140">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="66d15-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="66d15-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="66d15-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

