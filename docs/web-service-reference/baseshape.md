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
description: Das BaseShape-Element identifiziert die Gruppe von Eigenschaften in einer Antwort Elements oder Ordners zurückgegeben werden sollen.
ms.openlocfilehash: 69b27d23fd75d4c1a274f31dfa419b759dbb2bbe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757439"
---
# <a name="baseshape"></a><span data-ttu-id="b60d9-103">BaseShape</span><span class="sxs-lookup"><span data-stu-id="b60d9-103">BaseShape</span></span>

<span data-ttu-id="b60d9-104">Das **BaseShape** -Element identifiziert die Gruppe von Eigenschaften in einer Antwort Elements oder Ordners zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b60d9-104">The **BaseShape** element identifies the set of properties to return in an item or folder response.</span></span> 
  
```xml
<BaseShape>IdOnly or Default or AllProperties</BaseShape>
```

 <span data-ttu-id="b60d9-105">**DefaultShapeNamesType**</span><span class="sxs-lookup"><span data-stu-id="b60d9-105">**DefaultShapeNamesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b60d9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b60d9-106">Attributes and elements</span></span>

<span data-ttu-id="b60d9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b60d9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b60d9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b60d9-108">Attributes</span></span>

<span data-ttu-id="b60d9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b60d9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b60d9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b60d9-110">Child elements</span></span>

<span data-ttu-id="b60d9-111">Keine</span><span class="sxs-lookup"><span data-stu-id="b60d9-111">None</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b60d9-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b60d9-112">Parent elements</span></span>

