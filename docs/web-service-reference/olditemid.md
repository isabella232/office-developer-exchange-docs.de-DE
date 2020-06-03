---
title: OldItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OldItemId
api_type:
- schema
ms.assetid: fb57deee-9cc3-4730-9805-ff34f39e3ab7
description: Das OldItemId-Element enthält den eindeutigen Bezeichner des Elements, das kopiert oder verschoben wurde.
ms.openlocfilehash: 9fab14478ffbb2dd8ad013d59520af943584f2eb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467466"
---
# <a name="olditemid"></a><span data-ttu-id="91981-103">OldItemId</span><span class="sxs-lookup"><span data-stu-id="91981-103">OldItemId</span></span>

<span data-ttu-id="91981-104">Das **OldItemId** -Element enthält den eindeutigen Bezeichner des Elements, das kopiert oder verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="91981-104">The **OldItemId** element contains the unique identifier of the item that was copied or moved.</span></span> 
  
```xml
<OldItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="91981-105">**Itemidtype**</span><span class="sxs-lookup"><span data-stu-id="91981-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="91981-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="91981-106">Attributes and elements</span></span>

<span data-ttu-id="91981-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="91981-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91981-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="91981-108">Attributes</span></span>

|<span data-ttu-id="91981-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="91981-109">**Attribute**</span></span>|<span data-ttu-id="91981-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91981-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="91981-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="91981-111">**Id**</span></span> <br/> |<span data-ttu-id="91981-112">Enthält eine Zeichenfolge, die ein Element in der Exchange-Informationsspeicher identifiziert.</span><span class="sxs-lookup"><span data-stu-id="91981-112">Contains a string that identifies an item in the Exchange store.</span></span> <span data-ttu-id="91981-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="91981-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="91981-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="91981-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="91981-115">Enthält eine Zeichenfolge, die eine Version eines Elements identifiziert, das durch das ID-Attribut identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="91981-115">Contains a string that identifies a version of an item that is identified by the Id attribute.</span></span> <span data-ttu-id="91981-116">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="91981-116">This attribute is optional.</span></span> <span data-ttu-id="91981-117">Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Elements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="91981-117">Use this attribute to make sure that the correct version of an item is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="91981-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91981-118">Child elements</span></span>

<span data-ttu-id="91981-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="91981-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="91981-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91981-120">Parent elements</span></span>

|<span data-ttu-id="91981-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="91981-121">**Element**</span></span>|<span data-ttu-id="91981-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91981-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91981-123">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="91981-123">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="91981-124">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="91981-124">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="91981-125">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="91981-125">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="91981-126">Stellt ein Ereignis dar, in dem ein Element oder ein Ordner von einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="91981-126">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91981-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91981-127">Remarks</span></span>

<span data-ttu-id="91981-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="91981-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="91981-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="91981-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91981-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="91981-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="91981-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="91981-131">Schema Name</span></span>  <br/> |<span data-ttu-id="91981-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="91981-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="91981-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="91981-133">Validation File</span></span>  <br/> |<span data-ttu-id="91981-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="91981-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="91981-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="91981-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="91981-136">False</span><span class="sxs-lookup"><span data-stu-id="91981-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91981-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91981-137">See also</span></span>



[<span data-ttu-id="91981-138">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="91981-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="91981-139">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="91981-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="91981-140">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="91981-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="91981-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="91981-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

