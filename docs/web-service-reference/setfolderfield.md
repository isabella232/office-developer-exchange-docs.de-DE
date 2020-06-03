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
description: Das setfolderfield-Element stellt ein Update dar, mit dem der Wert für eine einzelne Eigenschaft eines Ordners in einem UpdateFolder-Vorgang festgelegt wird.
ms.openlocfilehash: ab75a3862801b9a7b3369d9a4116c653b461781c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530317"
---
# <a name="setfolderfield"></a><span data-ttu-id="4e3e8-103">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="4e3e8-103">SetFolderField</span></span>

<span data-ttu-id="4e3e8-104">Das **setfolderfield** -Element stellt ein Update dar, mit dem der Wert für eine einzelne Eigenschaft eines Ordners in einem UpdateFolder-Vorgang festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4e3e8-104">The **SetFolderField** element represents an update that sets the value for a single property on a folder in an UpdateFolder operation.</span></span> 

```xml
<SetFolderField>
   <FieldURI/>
   <Folder/>
</SetFolderField>
```
  
```xml
<SetFolderField>
   <IndexedFieldURI/> 
   <SearchFolder/> 
</SetFolderField>
```

```xml
<SetFolderField>
   <FieldURI/> 
   <TasksFolder/>
</SetFolderField>
```

```xml
<SetFolderField>
   <ExtendedFieldURI/> 
   <CalendarFolder/> 
</SetFolderField>
```

```xml
<SetFolderField>
   <ExtendedFieldURI/> 
   <SearchFolder/>
</SetFolderField>
```

```xml
<SetFolderField>
   <ExtendedFieldURI/> 
   <Folder/> 
</SetFolderField>
```

```xml
<SetFolderField>
    <IndexedFieldURI/> 
    <TasksFolder/>
</SetFolderField>
```

```xml
<SetFolderField>
   <FieldURI/> 
   <SearchFolder/>
</SetFolderField>
```

```xml
<SetFolderField>
   <FieldURI/> 
   <CalendarFolder/> 
</SetFolderField>
```

```xml
<SetFolderField>
   <ExtendedFieldURI/> 
   <TasksFolder/> 
</SetFolderField>
```

```xml
<SetFolderField>
   <IndexedFieldURI/> 
   <CalendarFolder/> 
</SetFolderField>
```

```xml
<SetFolderField>
   <IndexedFieldURI/> 
   <Folder/>
</SetFolderField>
```

```xml
<SetFolderField>
    <FieldURI/> 
    <ContactsFolder/>
</SetFolderField>
```

```xml
<SetFolderField>
   <ExtendedFieldURI/> 
   <ContactsFolder/>
</SetFolderField>
```

```xml
<SetFolderField>
   <IndexedFieldURI/> 
   <ContactsFolder/> 
</SetFolderField>
```


<span data-ttu-id="4e3e8-105">**SetFolderFieldType**</span><span class="sxs-lookup"><span data-stu-id="4e3e8-105">**SetFolderFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4e3e8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4e3e8-106">Attributes and elements</span></span>

<span data-ttu-id="4e3e8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4e3e8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4e3e8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4e3e8-108">Attributes</span></span>

<span data-ttu-id="4e3e8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4e3e8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4e3e8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4e3e8-110">Child elements</span></span>

|<span data-ttu-id="4e3e8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4e3e8-111">**Element**</span></span>|<span data-ttu-id="4e3e8-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4e3e8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e3e8-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="4e3e8-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="4e3e8-114">Identifiziert häufig referenzierte Eigenschaften nach URI.</span><span class="sxs-lookup"><span data-stu-id="4e3e8-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="4e3e8-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="4e3e8-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="4e3e8-116">Identifiziert einzelne Member eines Wörterbuchs.</span><span class="sxs-lookup"><span data-stu-id="4e3e8-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="4e3e8-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="4e3e8-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="4e3e8-118">Identifiziert erweiterte MAPI-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4e3e8-118">Identifies extended MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="4e3e8-119">Ordner</span><span class="sxs-lookup"><span data-stu-id="4e3e8-119">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="4e3e8-120">Gibt einen Ordner an, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4e3e8-120">Identifies a folder to update.</span></span>  <br/> |
|[<span data-ttu-id="4e3e8-121">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="4e3e8-121">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="4e3e8-122">Stellt einen Ordner dar, der in erster Linie Kalenderelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="4e3e8-122">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="4e3e8-123">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="4e3e8-123">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="4e3e8-124">Stellt einen Ordner Kontakte in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="4e3e8-124">Represents a Contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4e3e8-125">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="4e3e8-125">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="4e3e8-126">Stellt einen Suchordner dar, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="4e3e8-126">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4e3e8-127">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="4e3e8-127">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="4e3e8-128">Stellt einen Aufgabenordner dar, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="4e3e8-128">Represents a Tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4e3e8-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4e3e8-129">Parent elements</span></span>

|<span data-ttu-id="4e3e8-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="4e3e8-130">**Element**</span></span>|<span data-ttu-id="4e3e8-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4e3e8-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e3e8-132">Updates (Ordner)</span><span class="sxs-lookup"><span data-stu-id="4e3e8-132">Updates (Folder)</span></span>](updates-folder.md) <br/> |<span data-ttu-id="4e3e8-133">Enthält eine Gruppe von Elementen, die Append-, festlegen-und DELETE-Änderungen an Ordner Eigenschaften definiert.</span><span class="sxs-lookup"><span data-stu-id="4e3e8-133">Contains a set of elements that defines append, set, and delete changes to folder properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e3e8-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e3e8-134">Remarks</span></span>

<span data-ttu-id="4e3e8-135">Wenn die Eigenschaft vorhanden ist, wird der Wert der Eigenschaft auf den angegebenen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4e3e8-135">If the property exists, the property value is set to the specified value.</span></span> <span data-ttu-id="4e3e8-136">Wenn die Eigenschaft nicht vorhanden ist, wird die Eigenschaft mit dem angegebenen Wert erstellt.</span><span class="sxs-lookup"><span data-stu-id="4e3e8-136">If the property does not exist, the property is created with the specified value.</span></span>
  
<span data-ttu-id="4e3e8-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="4e3e8-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4e3e8-138">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4e3e8-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e3e8-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="4e3e8-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4e3e8-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4e3e8-140">Schema Name</span></span>  <br/> |<span data-ttu-id="4e3e8-141">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4e3e8-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="4e3e8-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4e3e8-142">Validation File</span></span>  <br/> |<span data-ttu-id="4e3e8-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4e3e8-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4e3e8-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4e3e8-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="4e3e8-145">False</span><span class="sxs-lookup"><span data-stu-id="4e3e8-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e3e8-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e3e8-146">See also</span></span>

- [<span data-ttu-id="4e3e8-147">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4e3e8-147">UpdateFolder operation</span></span>](updatefolder-operation.md)
- [<span data-ttu-id="4e3e8-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4e3e8-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

