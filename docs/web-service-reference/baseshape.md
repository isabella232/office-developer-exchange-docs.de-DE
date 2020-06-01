---
title: BaseShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BaseShape
api_type:
- schema
ms.assetid: 42c04f3b-abaa-4197-a3d6-d21677ffb1c0
description: Das BaseShape-Element gibt die Gruppe von Eigenschaften an, die in einer Element-oder Ordner Antwort zurückgegeben werden sollen.
ms.openlocfilehash: 9b3f00ff94fbfe6ad6373b16ad95eb9136f81c64
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464490"
---
# <a name="baseshape"></a><span data-ttu-id="6e46f-103">BaseShape</span><span class="sxs-lookup"><span data-stu-id="6e46f-103">BaseShape</span></span>

<span data-ttu-id="6e46f-104">Das **BaseShape** -Element gibt die Gruppe von Eigenschaften an, die in einer Element-oder Ordner Antwort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6e46f-104">The **BaseShape** element identifies the set of properties to return in an item or folder response.</span></span> 
  
```xml
<BaseShape>IdOnly or Default or AllProperties</BaseShape>
```

 <span data-ttu-id="6e46f-105">**DefaultShapeNamesType**</span><span class="sxs-lookup"><span data-stu-id="6e46f-105">**DefaultShapeNamesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6e46f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6e46f-106">Attributes and elements</span></span>

<span data-ttu-id="6e46f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6e46f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6e46f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6e46f-108">Attributes</span></span>

<span data-ttu-id="6e46f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6e46f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6e46f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6e46f-110">Child elements</span></span>

<span data-ttu-id="6e46f-111">Keines</span><span class="sxs-lookup"><span data-stu-id="6e46f-111">None</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6e46f-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6e46f-112">Parent elements</span></span>

|<span data-ttu-id="6e46f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6e46f-113">**Element**</span></span>|<span data-ttu-id="6e46f-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6e46f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6e46f-115">FolderShape</span><span class="sxs-lookup"><span data-stu-id="6e46f-115">FolderShape</span></span>](foldershape.md) <br/> | <span data-ttu-id="6e46f-116">Identifiziert die Ordner Eigenschaften, die in die GetFolder-, FindFolder-oder SyncFolderHierarchy-Antwort eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6e46f-116">Identifies the folder properties to include in the GetFolder, FindFolder, or SyncFolderHierarchy response.</span></span><br/><br/><span data-ttu-id="6e46f-117">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="6e46f-117">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetFolder/FolderShape` <br/>  `/FindFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[<span data-ttu-id="6e46f-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="6e46f-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="6e46f-119">Identifiziert die Elementeigenschaften und Inhalte, die in einer GetItem-, FindItem-oder SyncFolderItems-Antwort enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="6e46f-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span><br/><br/><span data-ttu-id="6e46f-120">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="6e46f-120">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6e46f-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="6e46f-121">Text value</span></span>

<span data-ttu-id="6e46f-122">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6e46f-122">A text value is required.</span></span> <span data-ttu-id="6e46f-123">In der folgenden Tabelle sind die möglichen Text Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e46f-123">The following table lists the possible text values.</span></span>
  
<span data-ttu-id="6e46f-124">**Textwerte für das BaseShape-Element**</span><span class="sxs-lookup"><span data-stu-id="6e46f-124">**Text values for the BaseShape element**</span></span>

|<span data-ttu-id="6e46f-125">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6e46f-125">**Value**</span></span>|<span data-ttu-id="6e46f-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6e46f-126">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6e46f-127">IdOnly</span><span class="sxs-lookup"><span data-stu-id="6e46f-127">IdOnly</span></span>  <br/> |<span data-ttu-id="6e46f-128">Gibt nur die Element-oder Ordner-ID zurück.</span><span class="sxs-lookup"><span data-stu-id="6e46f-128">Returns only the item or folder ID.</span></span>  <br/> |
|<span data-ttu-id="6e46f-129">Standard</span><span class="sxs-lookup"><span data-stu-id="6e46f-129">Default</span></span>  <br/> |<span data-ttu-id="6e46f-130">Gibt eine Reihe von Eigenschaften zurück, die als Standard für das Element oder den Ordner definiert sind.</span><span class="sxs-lookup"><span data-stu-id="6e46f-130">Returns a set of properties that are defined as the default for the item or folder.</span></span>  <br/> |
|<span data-ttu-id="6e46f-131">AllProperties</span><span class="sxs-lookup"><span data-stu-id="6e46f-131">AllProperties</span></span>  <br/> |<span data-ttu-id="6e46f-132">Gibt alle Eigenschaften zurück, die von der Exchange-Geschäftslogikschicht zum Erstellen eines Ordners verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6e46f-132">Returns all the properties used by the Exchange Business Logic layer to construct a folder.</span></span>  <br/> |
   
<span data-ttu-id="6e46f-133">In der folgenden Tabelle sind die Standardeigenschaften aufgeführt, die für eine FindFolder-Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6e46f-133">The following table lists the default properties that are returned for a FindFolder request.</span></span> <span data-ttu-id="6e46f-134">Alle Unterordner eines bestimmten Ordners werden in der Reihenfolge nach Namen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6e46f-134">All subfolders of a given folder are returned in order by name.</span></span>
  
<span data-ttu-id="6e46f-135">**Standardeigenschaften**</span><span class="sxs-lookup"><span data-stu-id="6e46f-135">**Default properties**</span></span>

