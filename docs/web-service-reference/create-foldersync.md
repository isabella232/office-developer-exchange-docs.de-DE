---
title: Erstellen (FolderSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Create
api_type:
- schema
ms.assetid: 6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1
description: Das Create-Element identifiziert einen einzelnen Ordner im lokalen Client-Speicher zu erstellen.
ms.openlocfilehash: 867eecb89c115b008d4828e162b21d078eba695c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757734"
---
# <a name="create-foldersync"></a><span data-ttu-id="33637-103">Erstellen (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="33637-103">Create (FolderSync)</span></span>

<span data-ttu-id="33637-104">Das **Create** -Element identifiziert einen einzelnen Ordner im lokalen Client-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="33637-104">The **Create** element identifies a single folder to create in the local client store.</span></span> 
  
[<span data-ttu-id="33637-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="33637-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
  
[<span data-ttu-id="33637-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="33637-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="33637-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="33637-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
[<span data-ttu-id="33637-108">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="33637-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
  
[<span data-ttu-id="33637-109">Erstellen (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="33637-109">Create (FolderSync)</span></span>](create-foldersync.md)
  
```xml
<Create>
   <Folder/>
   <CalendarFolder/>
   <ContactsFolder/>
   <SearchFolder/>
   <TasksFolder/>
</Create>
```

 <span data-ttu-id="33637-110">**SyncFolderHierarchyCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="33637-110">**SyncFolderHierarchyCreateOrUpdateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="33637-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="33637-111">Attributes and elements</span></span>

<span data-ttu-id="33637-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="33637-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="33637-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="33637-113">Attributes</span></span>

<span data-ttu-id="33637-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="33637-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="33637-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="33637-115">Child elements</span></span>

|<span data-ttu-id="33637-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="33637-116">**Element**</span></span>|<span data-ttu-id="33637-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="33637-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="33637-118">Folder</span><span class="sxs-lookup"><span data-stu-id="33637-118">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="33637-119">Definiert den Ordner, um das Erstellen, abrufen, suchen, synchronisieren oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="33637-119">Defines the folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="33637-120">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="33637-120">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="33637-121">Stellt einen Ordner, der in erster Linie Kalenderelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="33637-121">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="33637-122">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="33637-122">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="33637-123">Stellt einem Kontaktordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="33637-123">Represents a contact folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="33637-124">"SearchFolder"</span><span class="sxs-lookup"><span data-stu-id="33637-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="33637-125">Stellt einen Suchordner in einem Postfach enthalten.</span><span class="sxs-lookup"><span data-stu-id="33637-125">Represents a search folder contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="33637-126">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="33637-126">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="33637-127">Stellt einen Aufgabenordner, die in einem Postfach enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="33637-127">Represents a task folder contained in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="33637-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="33637-128">Parent elements</span></span>

|<span data-ttu-id="33637-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="33637-129">**Element**</span></span>|<span data-ttu-id="33637-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="33637-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="33637-131">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="33637-131">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="33637-132">Enthält ein Array Sequenz von Dateitypen ändern, die den Typ der Unterschiede zwischen den Elementen auf dem Client und der Elemente auf dem Exchange-Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="33637-132">Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33637-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="33637-133">Remarks</span></span>

<span data-ttu-id="33637-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="33637-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="33637-135">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="33637-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33637-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="33637-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="33637-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="33637-137">Schema name</span></span>  <br/> |<span data-ttu-id="33637-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="33637-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="33637-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="33637-139">Validation file</span></span>  <br/> |<span data-ttu-id="33637-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="33637-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="33637-141">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="33637-141">Can be empty</span></span>  <br/> |<span data-ttu-id="33637-142">False</span><span class="sxs-lookup"><span data-stu-id="33637-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="33637-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33637-143">See also</span></span>



[<span data-ttu-id="33637-144">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="33637-144">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="33637-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="33637-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

