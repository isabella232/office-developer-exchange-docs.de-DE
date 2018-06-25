---
title: SetFolderField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetFolderField
api_type:
- schema
ms.assetid: 8c69db7b-54b5-4ae2-abca-4d6e0937a790
description: Das SetFolderField-Element stellt ein Update, das den Wert für eine einzelne Eigenschaft für einen Ordner in einem Vorgang UpdateFolder fest.
ms.openlocfilehash: 1919c335197c83999875a17397e9c9d4405d1e3f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831407"
---
# <a name="setfolderfield"></a><span data-ttu-id="4dd88-103">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="4dd88-103">SetFolderField</span></span>

<span data-ttu-id="4dd88-104">Das **SetFolderField** -Element stellt ein Update, das den Wert für eine einzelne Eigenschaft für einen Ordner in einem Vorgang UpdateFolder fest.</span><span class="sxs-lookup"><span data-stu-id="4dd88-104">The **SetFolderField** element represents an update that sets the value for a single property on a folder in an UpdateFolder operation.</span></span> 
  
```xml
<SetFolderField>
   <FieldURI/>
   <Folder/>
</SetFolderField>
```

 <span data-ttu-id="4dd88-105">**SetFolderFieldType**</span><span class="sxs-lookup"><span data-stu-id="4dd88-105">**SetFolderFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4dd88-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4dd88-106">Attributes and elements</span></span>

<span data-ttu-id="4dd88-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4dd88-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4dd88-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4dd88-108">Attributes</span></span>

<span data-ttu-id="4dd88-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4dd88-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4dd88-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4dd88-110">Child elements</span></span>

|<span data-ttu-id="4dd88-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4dd88-111">**Element**</span></span>|<span data-ttu-id="4dd88-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4dd88-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4dd88-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="4dd88-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="4dd88-114">Identifiziert die Eigenschaften von URI häufig verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4dd88-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="4dd88-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="4dd88-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="4dd88-116">Einzelne Elemente eines Wörterbuchs identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4dd88-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="4dd88-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="4dd88-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="4dd88-118">Identifiziert extended MAPI-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4dd88-118">Identifies extended MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="4dd88-119">Folder</span><span class="sxs-lookup"><span data-stu-id="4dd88-119">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="4dd88-120">Gibt einen Ordner aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4dd88-120">Identifies a folder to update.</span></span>  <br/> |
|[<span data-ttu-id="4dd88-121">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="4dd88-121">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="4dd88-122">Stellt einen Ordner, der in erster Linie Kalenderelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="4dd88-122">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="4dd88-123">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="4dd88-123">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="4dd88-124">Stellt einen Kontakteordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="4dd88-124">Represents a Contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4dd88-125">"SearchFolder"</span><span class="sxs-lookup"><span data-stu-id="4dd88-125">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="4dd88-126">Stellt einen Suchordner, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="4dd88-126">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4dd88-127">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="4dd88-127">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="4dd88-128">Stellt einen Aufgabenordner, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="4dd88-128">Represents a Tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4dd88-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4dd88-129">Parent elements</span></span>

|<span data-ttu-id="4dd88-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="4dd88-130">**Element**</span></span>|<span data-ttu-id="4dd88-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4dd88-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4dd88-132">Updates (Ordner)</span><span class="sxs-lookup"><span data-stu-id="4dd88-132">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="4dd88-133">Enthält eine Reihe von Elementen, die definiert, anfügen, festlegen und Löschen von Änderungen an den Eigenschaften des Ordners.</span><span class="sxs-lookup"><span data-stu-id="4dd88-133">Contains a set of elements that defines append, set, and delete changes to folder properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4dd88-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4dd88-134">Remarks</span></span>

<span data-ttu-id="4dd88-135">Wenn die Eigenschaft vorhanden ist, wird der Wert der Eigenschaft auf den angegebenen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4dd88-135">If the property exists, the property value is set to the specified value.</span></span> <span data-ttu-id="4dd88-136">Wenn die Eigenschaft nicht vorhanden ist, wird die Eigenschaft mit dem angegebenen Wert erstellt.</span><span class="sxs-lookup"><span data-stu-id="4dd88-136">If the property does not exist, the property is created with the specified value.</span></span>
  
<span data-ttu-id="4dd88-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="4dd88-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4dd88-138">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4dd88-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4dd88-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="4dd88-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4dd88-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4dd88-140">Schema Name</span></span>  <br/> |<span data-ttu-id="4dd88-141">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4dd88-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="4dd88-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4dd88-142">Validation File</span></span>  <br/> |<span data-ttu-id="4dd88-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4dd88-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4dd88-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4dd88-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="4dd88-145">False</span><span class="sxs-lookup"><span data-stu-id="4dd88-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4dd88-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4dd88-146">See also</span></span>



[<span data-ttu-id="4dd88-147">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4dd88-147">UpdateFolder operation</span></span>](updatefolder-operation.md)


- [<span data-ttu-id="4dd88-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4dd88-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