|<span data-ttu-id="6e46f-136">**Folder**</span><span class="sxs-lookup"><span data-stu-id="6e46f-136">**Folder**</span></span>|<span data-ttu-id="6e46f-137">**Standardeigenschaften**</span><span class="sxs-lookup"><span data-stu-id="6e46f-137">**Default Properties**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6e46f-138">Posteingang</span><span class="sxs-lookup"><span data-stu-id="6e46f-138">Inbox</span></span>  <br/> |<span data-ttu-id="6e46f-139">Ordner-Nr, Anzeigename, ungelesene Anzahl, Gesamtanzahl, Unterordner Anzahl</span><span class="sxs-lookup"><span data-stu-id="6e46f-139">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="6e46f-140">Kontakte</span><span class="sxs-lookup"><span data-stu-id="6e46f-140">Contacts</span></span>  <br/> |<span data-ttu-id="6e46f-141">Ordner-und Anzeigename, Gesamtanzahl, Unterordner Anzahl</span><span class="sxs-lookup"><span data-stu-id="6e46f-141">FolderId, display name, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="6e46f-142">Kalender</span><span class="sxs-lookup"><span data-stu-id="6e46f-142">Calendar</span></span>  <br/> |<span data-ttu-id="6e46f-143">Ordner-und Anzeigename, Unterordner Anzahl</span><span class="sxs-lookup"><span data-stu-id="6e46f-143">FolderId, display name, subfolder count</span></span>  <br/> |
|<span data-ttu-id="6e46f-144">Entwürfe</span><span class="sxs-lookup"><span data-stu-id="6e46f-144">Drafts</span></span>  <br/> |<span data-ttu-id="6e46f-145">Ordner-Nr, Anzeigename, ungelesene Anzahl, Gesamtanzahl, Unterordner Anzahl</span><span class="sxs-lookup"><span data-stu-id="6e46f-145">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="6e46f-146">Gelöschte Elemente</span><span class="sxs-lookup"><span data-stu-id="6e46f-146">Deleted items</span></span>  <br/> |<span data-ttu-id="6e46f-147">Ordner-Nr, Anzeigename, ungelesene Anzahl, Gesamtanzahl, Unterordner Anzahl</span><span class="sxs-lookup"><span data-stu-id="6e46f-147">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="6e46f-148">Andere Ordner</span><span class="sxs-lookup"><span data-stu-id="6e46f-148">Other folders</span></span>  <br/> |<span data-ttu-id="6e46f-149">Ordner-Nr, Anzeigename, ungelesene Anzahl, Gesamtanzahl, Unterordner Anzahl</span><span class="sxs-lookup"><span data-stu-id="6e46f-149">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="6e46f-150">Postausgang</span><span class="sxs-lookup"><span data-stu-id="6e46f-150">Outbox</span></span>  <br/> |<span data-ttu-id="6e46f-151">Ordner-Nr, Anzeigename, ungelesene Anzahl, Gesamtanzahl, Unterordner Anzahl</span><span class="sxs-lookup"><span data-stu-id="6e46f-151">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="6e46f-152">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="6e46f-152">Tasks</span></span>  <br/> |<span data-ttu-id="6e46f-153">Ordner-und Anzeigename, überfällige Anzahl, Gesamtanzahl, Unterordner Anzahl</span><span class="sxs-lookup"><span data-stu-id="6e46f-153">FolderId, display name, past due count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="6e46f-154">Notes</span><span class="sxs-lookup"><span data-stu-id="6e46f-154">Notes</span></span>  <br/> |<span data-ttu-id="6e46f-155">Ordner-und Anzeigename, Gesamtanzahl, Unterordner Anzahl</span><span class="sxs-lookup"><span data-stu-id="6e46f-155">FolderId, display name, total count, subfolder count</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e46f-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e46f-156">Remarks</span></span>

<span data-ttu-id="6e46f-157">Verwenden Sie das [AdditionalProperties](additionalproperties.md) -Element, um zusätzlich zu den durch das [BaseShape](baseshape.md) -Element identifizierten Eigenschaften zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="6e46f-157">To return properties in addition to those identified by the [BaseShape](baseshape.md) element, use the [AdditionalProperties](additionalproperties.md) element.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6e46f-158">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6e46f-158">Example</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="6e46f-159">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6e46f-159">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e46f-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e46f-160">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6e46f-161">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6e46f-161">Schema Name</span></span>  <br/> |<span data-ttu-id="6e46f-162">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6e46f-162">Types schema</span></span>  <br/> |
|<span data-ttu-id="6e46f-163">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6e46f-163">Validation File</span></span>  <br/> |<span data-ttu-id="6e46f-164">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6e46f-164">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6e46f-165">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6e46f-165">Can be Empty</span></span>  <br/> |<span data-ttu-id="6e46f-166">False</span><span class="sxs-lookup"><span data-stu-id="6e46f-166">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6e46f-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e46f-167">See also</span></span>

- [<span data-ttu-id="6e46f-168">FolderShape</span><span class="sxs-lookup"><span data-stu-id="6e46f-168">FolderShape</span></span>](foldershape.md)
- [<span data-ttu-id="6e46f-169">ItemShape</span><span class="sxs-lookup"><span data-stu-id="6e46f-169">ItemShape</span></span>](itemshape.md)

