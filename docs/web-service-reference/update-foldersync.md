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
description: Das Update-Element identifiziert einen einzelnen Ordner, in den lokalen Client-Speicher zu aktualisieren.
ms.openlocfilehash: bf49741b2478edff450f114dc1464a0528072bea
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353504"
---
# <a name="update-foldersync"></a><span data-ttu-id="2847b-103">Update (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="2847b-103">Update (FolderSync)</span></span>

<span data-ttu-id="2847b-104">**Update** -Elements bezeichnet einen einzelnen Ordner, in den lokalen Client-Speicher zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2847b-104">The **Update** element identifies a single folder to update in the local client store.</span></span> 
  
- [<span data-ttu-id="2847b-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="2847b-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md) 
- [<span data-ttu-id="2847b-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2847b-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="2847b-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2847b-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)  
- [<span data-ttu-id="2847b-108">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="2847b-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md) 
- [<span data-ttu-id="2847b-109">Update (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="2847b-109">Update (FolderSync)</span></span>](update-foldersync.md)
  
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

<span data-ttu-id="2847b-110">**SyncFolderHierarchyCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="2847b-110">**SyncFolderHierarchyCreateOrUpdateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2847b-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2847b-111">Attributes and elements</span></span>

<span data-ttu-id="2847b-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2847b-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2847b-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="2847b-113">Attributes</span></span>

<span data-ttu-id="2847b-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="2847b-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2847b-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2847b-115">Child elements</span></span>

|<span data-ttu-id="2847b-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="2847b-116">**Element**</span></span>|<span data-ttu-id="2847b-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2847b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2847b-118">Folder</span><span class="sxs-lookup"><span data-stu-id="2847b-118">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="2847b-119">Definiert den Ordner, um das Erstellen, abrufen, suchen, synchronisieren oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2847b-119">Defines the folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="2847b-120">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="2847b-120">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="2847b-121">Stellt einen Ordner, der in erster Linie Kalenderelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="2847b-121">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="2847b-122">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="2847b-122">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="2847b-123">Stellt einem Kontaktordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="2847b-123">Represents a contact folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="2847b-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="2847b-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="2847b-125">Stellt einen Suchordner, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="2847b-125">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="2847b-126">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="2847b-126">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="2847b-127">Stellt eine Aufgabe Ordner t Thcontained in einem Postfach ist.</span><span class="sxs-lookup"><span data-stu-id="2847b-127">Represents a task folder t is thcontained in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2847b-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2847b-128">Parent elements</span></span>

|<span data-ttu-id="2847b-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="2847b-129">**Element**</span></span>|<span data-ttu-id="2847b-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2847b-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2847b-131">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="2847b-131">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="2847b-132">Enthält eine sequenzierten Array von Änderungstypen, die den Typ der Unterschiede zwischen den Ordnern auf dem Client und die Ordner auf dem Exchange-Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="2847b-132">Contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2847b-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2847b-133">Remarks</span></span>

<span data-ttu-id="2847b-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="2847b-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2847b-135">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2847b-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2847b-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="2847b-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2847b-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2847b-137">Schema name</span></span>  <br/> |<span data-ttu-id="2847b-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="2847b-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="2847b-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2847b-139">Validation file</span></span>  <br/> |<span data-ttu-id="2847b-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2847b-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2847b-141">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2847b-141">Can be empty</span></span>  <br/> |<span data-ttu-id="2847b-142">False</span><span class="sxs-lookup"><span data-stu-id="2847b-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2847b-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2847b-143">See also</span></span>

- [<span data-ttu-id="2847b-144">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2847b-144">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="2847b-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2847b-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