|<span data-ttu-id="b60d9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b60d9-113">**Element**</span></span>|<span data-ttu-id="b60d9-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b60d9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b60d9-115">FolderShape</span><span class="sxs-lookup"><span data-stu-id="b60d9-115">FolderShape</span></span>](foldershape.md) <br/> | <span data-ttu-id="b60d9-116">Identifiziert die Ordnereigenschaften in der Antwort GetFolder, FindFolder oder SyncFolderHierarchy aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="b60d9-116">Identifies the folder properties to include in the GetFolder, FindFolder, or SyncFolderHierarchy response.</span></span><br/><br/><span data-ttu-id="b60d9-117">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="b60d9-117">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetFolder/FolderShape` <br/>  `/FindFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[<span data-ttu-id="b60d9-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="b60d9-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="b60d9-119">Identifiziert die Elementeigenschaften und den Inhalt in einer Antwort GetItem, FindItem oder SyncFolderItems aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="b60d9-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span><br/><br/><span data-ttu-id="b60d9-120">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="b60d9-120">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b60d9-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="b60d9-121">Text value</span></span>

<span data-ttu-id="b60d9-122">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b60d9-122">A text value is required.</span></span> <span data-ttu-id="b60d9-123">Die folgende Tabelle enthält die möglichen Textwerte.</span><span class="sxs-lookup"><span data-stu-id="b60d9-123">The following table lists the possible text values.</span></span>
  
<span data-ttu-id="b60d9-124">**Textwerte für das BaseShape-element**</span><span class="sxs-lookup"><span data-stu-id="b60d9-124">**Text values for the BaseShape element**</span></span>

|<span data-ttu-id="b60d9-125">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b60d9-125">**Value**</span></span>|<span data-ttu-id="b60d9-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b60d9-126">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b60d9-127">IdOnly</span><span class="sxs-lookup"><span data-stu-id="b60d9-127">IdOnly</span></span>  <br/> |<span data-ttu-id="b60d9-128">Gibt nur die ID Elements oder Ordners zurück.</span><span class="sxs-lookup"><span data-stu-id="b60d9-128">Returns only the item or folder ID.</span></span>  <br/> |
|<span data-ttu-id="b60d9-129">Standard</span><span class="sxs-lookup"><span data-stu-id="b60d9-129">Default</span></span>  <br/> |<span data-ttu-id="b60d9-130">Gibt einen Satz von Eigenschaften, die als Standard für das Element oder Ordner definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b60d9-130">Returns a set of properties that are defined as the default for the item or folder.</span></span>  <br/> |
|<span data-ttu-id="b60d9-131">AllProperties</span><span class="sxs-lookup"><span data-stu-id="b60d9-131">AllProperties</span></span>  <br/> |<span data-ttu-id="b60d9-132">Gibt die Eigenschaften, die für die durch die Ebene des Exchange-Geschäftslogik verwendet, um einen Ordner zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b60d9-132">Returns all the properties used by the Exchange Business Logic layer to construct a folder.</span></span>  <br/> |
   
<span data-ttu-id="b60d9-133">Die folgende Tabelle enthält die Standardeigenschaften, die für eine Anforderung FindFolder zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b60d9-133">The following table lists the default properties that are returned for a FindFolder request.</span></span> <span data-ttu-id="b60d9-134">Alle Unterordner eines bestimmten Ordners werden namentlich in der Reihenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b60d9-134">All subfolders of a given folder are returned in order by name.</span></span>
  
<span data-ttu-id="b60d9-135">**Standardeigenschaften**</span><span class="sxs-lookup"><span data-stu-id="b60d9-135">**Default properties**</span></span>

|<span data-ttu-id="b60d9-136">**Folder**</span><span class="sxs-lookup"><span data-stu-id="b60d9-136">**Folder**</span></span>|<span data-ttu-id="b60d9-137">**Standardeigenschaften**</span><span class="sxs-lookup"><span data-stu-id="b60d9-137">**Default Properties**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b60d9-138">Posteingang</span><span class="sxs-lookup"><span data-stu-id="b60d9-138">Inbox</span></span>  <br/> |<span data-ttu-id="b60d9-139">FolderId, Anzeigename, ungelesenen, Gesamtzahl, Anzahl der Unterordner</span><span class="sxs-lookup"><span data-stu-id="b60d9-139">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="b60d9-140">Kontakte</span><span class="sxs-lookup"><span data-stu-id="b60d9-140">Contacts</span></span>  <br/> |<span data-ttu-id="b60d9-141">FolderId, Anzeigename, Gesamtzahl, Anzahl der Unterordner</span><span class="sxs-lookup"><span data-stu-id="b60d9-141">FolderId, display name, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="b60d9-142">Kalender</span><span class="sxs-lookup"><span data-stu-id="b60d9-142">Calendar</span></span>  <br/> |<span data-ttu-id="b60d9-143">FolderId, Anzeigename, Anzahl der Unterordner</span><span class="sxs-lookup"><span data-stu-id="b60d9-143">FolderId, display name, subfolder count</span></span>  <br/> |
|<span data-ttu-id="b60d9-144">Entwürfe</span><span class="sxs-lookup"><span data-stu-id="b60d9-144">Drafts</span></span>  <br/> |<span data-ttu-id="b60d9-145">FolderId, Anzeigename, ungelesenen, Gesamtzahl, Anzahl der Unterordner</span><span class="sxs-lookup"><span data-stu-id="b60d9-145">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="b60d9-146">Gelöschte Elemente</span><span class="sxs-lookup"><span data-stu-id="b60d9-146">Deleted items</span></span>  <br/> |<span data-ttu-id="b60d9-147">FolderId, Anzeigename, ungelesenen, Gesamtzahl, Anzahl der Unterordner</span><span class="sxs-lookup"><span data-stu-id="b60d9-147">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="b60d9-148">Andere Ordner</span><span class="sxs-lookup"><span data-stu-id="b60d9-148">Other folders</span></span>  <br/> |<span data-ttu-id="b60d9-149">FolderId, Anzeigename, ungelesenen, Gesamtzahl, Anzahl der Unterordner</span><span class="sxs-lookup"><span data-stu-id="b60d9-149">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="b60d9-150">Postausgang</span><span class="sxs-lookup"><span data-stu-id="b60d9-150">Outbox</span></span>  <br/> |<span data-ttu-id="b60d9-151">FolderId, Anzeigename, ungelesenen, Gesamtzahl, Anzahl der Unterordner</span><span class="sxs-lookup"><span data-stu-id="b60d9-151">FolderId, display name, unread count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="b60d9-152">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="b60d9-152">Tasks</span></span>  <br/> |<span data-ttu-id="b60d9-153">FolderId Anzeigename überfälligen Count, Gesamtzahl, Anzahl der Unterordner</span><span class="sxs-lookup"><span data-stu-id="b60d9-153">FolderId, display name, past due count, total count, subfolder count</span></span>  <br/> |
|<span data-ttu-id="b60d9-154">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="b60d9-154">Notes</span></span>  <br/> |<span data-ttu-id="b60d9-155">FolderId, Anzeigename, Gesamtzahl, Anzahl der Unterordner</span><span class="sxs-lookup"><span data-stu-id="b60d9-155">FolderId, display name, total count, subfolder count</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b60d9-156">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b60d9-156">Remarks</span></span>

<span data-ttu-id="b60d9-157">Verwenden Sie zum Zurückgeben von Eigenschaften zusätzlich zu den durch das [BaseShape](baseshape.md) -Element, das [AdditionalProperties](additionalproperties.md) -Element ein.</span><span class="sxs-lookup"><span data-stu-id="b60d9-157">To return properties in addition to those identified by the [BaseShape](baseshape.md) element, use the [AdditionalProperties](additionalproperties.md) element.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b60d9-158">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b60d9-158">Example</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a><span data-ttu-id="b60d9-159">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b60d9-159">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b60d9-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="b60d9-160">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b60d9-161">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b60d9-161">Schema Name</span></span>  <br/> |<span data-ttu-id="b60d9-162">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b60d9-162">Types schema</span></span>  <br/> |
|<span data-ttu-id="b60d9-163">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b60d9-163">Validation File</span></span>  <br/> |<span data-ttu-id="b60d9-164">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b60d9-164">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b60d9-165">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b60d9-165">Can be Empty</span></span>  <br/> |<span data-ttu-id="b60d9-166">False</span><span class="sxs-lookup"><span data-stu-id="b60d9-166">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b60d9-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b60d9-167">See also</span></span>

- [<span data-ttu-id="b60d9-168">FolderShape</span><span class="sxs-lookup"><span data-stu-id="b60d9-168">FolderShape</span></span>](foldershape.md)
- [<span data-ttu-id="b60d9-169">ItemShape</span><span class="sxs-lookup"><span data-stu-id="b60d9-169">ItemShape</span></span>](itemshape.md)

