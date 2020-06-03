---
title: Updates (Ordner)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Updates
api_type:
- schema
ms.assetid: b047e3a4-a5ab-4098-b7a0-273bc809e702
description: Das Updates-Element enthält eine Reihe von Elementen, die Append-, festlegen-und DELETE-Änderungen an Ordner Eigenschaften definieren.
ms.openlocfilehash: 3282171dfc188a9d4735a19a97e80fe0e2f79b89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457179"
---
# <a name="updates-folder"></a><span data-ttu-id="ba02b-103">Updates (Ordner)</span><span class="sxs-lookup"><span data-stu-id="ba02b-103">Updates (Folder)</span></span>

<span data-ttu-id="ba02b-104">Das **Updates** -Element enthält eine Reihe von Elementen, die Append-, festlegen-und DELETE-Änderungen an Ordner Eigenschaften definieren.</span><span class="sxs-lookup"><span data-stu-id="ba02b-104">The **Updates** element contains a set of elements that define append, set, and delete changes to folder properties.</span></span> 
  
- [<span data-ttu-id="ba02b-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="ba02b-105">UpdateFolder</span></span>](updatefolder.md)
  
- [<span data-ttu-id="ba02b-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="ba02b-106">FolderChanges</span></span>](folderchanges.md)
  
- [<span data-ttu-id="ba02b-107">FolderChange</span><span class="sxs-lookup"><span data-stu-id="ba02b-107">FolderChange</span></span>](folderchange.md)
  
- [<span data-ttu-id="ba02b-108">Updates (Ordner)</span><span class="sxs-lookup"><span data-stu-id="ba02b-108">Updates (Folder)</span></span>](updates-folder.md)
  
```xml
<Updates>
   <AppendToFolderField/>
   <SetFolderField/>
   <DeleteFolderField/>
</Updates>
```

<span data-ttu-id="ba02b-109">**NonEmptyArrayOfFolderChangeDescriptionsType**</span><span class="sxs-lookup"><span data-stu-id="ba02b-109">**NonEmptyArrayOfFolderChangeDescriptionsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ba02b-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ba02b-110">Attributes and elements</span></span>

<span data-ttu-id="ba02b-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ba02b-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba02b-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="ba02b-112">Attributes</span></span>

<span data-ttu-id="ba02b-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ba02b-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba02b-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba02b-114">Child elements</span></span>

|<span data-ttu-id="ba02b-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba02b-115">**Element**</span></span>|<span data-ttu-id="ba02b-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba02b-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba02b-117">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="ba02b-117">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="ba02b-118">Stellt Daten dar, die während eines [UpdateFolder-Vorgangs](updatefolder-operation.md)an eine Folder-Eigenschaft angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ba02b-118">Represents data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="ba02b-119">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="ba02b-119">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="ba02b-120">Stellt eine Aktualisierung auf eine einzelne Eigenschaft in einem Ordner in einer [UpdateFolder-Vorgang](updatefolder-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="ba02b-120">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="ba02b-121">DeleteFolderField</span><span class="sxs-lookup"><span data-stu-id="ba02b-121">DeleteFolderField</span></span>](deletefolderfield.md) <br/> |<span data-ttu-id="ba02b-122">Stellt einen Vorgang zum Löschen einer bestimmten Eigenschaft aus einem Ordner während eines [UpdateFolder-Vorgangs](updatefolder-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="ba02b-122">Represents an operation to delete a given property from a folder during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ba02b-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba02b-123">Parent elements</span></span>

|<span data-ttu-id="ba02b-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba02b-124">**Element**</span></span>|<span data-ttu-id="ba02b-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba02b-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba02b-126">FolderChange</span><span class="sxs-lookup"><span data-stu-id="ba02b-126">FolderChange</span></span>](folderchange.md) <br/> |<span data-ttu-id="ba02b-127">Stellt eine Auflistung von Änderungen dar, die für einen einzelnen Ordner ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ba02b-127">Represents a collection of changes to be performed on a single folder.</span></span>  <br/> <span data-ttu-id="ba02b-128">Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/UpdateFolder/FolderChanges/FolderChange[i]`</span><span class="sxs-lookup"><span data-stu-id="ba02b-128">The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange[i]`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba02b-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba02b-129">Remarks</span></span>

<span data-ttu-id="ba02b-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ba02b-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba02b-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ba02b-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba02b-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba02b-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ba02b-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ba02b-133">Schema Name</span></span>  <br/> |<span data-ttu-id="ba02b-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ba02b-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="ba02b-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ba02b-135">Validation File</span></span>  <br/> |<span data-ttu-id="ba02b-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ba02b-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ba02b-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ba02b-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="ba02b-138">False</span><span class="sxs-lookup"><span data-stu-id="ba02b-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba02b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba02b-139">See also</span></span>

- [<span data-ttu-id="ba02b-140">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ba02b-140">UpdateFolder operation</span></span>](updatefolder-operation.md)
- [<span data-ttu-id="ba02b-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ba02b-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

