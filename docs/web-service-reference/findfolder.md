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
ms.openlocfilehash: d41283547c443e38e2e87379a7224df9c89f901d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758443"
---
# <a name="findfolder"></a><span data-ttu-id="a8528-103">FindFolder</span><span class="sxs-lookup"><span data-stu-id="a8528-103">FindFolder</span></span>

<span data-ttu-id="a8528-104">Das **FindFolder** -Element definiert eine Anforderung zum Suchen von Ordnern in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="a8528-104">The **FindFolder** element defines a request to find folders in a mailbox.</span></span> 
  
```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <IndexedPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

 <span data-ttu-id="a8528-105">**FindFolderType**</span><span class="sxs-lookup"><span data-stu-id="a8528-105">**FindFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a8528-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a8528-106">Attributes and elements</span></span>

<span data-ttu-id="a8528-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a8528-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8528-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a8528-108">Attributes</span></span>

|<span data-ttu-id="a8528-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a8528-109">**Attribute**</span></span>|<span data-ttu-id="a8528-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a8528-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8528-111">Durchqueren</span><span class="sxs-lookup"><span data-stu-id="a8528-111">Traversal</span></span>  <br/> |<span data-ttu-id="a8528-112">Definiert, wie eine Suche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8528-112">Defines how a search is performed.</span></span> <span data-ttu-id="a8528-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a8528-113">This attribute is required.</span></span>  <br/> |
   
#### <a name="traversal-attribute-values"></a><span data-ttu-id="a8528-114">Traversal Attributwerte</span><span class="sxs-lookup"><span data-stu-id="a8528-114">Traversal attribute values</span></span>

|<span data-ttu-id="a8528-115">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a8528-115">**Value**</span></span>|<span data-ttu-id="a8528-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a8528-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8528-117">Flach</span><span class="sxs-lookup"><span data-stu-id="a8528-117">Shallow</span></span>  <br/> |<span data-ttu-id="a8528-118">Weist den FindFolder Vorgang, um nur den identifizierten Ordner suchen und nur den Ordner IDs für Elemente zurückgegeben, die nicht gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="a8528-118">Instructs the FindFolder operation to search only the identified folder and to return only the folder IDs for items that have not been deleted.</span></span> <span data-ttu-id="a8528-119">Dies ist eine flache durchqueren bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a8528-119">This is called a shallow traversal.</span></span>  <br/> |
|<span data-ttu-id="a8528-120">Tief</span><span class="sxs-lookup"><span data-stu-id="a8528-120">Deep</span></span>  <br/> |<span data-ttu-id="a8528-121">Weist den Vorgang FindFolder in alle untergeordneten Ordner des angegebenen übergeordneten Ordners durchsuchen und nur den Ordner IDs für Elemente zurückgegeben, die nicht gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="a8528-121">Instructs the FindFolder operation to search in all child folders of the identified parent folder and to return only the folder IDs for items that have not been deleted.</span></span> <span data-ttu-id="a8528-122">Dies ist eine umfassende durchqueren bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a8528-122">This is called a deep traversal.</span></span>  <br/> |
|<span data-ttu-id="a8528-123">SoftDeleted</span><span class="sxs-lookup"><span data-stu-id="a8528-123">SoftDeleted</span></span>  <br/> |<span data-ttu-id="a8528-124">Weist den Vorgang FindFolder flache durchqueren Suchmethode für gelöschte Elemente.</span><span class="sxs-lookup"><span data-stu-id="a8528-124">Instructs the FindFolder operation to perform a shallow traversal search for deleted items.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a8528-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a8528-125">Child elements</span></span>

|<span data-ttu-id="a8528-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="a8528-126">**Element**</span></span>|<span data-ttu-id="a8528-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a8528-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8528-128">FolderShape</span><span class="sxs-lookup"><span data-stu-id="a8528-128">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="a8528-129">Gibt die Eigenschaften des Ordners in einer Antwort FindFolder aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="a8528-129">Identifies the folder properties to include in a FindFolder response.</span></span>  <br/> |
|[<span data-ttu-id="a8528-130">IndexedPageFolderView</span><span class="sxs-lookup"><span data-stu-id="a8528-130">IndexedPageFolderView</span></span>](indexedpagefolderview.md) <br/> |<span data-ttu-id="a8528-131">Beschreibt, wie ausgelagerten Elementinformationen in einer FindFolder Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a8528-131">Describes how paged item information is returned in a FindFolder response.</span></span> <span data-ttu-id="a8528-132">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8528-132">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a8528-133">FractionalPageFolderView</span><span class="sxs-lookup"><span data-stu-id="a8528-133">FractionalPageFolderView</span></span>](fractionalpagefolderview.md) <br/> |<span data-ttu-id="a8528-134">Beschreibt, in der Seitenansicht startet und die maximale Anzahl von Ordnern in einer Anforderung FindFolder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a8528-134">Describes where the paged view starts and the maximum number of folders returned in a FindFolder request.</span></span> <span data-ttu-id="a8528-135">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8528-135">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a8528-136">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="a8528-136">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="a8528-137">Definiert eine Einschränkung oder Abfrage, die zum Filtern von Ordnern in einem Vorgang FindFolder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a8528-137">Defines a restriction or query that is used to filter folders in a FindFolder operation.</span></span> <span data-ttu-id="a8528-138">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8528-138">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a8528-139">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="a8528-139">ParentFolderIds</span></span>](parentfolderids.md) <br/> |<span data-ttu-id="a8528-140">Ordner für den Vorgang FindFolder suchen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a8528-140">Identifies folders for the FindFolder operation to search.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a8528-141">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a8528-141">Parent elements</span></span>

<span data-ttu-id="a8528-142">Keine.</span><span class="sxs-lookup"><span data-stu-id="a8528-142">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8528-143">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a8528-143">Remarks</span></span>

<span data-ttu-id="a8528-144">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a8528-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="a8528-145">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a8528-145">Example</span></span>

<span data-ttu-id="a8528-146">Im folgenden Beispiel wird eine Anforderung FindFolder veranschaulicht eine Anforderung an alle Ordner befindet sich im Posteingang suchen bilden.</span><span class="sxs-lookup"><span data-stu-id="a8528-146">The following example of a FindFolder request shows how to form a request to find all the folders located in an Inbox.</span></span>
  
```
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

## <a name="element-information"></a><span data-ttu-id="a8528-147">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a8528-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8528-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8528-148">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a8528-149">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a8528-149">Schema Name</span></span>  <br/> |<span data-ttu-id="a8528-150">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a8528-150">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a8528-151">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a8528-151">Validation File</span></span>  <br/> |<span data-ttu-id="a8528-152">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a8528-152">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a8528-153">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a8528-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="a8528-154">False</span><span class="sxs-lookup"><span data-stu-id="a8528-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8528-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8528-155">See also</span></span>



[<span data-ttu-id="a8528-156">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="a8528-156">FindFolder operation</span></span>](findfolder-operation.md)

