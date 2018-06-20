---
title: ArchiveTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c4cb0718-37cd-41aa-86e7-b492c4bb86aa
description: Das ArchiveTag-Element gibt den Aufbewahrung Bezeichner des Archivs Tags auf eines Elements oder Ordners festlegen.
ms.openlocfilehash: ae9c7d512981af3bf564bcb73a9a27c5c78217fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757377"
---
# <a name="archivetag"></a><span data-ttu-id="bccc4-103">ArchiveTag</span><span class="sxs-lookup"><span data-stu-id="bccc4-103">ArchiveTag</span></span>

<span data-ttu-id="bccc4-104">Das **ArchiveTag** -Element gibt den Aufbewahrung Bezeichner des Archivs Tags auf eines Elements oder Ordners festlegen.</span><span class="sxs-lookup"><span data-stu-id="bccc4-104">The **ArchiveTag** element specifies the retention identifier of the archive tag set on an item or folder.</span></span> 
  
```XML
<ArchiveTag IsExplicit=""></ArchiveTag>
```

 <span data-ttu-id="bccc4-105">**RetentionTagType**</span><span class="sxs-lookup"><span data-stu-id="bccc4-105">**RetentionTagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bccc4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bccc4-106">Attributes and elements</span></span>

<span data-ttu-id="bccc4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bccc4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bccc4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="bccc4-108">Attributes</span></span>

|<span data-ttu-id="bccc4-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="bccc4-109">**Attribute**</span></span>|<span data-ttu-id="bccc4-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bccc4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bccc4-111">**IsExplicit**</span><span class="sxs-lookup"><span data-stu-id="bccc4-111">**IsExplicit**</span></span> <br/> |<span data-ttu-id="bccc4-112">Gibt an, ob die Aufbewahrungsrichtlinie auf eines Elements oder Ordners explizit festgelegt ist oder ob es von einem übergeordneten Ordner geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="bccc4-112">Specifies whether the retention policy is explicitly set on an item or folder or whether it is inherited from a parent folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bccc4-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bccc4-113">Child elements</span></span>

<span data-ttu-id="bccc4-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="bccc4-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bccc4-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bccc4-115">Parent elements</span></span>

|<span data-ttu-id="bccc4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="bccc4-116">**Element**</span></span>|<span data-ttu-id="bccc4-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bccc4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bccc4-118">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="bccc4-118">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="bccc4-119">Stellt einen Ordner, der in erster Linie Kalenderelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="bccc4-119">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="bccc4-120">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="bccc4-120">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="bccc4-121">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="bccc4-121">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="bccc4-122">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="bccc4-122">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="bccc4-123">Stellt ein Kontaktelement im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="bccc4-123">Represents a contact item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="bccc4-124">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="bccc4-124">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="bccc4-125">Stellt einen Kontakteordner, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="bccc4-125">Represents a contacts folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="bccc4-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="bccc4-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="bccc4-127">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="bccc4-127">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="bccc4-128">Folder</span><span class="sxs-lookup"><span data-stu-id="bccc4-128">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="bccc4-129">Definiert einen Ordner erstellen, abrufen, suchen, synchronisieren oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="bccc4-129">Defines a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="bccc4-130">Element</span><span class="sxs-lookup"><span data-stu-id="bccc4-130">Item</span></span>](item.md) <br/> |<span data-ttu-id="bccc4-131">Stellt ein generisches Element im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="bccc4-131">Represents a generic item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="bccc4-132">Message</span><span class="sxs-lookup"><span data-stu-id="bccc4-132">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="bccc4-133">Stellt eine Microsoft Exchange-e-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="bccc4-133">Represents a Microsoft Exchange email message.</span></span>  <br/> |
|[<span data-ttu-id="bccc4-134">PostItem-Objekt</span><span class="sxs-lookup"><span data-stu-id="bccc4-134">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="bccc4-135">Stellt ein Post-Element im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="bccc4-135">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="bccc4-136">"SearchFolder"</span><span class="sxs-lookup"><span data-stu-id="bccc4-136">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="bccc4-137">Stellt einen Suchordner, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="bccc4-137">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="bccc4-138">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="bccc4-138">Task</span></span>](task.md) <br/> |<span data-ttu-id="bccc4-139">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="bccc4-139">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="bccc4-140">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="bccc4-140">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="bccc4-141">Stellt einen Aufgabenordner, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="bccc4-141">Represents a tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bccc4-142">Textwert</span><span class="sxs-lookup"><span data-stu-id="bccc4-142">Text value</span></span>

<span data-ttu-id="bccc4-143">Der Textwert des **ArchiveTag** -Elements ist eine GUID, die Aufbewahrungsrichtlinie identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bccc4-143">The text value of the **ArchiveTag** element is a GUID that identifies the retention policy.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bccc4-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bccc4-144">Remarks</span></span>

<span data-ttu-id="bccc4-145">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bccc4-145">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="bccc4-146">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="bccc4-146">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bccc4-147">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bccc4-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bccc4-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="bccc4-148">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bccc4-149">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bccc4-149">Schema Name</span></span>  <br/> |<span data-ttu-id="bccc4-150">Typschema</span><span class="sxs-lookup"><span data-stu-id="bccc4-150">Type schema</span></span>  <br/> |
|<span data-ttu-id="bccc4-151">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bccc4-151">Validation File</span></span>  <br/> |<span data-ttu-id="bccc4-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bccc4-152">types.xsd</span></span>  <br/> |
|<span data-ttu-id="bccc4-153">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="bccc4-153">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="bccc4-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bccc4-154">See also</span></span>

- [<span data-ttu-id="bccc4-155">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bccc4-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

