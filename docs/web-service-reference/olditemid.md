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
ms.openlocfilehash: ced7fc6891e0d1fde42a8cb9cad4f4e55493b5d1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830648"
---
# <a name="olditemid"></a><span data-ttu-id="4bff6-103">OldItemId</span><span class="sxs-lookup"><span data-stu-id="4bff6-103">OldItemId</span></span>

<span data-ttu-id="4bff6-104">Das **OldItemId** -Element enthält den eindeutigen Bezeichner des Elements, das kopiert oder verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="4bff6-104">The **OldItemId** element contains the unique identifier of the item that was copied or moved.</span></span> 
  
```xml
<OldItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="4bff6-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="4bff6-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4bff6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4bff6-106">Attributes and elements</span></span>

<span data-ttu-id="4bff6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4bff6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4bff6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4bff6-108">Attributes</span></span>

|<span data-ttu-id="4bff6-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4bff6-109">**Attribute**</span></span>|<span data-ttu-id="4bff6-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4bff6-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4bff6-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="4bff6-111">**Id**</span></span> <br/> |<span data-ttu-id="4bff6-112">Enthält eine Zeichenfolge zur Identifizierung ein Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="4bff6-112">Contains a string that identifies an item in the Exchange store.</span></span> <span data-ttu-id="4bff6-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4bff6-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="4bff6-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="4bff6-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="4bff6-115">Enthält eine Zeichenfolge, die eine Version eines Elements identifiziert, die von dem Id-Attribut angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4bff6-115">Contains a string that identifies a version of an item that is identified by the Id attribute.</span></span> <span data-ttu-id="4bff6-116">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="4bff6-116">This attribute is optional.</span></span> <span data-ttu-id="4bff6-117">Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Elements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4bff6-117">Use this attribute to make sure that the correct version of an item is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4bff6-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4bff6-118">Child elements</span></span>

<span data-ttu-id="4bff6-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="4bff6-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4bff6-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4bff6-120">Parent elements</span></span>

|<span data-ttu-id="4bff6-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="4bff6-121">**Element**</span></span>|<span data-ttu-id="4bff6-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4bff6-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4bff6-123">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="4bff6-123">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="4bff6-124">Stellt ein Ereignis in der eines Elements oder Ordners kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="4bff6-124">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="4bff6-125">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="4bff6-125">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="4bff6-126">Stellt ein Ereignis in der eines Elements oder Ordners von einem übergeordneten Ordner in einer anderen übergeordneten Ordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="4bff6-126">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4bff6-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4bff6-127">Remarks</span></span>

<span data-ttu-id="4bff6-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="4bff6-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4bff6-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4bff6-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4bff6-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="4bff6-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4bff6-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4bff6-131">Schema Name</span></span>  <br/> |<span data-ttu-id="4bff6-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4bff6-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="4bff6-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4bff6-133">Validation File</span></span>  <br/> |<span data-ttu-id="4bff6-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4bff6-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4bff6-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4bff6-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="4bff6-136">False</span><span class="sxs-lookup"><span data-stu-id="4bff6-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4bff6-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bff6-137">See also</span></span>



[<span data-ttu-id="4bff6-138">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="4bff6-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="4bff6-139">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4bff6-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="4bff6-140">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="4bff6-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="4bff6-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4bff6-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

