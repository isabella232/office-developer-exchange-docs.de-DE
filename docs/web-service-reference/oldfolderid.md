---
title: OldFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OldFolderId
api_type:
- schema
ms.assetid: da554a97-ab87-4950-9fc4-26b1972381bb
description: Das OldFolderId-Element enthält den ursprünglichen Bezeichner eines Ordners, die verschoben oder kopiert wurde.
ms.openlocfilehash: ef73cad73213a1e8b5341907cd22177d8e1ba628
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830645"
---
# <a name="oldfolderid"></a><span data-ttu-id="13139-103">OldFolderId</span><span class="sxs-lookup"><span data-stu-id="13139-103">OldFolderId</span></span>

<span data-ttu-id="13139-104">Das **OldFolderId** -Element enthält den ursprünglichen Bezeichner eines Ordners, die verschoben oder kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="13139-104">The **OldFolderId** element contains the original identifier of a folder that was moved or copied.</span></span> 
  
```xml
<OldFolderId Id="" ChangeKey=""/>
```

 <span data-ttu-id="13139-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="13139-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="13139-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="13139-106">Attributes and elements</span></span>

<span data-ttu-id="13139-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="13139-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13139-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="13139-108">Attributes</span></span>

|<span data-ttu-id="13139-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="13139-109">**Attribute**</span></span>|<span data-ttu-id="13139-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13139-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="13139-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="13139-111">**Id**</span></span> <br/> |<span data-ttu-id="13139-112">Enthält eine Zeichenfolge, die einen Ordner im Exchange-Speicher identifiziert.</span><span class="sxs-lookup"><span data-stu-id="13139-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="13139-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="13139-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="13139-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="13139-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="13139-115">Enthält eine Zeichenfolge, die eine Version eines Ordners identifiziert, die von dem Id-Attribut angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="13139-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="13139-116">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="13139-116">This attribute is optional.</span></span> <span data-ttu-id="13139-117">Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Ordners verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="13139-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="13139-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="13139-118">Child elements</span></span>

<span data-ttu-id="13139-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="13139-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="13139-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="13139-120">Parent elements</span></span>

|<span data-ttu-id="13139-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="13139-121">**Element**</span></span>|<span data-ttu-id="13139-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13139-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13139-123">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="13139-123">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="13139-124">Stellt ein Ereignis in der eines Elements oder Ordners kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="13139-124">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="13139-125">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="13139-125">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="13139-126">Stellt ein Ereignis in der eines Elements oder Ordners von einem übergeordneten Ordner in einer anderen übergeordneten Ordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="13139-126">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13139-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="13139-127">Remarks</span></span>

<span data-ttu-id="13139-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="13139-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="13139-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="13139-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13139-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="13139-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="13139-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="13139-131">Schema Name</span></span>  <br/> |<span data-ttu-id="13139-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="13139-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="13139-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="13139-133">Validation File</span></span>  <br/> |<span data-ttu-id="13139-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="13139-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="13139-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="13139-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="13139-136">False</span><span class="sxs-lookup"><span data-stu-id="13139-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13139-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13139-137">See also</span></span>



[<span data-ttu-id="13139-138">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="13139-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="13139-139">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="13139-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="13139-140">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="13139-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="13139-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="13139-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

