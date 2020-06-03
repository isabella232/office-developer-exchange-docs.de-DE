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
description: Das Create-Element identifiziert einen einzelnen Ordner, der im lokalen Clientspeicher erstellt werden soll.
ms.openlocfilehash: 43f6a6b3c084c8ecae767c512181bbdf50c7e786
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458376"
---
# <a name="create-foldersync"></a><span data-ttu-id="bf6b3-103">Erstellen (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="bf6b3-103">Create (FolderSync)</span></span>

<span data-ttu-id="bf6b3-104">Das **Create** -Element identifiziert einen einzelnen Ordner, der im lokalen Clientspeicher erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf6b3-104">The **Create** element identifies a single folder to create in the local client store.</span></span> 
  
[<span data-ttu-id="bf6b3-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="bf6b3-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
  
[<span data-ttu-id="bf6b3-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="bf6b3-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="bf6b3-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bf6b3-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
[<span data-ttu-id="bf6b3-108">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="bf6b3-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
  
[<span data-ttu-id="bf6b3-109">Erstellen (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="bf6b3-109">Create (FolderSync)</span></span>](create-foldersync.md)
  
```xml
<Create>
   <Folder/>
   <CalendarFolder/>
   <ContactsFolder/>
   <SearchFolder/>
   <TasksFolder/>
</Create>
```

 <span data-ttu-id="bf6b3-110">**SyncFolderHierarchyCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="bf6b3-110">**SyncFolderHierarchyCreateOrUpdateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bf6b3-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bf6b3-111">Attributes and elements</span></span>

<span data-ttu-id="bf6b3-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bf6b3-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bf6b3-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="bf6b3-113">Attributes</span></span>

<span data-ttu-id="bf6b3-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="bf6b3-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bf6b3-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bf6b3-115">Child elements</span></span>

|<span data-ttu-id="bf6b3-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="bf6b3-116">**Element**</span></span>|<span data-ttu-id="bf6b3-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bf6b3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bf6b3-118">Folder</span><span class="sxs-lookup"><span data-stu-id="bf6b3-118">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="bf6b3-119">Definiert den Ordner zum Erstellen, abrufen, suchen, synchronisieren oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="bf6b3-119">Defines the folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="bf6b3-120">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="bf6b3-120">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="bf6b3-121">Stellt einen Ordner dar, der in erster Linie Kalenderelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="bf6b3-121">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="bf6b3-122">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="bf6b3-122">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="bf6b3-123">Stellt einen Kontaktordner in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="bf6b3-123">Represents a contact folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="bf6b3-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="bf6b3-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="bf6b3-125">Stellt einen in einem Postfach enthaltenen Suchordner dar.</span><span class="sxs-lookup"><span data-stu-id="bf6b3-125">Represents a search folder contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="bf6b3-126">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="bf6b3-126">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="bf6b3-127">Stellt einen Aufgabenordner dar, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="bf6b3-127">Represents a task folder contained in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bf6b3-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bf6b3-128">Parent elements</span></span>

|<span data-ttu-id="bf6b3-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="bf6b3-129">**Element**</span></span>|<span data-ttu-id="bf6b3-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bf6b3-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bf6b3-131">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="bf6b3-131">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="bf6b3-132">Enthält ein Sequenz Array von Änderungstypen, die die Art der Unterschiede zwischen den Elementen auf dem Client und den Elementen auf dem Exchange-Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="bf6b3-132">Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf6b3-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf6b3-133">Remarks</span></span>

<span data-ttu-id="bf6b3-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="bf6b3-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bf6b3-135">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="bf6b3-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf6b3-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="bf6b3-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bf6b3-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bf6b3-137">Schema name</span></span>  <br/> |<span data-ttu-id="bf6b3-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="bf6b3-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="bf6b3-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bf6b3-139">Validation file</span></span>  <br/> |<span data-ttu-id="bf6b3-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bf6b3-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bf6b3-141">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="bf6b3-141">Can be empty</span></span>  <br/> |<span data-ttu-id="bf6b3-142">False</span><span class="sxs-lookup"><span data-stu-id="bf6b3-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bf6b3-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf6b3-143">See also</span></span>



[<span data-ttu-id="bf6b3-144">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bf6b3-144">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="bf6b3-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bf6b3-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

