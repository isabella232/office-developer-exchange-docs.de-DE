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
description: Das DeleteFolderField-Element stellt einen Vorgang so löschen Sie eine bestimmte Eigenschaft aus einem Ordner während eines Anrufs UpdateFolder dar.
ms.openlocfilehash: 60d4a5c19d89c109913e83fea99c2f7910566c72
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354092"
---
# <a name="deletefolderfield"></a><span data-ttu-id="6fef0-103">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="6fef0-103">DeleteFolderField</span></span>

<span data-ttu-id="6fef0-104">Das **DeleteFolderField** -Element stellt einen Vorgang so löschen Sie eine bestimmte Eigenschaft aus einem Ordner während eines Anrufs UpdateFolder dar.</span><span class="sxs-lookup"><span data-stu-id="6fef0-104">The **DeleteFolderField** element represents an operation to delete a given property from a folder during an UpdateFolder call.</span></span> 
  
- [<span data-ttu-id="6fef0-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="6fef0-105">UpdateFolder</span></span>](updatefolder.md) 
- [<span data-ttu-id="6fef0-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="6fef0-106">FolderChanges</span></span>](folderchanges.md)  
- [<span data-ttu-id="6fef0-107">FolderChange</span><span class="sxs-lookup"><span data-stu-id="6fef0-107">FolderChange</span></span>](folderchange.md)  
- [<span data-ttu-id="6fef0-108">Updates (Ordner)</span><span class="sxs-lookup"><span data-stu-id="6fef0-108">Updates (Folder)</span></span>](updates-folder.md) 
- [<span data-ttu-id="6fef0-109">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="6fef0-109">DeleteFolderField</span></span>](deletefolderfield.md)
  
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

<span data-ttu-id="6fef0-110">**DeleteFolderFieldType**</span><span class="sxs-lookup"><span data-stu-id="6fef0-110">**DeleteFolderFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6fef0-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6fef0-111">Attributes and elements</span></span>

<span data-ttu-id="6fef0-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6fef0-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6fef0-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="6fef0-113">Attributes</span></span>

<span data-ttu-id="6fef0-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="6fef0-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6fef0-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fef0-115">Child elements</span></span>

|<span data-ttu-id="6fef0-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="6fef0-116">**Element**</span></span>|<span data-ttu-id="6fef0-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6fef0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6fef0-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="6fef0-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="6fef0-119">Identifiziert die Eigenschaften von URI häufig verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6fef0-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="6fef0-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="6fef0-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="6fef0-121">Einzelne Mitglieder einer Wörterbuch-Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6fef0-121">Identifies individual members of a dictionary property.</span></span>  <br/> |
|[<span data-ttu-id="6fef0-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="6fef0-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="6fef0-123">Identifiziert extended MAPI-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6fef0-123">Identifies extended MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6fef0-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fef0-124">Parent elements</span></span>

|<span data-ttu-id="6fef0-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="6fef0-125">**Element**</span></span>|<span data-ttu-id="6fef0-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6fef0-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6fef0-127">Updates (Ordner)</span><span class="sxs-lookup"><span data-stu-id="6fef0-127">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="6fef0-128">Enthält eine Reihe von Elementen, definieren anfügen, festlegen und Löschen von Änderungen an den Eigenschaften des Ordners.</span><span class="sxs-lookup"><span data-stu-id="6fef0-128">Contains a set of elements that define append, set, and delete changes to folder properties.</span></span>  <br/> <span data-ttu-id="6fef0-129">Es folgt der XPath-Ausdruck, der dieses Element:`/UpdateFolder/FolderChanges/FolderChange[i]/Updates`</span><span class="sxs-lookup"><span data-stu-id="6fef0-129">The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange[i]/Updates`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6fef0-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6fef0-130">Remarks</span></span>

<span data-ttu-id="6fef0-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="6fef0-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6fef0-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6fef0-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fef0-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="6fef0-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6fef0-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6fef0-134">Schema Name</span></span>  <br/> |<span data-ttu-id="6fef0-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6fef0-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="6fef0-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6fef0-136">Validation File</span></span>  <br/> |<span data-ttu-id="6fef0-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6fef0-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6fef0-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6fef0-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="6fef0-139">False</span><span class="sxs-lookup"><span data-stu-id="6fef0-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6fef0-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fef0-140">See also</span></span>

- [<span data-ttu-id="6fef0-141">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6fef0-141">UpdateFolder operation</span></span>](updatefolder-operation.md)

