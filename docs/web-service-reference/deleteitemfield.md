---
title: DeleteItemField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItemField
api_type:
- schema
ms.assetid: 3893be6a-49a7-49f6-bf53-c7f819ec3f87
description: Das DeleteItemField-Element stellt einen Vorgang zum Löschen einer bestimmten Eigenschaft aus einem Element während eines Anrufs UpdateItem dar.
ms.openlocfilehash: 2388bd10379211a31890b7c4f27920431ce444c8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757928"
---
# <a name="deleteitemfield"></a><span data-ttu-id="77860-103">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="77860-103">DeleteItemField</span></span>

<span data-ttu-id="77860-104">Das **DeleteItemField** -Element stellt einen Vorgang zum Löschen einer bestimmten Eigenschaft aus einem Element während eines Anrufs UpdateItem dar.</span><span class="sxs-lookup"><span data-stu-id="77860-104">The **DeleteItemField** element represents an operation to delete a given property from an item during an UpdateItem call.</span></span> 
 
- [<span data-ttu-id="77860-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="77860-105">UpdateItem</span></span>](updateitem.md)  
- [<span data-ttu-id="77860-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="77860-106">ItemChanges</span></span>](itemchanges.md) 
- [<span data-ttu-id="77860-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="77860-107">ItemChange</span></span>](itemchange.md) 
- [<span data-ttu-id="77860-108">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="77860-108">Updates (Item)</span></span>](updates-item.md) 
- [<span data-ttu-id="77860-109">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="77860-109">DeleteItemField</span></span>](deleteitemfield.md)
  
```xml
<DeleteItemField>
   <FieldURI/>
</DeleteItemField>
```

 <span data-ttu-id="77860-110">**DeleteItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="77860-110">**DeleteItemFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="77860-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="77860-111">Attributes and elements</span></span>

<span data-ttu-id="77860-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="77860-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="77860-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="77860-113">Attributes</span></span>

<span data-ttu-id="77860-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="77860-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="77860-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="77860-115">Child elements</span></span>

|<span data-ttu-id="77860-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="77860-116">**Element**</span></span>|<span data-ttu-id="77860-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="77860-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77860-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="77860-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="77860-119">Identifiziert die Eigenschaften von URI häufig verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="77860-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="77860-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="77860-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="77860-121">Einzelne Mitglieder einer Wörterbuch-Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="77860-121">Identifies individual members of a dictionary property.</span></span>  <br/> |
|[<span data-ttu-id="77860-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="77860-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="77860-123">Identifiziert extended MAPI-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="77860-123">Identifies extended MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="77860-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="77860-124">Parent elements</span></span>

|<span data-ttu-id="77860-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="77860-125">**Element**</span></span>|<span data-ttu-id="77860-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="77860-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77860-127">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="77860-127">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="77860-128">Enthält eine Reihe von Elementen, definieren anfügen, festlegen und Löschen von Änderungen an Elementeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="77860-128">Contains a set of elements that define append, set, and delete changes to item properties.</span></span>  <br/><br/><span data-ttu-id="77860-129">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="77860-129">The following is the XPath expression to this element:</span></span><br/>`/UpdateItem/ItemChanges/ItemChange[i]/Updates` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77860-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="77860-130">Remarks</span></span>

<span data-ttu-id="77860-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="77860-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="77860-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="77860-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77860-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="77860-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="77860-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="77860-134">Schema Name</span></span>  <br/> |<span data-ttu-id="77860-135">Typen-schema</span><span class="sxs-lookup"><span data-stu-id="77860-135">types schema</span></span>  <br/> |
|<span data-ttu-id="77860-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="77860-136">Validation File</span></span>  <br/> |<span data-ttu-id="77860-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="77860-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="77860-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="77860-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="77860-139">False</span><span class="sxs-lookup"><span data-stu-id="77860-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="77860-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77860-140">See also</span></span>

- [<span data-ttu-id="77860-141">UpdateItem Operation</span><span class="sxs-lookup"><span data-stu-id="77860-141">UpdateItem operation</span></span>](updateitem-operation.md)

