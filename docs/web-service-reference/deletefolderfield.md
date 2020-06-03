---
title: DeleteFolderField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolderField
api_type:
- schema
ms.assetid: f9c2187b-4c60-4358-b4b4-ede50eadae48
description: Das DeleteFolderField-Element stellt einen Vorgang zum Löschen einer bestimmten Eigenschaft aus einem Ordner während eines UpdateFolder-Aufrufs dar.
ms.openlocfilehash: a0b48b667c8c8afbd5729d5deb84359a6a6ccc25
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462157"
---
# <a name="deletefolderfield"></a><span data-ttu-id="8d3de-103">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="8d3de-103">DeleteFolderField</span></span>

<span data-ttu-id="8d3de-104">Das **DeleteFolderField** -Element stellt einen Vorgang zum Löschen einer bestimmten Eigenschaft aus einem Ordner während eines UpdateFolder-Aufrufs dar.</span><span class="sxs-lookup"><span data-stu-id="8d3de-104">The **DeleteFolderField** element represents an operation to delete a given property from a folder during an UpdateFolder call.</span></span> 
  
- [<span data-ttu-id="8d3de-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="8d3de-105">UpdateFolder</span></span>](updatefolder.md) 
- [<span data-ttu-id="8d3de-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="8d3de-106">FolderChanges</span></span>](folderchanges.md)  
- [<span data-ttu-id="8d3de-107">FolderChange</span><span class="sxs-lookup"><span data-stu-id="8d3de-107">FolderChange</span></span>](folderchange.md)  
- [<span data-ttu-id="8d3de-108">Updates (Ordner)</span><span class="sxs-lookup"><span data-stu-id="8d3de-108">Updates (Folder)</span></span>](updates-folder.md) 
- [<span data-ttu-id="8d3de-109">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="8d3de-109">DeleteFolderField</span></span>](deletefolderfield.md)
  
```xml
<DeleteFolderField>
   <FieldURI/>
</DeleteFolderField>
```

```xml
<DeleteFolderField>
   <ExtendedFieldURI/>
</DeleteFolderField>
```

```xml
<DeleteFolderField>
   <IndexedFieldURI/>
</DeleteFolderField>
```

<span data-ttu-id="8d3de-110">**DeleteFolderFieldType**</span><span class="sxs-lookup"><span data-stu-id="8d3de-110">**DeleteFolderFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="8d3de-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8d3de-111">Attributes and elements</span></span>

<span data-ttu-id="8d3de-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8d3de-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d3de-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="8d3de-113">Attributes</span></span>

<span data-ttu-id="8d3de-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="8d3de-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8d3de-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d3de-115">Child elements</span></span>

|<span data-ttu-id="8d3de-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="8d3de-116">**Element**</span></span>|<span data-ttu-id="8d3de-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d3de-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d3de-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="8d3de-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="8d3de-119">Identifiziert häufig referenzierte Eigenschaften nach URI.</span><span class="sxs-lookup"><span data-stu-id="8d3de-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="8d3de-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="8d3de-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="8d3de-121">Identifiziert einzelne Member einer Dictionary-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8d3de-121">Identifies individual members of a dictionary property.</span></span>  <br/> |
|[<span data-ttu-id="8d3de-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="8d3de-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="8d3de-123">Identifiziert erweiterte MAPI-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8d3de-123">Identifies extended MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8d3de-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d3de-124">Parent elements</span></span>

|<span data-ttu-id="8d3de-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="8d3de-125">**Element**</span></span>|<span data-ttu-id="8d3de-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d3de-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d3de-127">Updates (Ordner)</span><span class="sxs-lookup"><span data-stu-id="8d3de-127">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="8d3de-128">Enthält eine Gruppe von Elementen, die Append-, festlegen-und DELETE-Änderungen an Ordner Eigenschaften definieren.</span><span class="sxs-lookup"><span data-stu-id="8d3de-128">Contains a set of elements that define append, set, and delete changes to folder properties.</span></span>  <br/> <span data-ttu-id="8d3de-129">Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/UpdateFolder/FolderChanges/FolderChange[i]/Updates`</span><span class="sxs-lookup"><span data-stu-id="8d3de-129">The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange[i]/Updates`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d3de-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d3de-130">Remarks</span></span>

<span data-ttu-id="8d3de-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="8d3de-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8d3de-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8d3de-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d3de-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d3de-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8d3de-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8d3de-134">Schema Name</span></span>  <br/> |<span data-ttu-id="8d3de-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8d3de-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="8d3de-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8d3de-136">Validation File</span></span>  <br/> |<span data-ttu-id="8d3de-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8d3de-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8d3de-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8d3de-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="8d3de-139">False</span><span class="sxs-lookup"><span data-stu-id="8d3de-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d3de-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d3de-140">See also</span></span>

- [<span data-ttu-id="8d3de-141">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8d3de-141">UpdateFolder operation</span></span>](updatefolder-operation.md)

