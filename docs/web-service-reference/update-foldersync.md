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
ms.openlocfilehash: 6d4a6233df41ea95e1fd9b394502bfb2728bddb6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839337"
---
# <a name="update-foldersync"></a><span data-ttu-id="cfd00-103">Update (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="cfd00-103">Update (FolderSync)</span></span>

<span data-ttu-id="cfd00-104">**Update** -Elements bezeichnet einen einzelnen Ordner, in den lokalen Client-Speicher zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="cfd00-104">The **Update** element identifies a single folder to update in the local client store.</span></span> 
  
[<span data-ttu-id="cfd00-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="cfd00-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
  
[<span data-ttu-id="cfd00-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cfd00-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="cfd00-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cfd00-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
[<span data-ttu-id="cfd00-108">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="cfd00-108">Changes (Hierarchy)</span></span>](changes-hierarchy.md)
  
[<span data-ttu-id="cfd00-109">Update (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="cfd00-109">Update (FolderSync)</span></span>](update-foldersync.md)
  
```xml
<Update>
   <Folder/>
</Update>
```

 <span data-ttu-id="cfd00-110">**SyncFolderHierarchyCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="cfd00-110">**SyncFolderHierarchyCreateOrUpdateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cfd00-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cfd00-111">Attributes and elements</span></span>

<span data-ttu-id="cfd00-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cfd00-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cfd00-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="cfd00-113">Attributes</span></span>

<span data-ttu-id="cfd00-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="cfd00-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cfd00-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cfd00-115">Child elements</span></span>

|<span data-ttu-id="cfd00-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="cfd00-116">**Element**</span></span>|<span data-ttu-id="cfd00-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cfd00-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cfd00-118">Folder</span><span class="sxs-lookup"><span data-stu-id="cfd00-118">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="cfd00-119">Definiert den Ordner, um das Erstellen, abrufen, suchen, synchronisieren oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="cfd00-119">Defines the folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="cfd00-120">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="cfd00-120">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="cfd00-121">Stellt einen Ordner, der in erster Linie Kalenderelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="cfd00-121">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="cfd00-122">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="cfd00-122">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="cfd00-123">Stellt einem Kontaktordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="cfd00-123">Represents a contact folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="cfd00-124">"SearchFolder"</span><span class="sxs-lookup"><span data-stu-id="cfd00-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="cfd00-125">Stellt einen Suchordner, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="cfd00-125">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="cfd00-126">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="cfd00-126">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="cfd00-127">Stellt eine Aufgabe Ordner t Thcontained in einem Postfach ist.</span><span class="sxs-lookup"><span data-stu-id="cfd00-127">Represents a task folder t is thcontained in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cfd00-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cfd00-128">Parent elements</span></span>

|<span data-ttu-id="cfd00-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="cfd00-129">**Element**</span></span>|<span data-ttu-id="cfd00-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cfd00-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cfd00-131">Änderungen (Hierarchie)</span><span class="sxs-lookup"><span data-stu-id="cfd00-131">Changes (Hierarchy)</span></span>](changes-hierarchy.md) <br/> |<span data-ttu-id="cfd00-132">Enthält eine sequenzierten Array von Änderungstypen, die den Typ der Unterschiede zwischen den Ordnern auf dem Client und die Ordner auf dem Exchange-Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="cfd00-132">Contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cfd00-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cfd00-133">Remarks</span></span>

<span data-ttu-id="cfd00-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="cfd00-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cfd00-135">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="cfd00-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cfd00-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="cfd00-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cfd00-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cfd00-137">Schema name</span></span>  <br/> |<span data-ttu-id="cfd00-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="cfd00-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="cfd00-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cfd00-139">Validation file</span></span>  <br/> |<span data-ttu-id="cfd00-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cfd00-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cfd00-141">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="cfd00-141">Can be empty</span></span>  <br/> |<span data-ttu-id="cfd00-142">False</span><span class="sxs-lookup"><span data-stu-id="cfd00-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cfd00-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfd00-143">See also</span></span>



[<span data-ttu-id="cfd00-144">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cfd00-144">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="cfd00-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cfd00-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

