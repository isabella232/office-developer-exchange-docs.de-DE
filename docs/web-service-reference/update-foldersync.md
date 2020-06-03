---
title: Update (FolderSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Update
api_type:
- schema
ms.assetid: 47ed8edb-2a94-471b-b965-93f91456252e
description: Das Update-Element identifiziert einen einzelnen Ordner, der im lokalen Clientspeicher aktualisiert werden soll.
ms.openlocfilehash: 5c1b5b1fd87e4651125293eac431c56f732c6c02
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467137"
---
# <a name="update-foldersync"></a><span data-ttu-id="abd40-103">Update (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="abd40-103">Update (FolderSync)</span></span>

<span data-ttu-id="abd40-104">Das **Update** -Element identifiziert einen einzelnen Ordner, der im lokalen Clientspeicher aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="abd40-104">The **Update** element identifies a single folder to update in the local client store.</span></span> 
  
- [<span data-ttu-id="abd40-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="abd40-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md) 
- [<span data-ttu-id="abd40-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="abd40-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="abd40-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="abd40-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)  
- [<span data-ttu-id="abd40-108">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="abd40-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md) 
- [<span data-ttu-id="abd40-109">Update (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="abd40-109">Update (FolderSync)</span></span>](update-foldersync.md)
  
```xml
<Update>
   <Folder/>
</Update>
```

```xml
<Update>
   <CalendarFolder/>
</Update>
```

```xml
<Update>
   <ContactsFolder/>
</Update>
```

```xml
<Update>
   <TasksFolder/>
</Update>
```

```xml
<Update>
   <SearchFolder/>
</Update>
```

<span data-ttu-id="abd40-110">**SyncFolderHierarchyCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="abd40-110">**SyncFolderHierarchyCreateOrUpdateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="abd40-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="abd40-111">Attributes and elements</span></span>

<span data-ttu-id="abd40-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="abd40-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="abd40-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="abd40-113">Attributes</span></span>

<span data-ttu-id="abd40-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="abd40-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="abd40-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="abd40-115">Child elements</span></span>

|<span data-ttu-id="abd40-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="abd40-116">**Element**</span></span>|<span data-ttu-id="abd40-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="abd40-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="abd40-118">Folder</span><span class="sxs-lookup"><span data-stu-id="abd40-118">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="abd40-119">Definiert den Ordner zum Erstellen, abrufen, suchen, synchronisieren oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="abd40-119">Defines the folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="abd40-120">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="abd40-120">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="abd40-121">Stellt einen Ordner dar, der in erster Linie Kalenderelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="abd40-121">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="abd40-122">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="abd40-122">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="abd40-123">Stellt einen Kontaktordner in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="abd40-123">Represents a contact folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="abd40-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="abd40-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="abd40-125">Stellt einen Suchordner dar, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="abd40-125">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="abd40-126">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="abd40-126">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="abd40-127">Stellt einen Aufgabenordner dar, den t in einem Postfach thcontained.</span><span class="sxs-lookup"><span data-stu-id="abd40-127">Represents a task folder t is thcontained in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="abd40-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="abd40-128">Parent elements</span></span>

|<span data-ttu-id="abd40-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="abd40-129">**Element**</span></span>|<span data-ttu-id="abd40-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="abd40-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="abd40-131">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="abd40-131">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="abd40-132">Enthält ein sequenziertes Array von Änderungstypen, die die Art der Unterschiede zwischen den Ordnern auf dem Client und den Ordnern auf dem Exchange-Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="abd40-132">Contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abd40-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="abd40-133">Remarks</span></span>

<span data-ttu-id="abd40-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="abd40-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="abd40-135">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="abd40-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="abd40-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="abd40-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="abd40-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="abd40-137">Schema name</span></span>  <br/> |<span data-ttu-id="abd40-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="abd40-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="abd40-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="abd40-139">Validation file</span></span>  <br/> |<span data-ttu-id="abd40-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="abd40-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="abd40-141">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="abd40-141">Can be empty</span></span>  <br/> |<span data-ttu-id="abd40-142">False</span><span class="sxs-lookup"><span data-stu-id="abd40-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="abd40-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abd40-143">See also</span></span>

- [<span data-ttu-id="abd40-144">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="abd40-144">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="abd40-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="abd40-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

