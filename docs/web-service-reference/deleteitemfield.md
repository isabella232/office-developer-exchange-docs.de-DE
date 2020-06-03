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
description: Das DeleteItemField-Element stellt einen Vorgang zum Löschen einer bestimmten Eigenschaft aus einem Element während eines UpdateItem-Aufrufs dar.
ms.openlocfilehash: e6f5ee8a1130d7c040f3ddd94021eff6d4a758b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455674"
---
# <a name="deleteitemfield"></a><span data-ttu-id="3bab5-103">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="3bab5-103">DeleteItemField</span></span>

<span data-ttu-id="3bab5-104">Das **DeleteItemField** -Element stellt einen Vorgang zum Löschen einer bestimmten Eigenschaft aus einem Element während eines UpdateItem-Aufrufs dar.</span><span class="sxs-lookup"><span data-stu-id="3bab5-104">The **DeleteItemField** element represents an operation to delete a given property from an item during an UpdateItem call.</span></span> 
 
- [<span data-ttu-id="3bab5-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="3bab5-105">UpdateItem</span></span>](updateitem.md)  
- [<span data-ttu-id="3bab5-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="3bab5-106">ItemChanges</span></span>](itemchanges.md) 
- [<span data-ttu-id="3bab5-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="3bab5-107">ItemChange</span></span>](itemchange.md) 
- [<span data-ttu-id="3bab5-108">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="3bab5-108">Updates (Item)</span></span>](updates-item.md) 
- [<span data-ttu-id="3bab5-109">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="3bab5-109">DeleteItemField</span></span>](deleteitemfield.md)
  
```xml
<DeleteItemField>
   <FieldURI/>
</DeleteItemField>
```

```xml
<DeleteItemField>
   <IndexedFieldURI/> 
</DeleteItemField>
```

```xml
<DeleteItemField>
   <ExtendedFieldURI/>
</DeleteItemField>
```

<span data-ttu-id="3bab5-110">**DeleteItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="3bab5-110">**DeleteItemFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3bab5-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3bab5-111">Attributes and elements</span></span>

<span data-ttu-id="3bab5-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3bab5-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3bab5-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="3bab5-113">Attributes</span></span>

<span data-ttu-id="3bab5-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="3bab5-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3bab5-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3bab5-115">Child elements</span></span>

|<span data-ttu-id="3bab5-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="3bab5-116">**Element**</span></span>|<span data-ttu-id="3bab5-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3bab5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3bab5-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="3bab5-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="3bab5-119">Identifiziert häufig referenzierte Eigenschaften nach URI.</span><span class="sxs-lookup"><span data-stu-id="3bab5-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="3bab5-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="3bab5-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="3bab5-121">Identifiziert einzelne Member einer Dictionary-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3bab5-121">Identifies individual members of a dictionary property.</span></span>  <br/> |
|[<span data-ttu-id="3bab5-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="3bab5-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="3bab5-123">Identifiziert erweiterte MAPI-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3bab5-123">Identifies extended MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3bab5-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3bab5-124">Parent elements</span></span>

|<span data-ttu-id="3bab5-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="3bab5-125">**Element**</span></span>|<span data-ttu-id="3bab5-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3bab5-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3bab5-127">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="3bab5-127">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="3bab5-128">Enthält eine Gruppe von Elementen, die Append-, festlegen-und DELETE-Änderungen an Elementeigenschaften definieren.</span><span class="sxs-lookup"><span data-stu-id="3bab5-128">Contains a set of elements that define append, set, and delete changes to item properties.</span></span>  <br/><br/><span data-ttu-id="3bab5-129">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="3bab5-129">The following is the XPath expression to this element:</span></span><br/>`/UpdateItem/ItemChanges/ItemChange[i]/Updates` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3bab5-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3bab5-130">Remarks</span></span>

<span data-ttu-id="3bab5-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="3bab5-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3bab5-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3bab5-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3bab5-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="3bab5-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3bab5-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3bab5-134">Schema Name</span></span>  <br/> |<span data-ttu-id="3bab5-135">Typenschema</span><span class="sxs-lookup"><span data-stu-id="3bab5-135">types schema</span></span>  <br/> |
|<span data-ttu-id="3bab5-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3bab5-136">Validation File</span></span>  <br/> |<span data-ttu-id="3bab5-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3bab5-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3bab5-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3bab5-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="3bab5-139">False</span><span class="sxs-lookup"><span data-stu-id="3bab5-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3bab5-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bab5-140">See also</span></span>

- [<span data-ttu-id="3bab5-141">UpdateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3bab5-141">UpdateItem operation</span></span>](updateitem-operation.md)

