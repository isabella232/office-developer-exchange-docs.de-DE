---
title: FindFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindFolder
api_type:
- schema
ms.assetid: b8a59740-d978-454c-9629-a10792385ba0
description: Das FindFolder-Element definiert eine Anforderung zum Suchen von Ordnern in einem Postfach.
ms.openlocfilehash: 248047206a661afe723543e52c51b57847148423
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462577"
---
# <a name="findfolder"></a><span data-ttu-id="4f73c-103">FindFolder</span><span class="sxs-lookup"><span data-stu-id="4f73c-103">FindFolder</span></span>

<span data-ttu-id="4f73c-104">Das **FindFolder** -Element definiert eine Anforderung zum Suchen von Ordnern in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="4f73c-104">The **FindFolder** element defines a request to find folders in a mailbox.</span></span> 
  
```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <IndexedPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <FractionalPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

<span data-ttu-id="4f73c-105">**FindFolderType**</span><span class="sxs-lookup"><span data-stu-id="4f73c-105">**FindFolderType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4f73c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4f73c-106">Attributes and elements</span></span>

<span data-ttu-id="4f73c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4f73c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f73c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4f73c-108">Attributes</span></span>

|<span data-ttu-id="4f73c-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4f73c-109">**Attribute**</span></span>|<span data-ttu-id="4f73c-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f73c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4f73c-111">Traversal</span><span class="sxs-lookup"><span data-stu-id="4f73c-111">Traversal</span></span>  <br/> |<span data-ttu-id="4f73c-112">Definiert, wie eine Suche durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f73c-112">Defines how a search is performed.</span></span> <span data-ttu-id="4f73c-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4f73c-113">This attribute is required.</span></span>  <br/> |
   
#### <a name="traversal-attribute-values"></a><span data-ttu-id="4f73c-114">Traversal-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="4f73c-114">Traversal attribute values</span></span>

|<span data-ttu-id="4f73c-115">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4f73c-115">**Value**</span></span>|<span data-ttu-id="4f73c-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f73c-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4f73c-117">Flachen</span><span class="sxs-lookup"><span data-stu-id="4f73c-117">Shallow</span></span>  <br/> |<span data-ttu-id="4f73c-118">Weist den FindFolder-Vorgang an, nur den identifizierten Ordner zu durchsuchen und nur die Ordner-IDs für Elemente zurückzugeben, die nicht gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="4f73c-118">Instructs the FindFolder operation to search only the identified folder and to return only the folder IDs for items that have not been deleted.</span></span> <span data-ttu-id="4f73c-119">Dies wird als flacher Durchlauf bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4f73c-119">This is called a shallow traversal.</span></span>  <br/> |
|<span data-ttu-id="4f73c-120">Tiefe</span><span class="sxs-lookup"><span data-stu-id="4f73c-120">Deep</span></span>  <br/> |<span data-ttu-id="4f73c-121">Weist den FindFolder-Vorgang an, in allen untergeordneten Ordnern des identifizierten übergeordneten Ordners zu suchen und nur die Ordner-IDs für Elemente zurückzugeben, die nicht gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="4f73c-121">Instructs the FindFolder operation to search in all child folders of the identified parent folder and to return only the folder IDs for items that have not been deleted.</span></span> <span data-ttu-id="4f73c-122">Dies wird als Deep Traversal bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4f73c-122">This is called a deep traversal.</span></span>  <br/> |
|<span data-ttu-id="4f73c-123">SoftDeleted</span><span class="sxs-lookup"><span data-stu-id="4f73c-123">SoftDeleted</span></span>  <br/> |<span data-ttu-id="4f73c-124">Weist den FindFolder-Vorgang an, eine flache Durchquerung der Suche nach gelöschten Elementen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="4f73c-124">Instructs the FindFolder operation to perform a shallow traversal search for deleted items.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4f73c-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f73c-125">Child elements</span></span>

|<span data-ttu-id="4f73c-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f73c-126">**Element**</span></span>|<span data-ttu-id="4f73c-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f73c-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f73c-128">FolderShape</span><span class="sxs-lookup"><span data-stu-id="4f73c-128">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="4f73c-129">Gibt die Ordner Eigenschaften an, die in eine FindFolder-Antwort eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4f73c-129">Identifies the folder properties to include in a FindFolder response.</span></span>  <br/> |
|[<span data-ttu-id="4f73c-130">IndexedPageFolderView</span><span class="sxs-lookup"><span data-stu-id="4f73c-130">IndexedPageFolderView</span></span>](indexedpagefolderview.md) <br/> |<span data-ttu-id="4f73c-131">Beschreibt, wie Informationen zum ausgelagerten Element in einer FindFolder-Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4f73c-131">Describes how paged item information is returned in a FindFolder response.</span></span> <span data-ttu-id="4f73c-132">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="4f73c-132">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="4f73c-133">FractionalPageFolderView</span><span class="sxs-lookup"><span data-stu-id="4f73c-133">FractionalPageFolderView</span></span>](fractionalpagefolderview.md) <br/> |<span data-ttu-id="4f73c-134">Beschreibt, wo die ausgelagerte Ansicht beginnt und wie viele Ordner in einer FindFolder-Anforderung maximal zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4f73c-134">Describes where the paged view starts and the maximum number of folders returned in a FindFolder request.</span></span> <span data-ttu-id="4f73c-135">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="4f73c-135">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="4f73c-136">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="4f73c-136">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="4f73c-137">Definiert eine Einschränkung oder Abfrage, die zum Filtern von Ordnern in einem FindFolder-Vorgang verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4f73c-137">Defines a restriction or query that is used to filter folders in a FindFolder operation.</span></span> <span data-ttu-id="4f73c-138">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="4f73c-138">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="4f73c-139">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="4f73c-139">ParentFolderIds</span></span>](parentfolderids.md) <br/> |<span data-ttu-id="4f73c-140">Identifiziert Ordner für den zu durchsuchenden FindFolder-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="4f73c-140">Identifies folders for the FindFolder operation to search.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4f73c-141">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f73c-141">Parent elements</span></span>

<span data-ttu-id="4f73c-142">Keine.</span><span class="sxs-lookup"><span data-stu-id="4f73c-142">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4f73c-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f73c-143">Remarks</span></span>

<span data-ttu-id="4f73c-144">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="4f73c-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="4f73c-145">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4f73c-145">Example</span></span>

<span data-ttu-id="4f73c-146">Im folgenden Beispiel einer FindFolder-Anforderung wird gezeigt, wie eine Anforderung zum Auffinden aller Ordner in einem Posteingang bildet.</span><span class="sxs-lookup"><span data-stu-id="4f73c-146">The following example of a FindFolder request shows how to form a request to find all the folders located in an Inbox.</span></span>
  
```xml
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

## <a name="element-information"></a><span data-ttu-id="4f73c-147">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4f73c-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f73c-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="4f73c-148">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4f73c-149">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4f73c-149">Schema Name</span></span>  <br/> |<span data-ttu-id="4f73c-150">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4f73c-150">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4f73c-151">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4f73c-151">Validation File</span></span>  <br/> |<span data-ttu-id="4f73c-152">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4f73c-152">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4f73c-153">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4f73c-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="4f73c-154">False</span><span class="sxs-lookup"><span data-stu-id="4f73c-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4f73c-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f73c-155">See also</span></span>

- [<span data-ttu-id="4f73c-156">FindFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4f73c-156">FindFolder operation</span></span>](findfolder-operation.md)

