---
title: FolderShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderShape
api_type:
- schema
ms.assetid: 244f4f46-a33d-4764-92e3-1bddb4dc6a49
description: Das FolderShape-Element identifiziert die Ordnereigenschaften in einer Antwort GetFolder, FindFolder oder SyncFolderHierarchy aufzunehmen.
ms.openlocfilehash: 8ebdd70ef13ee9f0cce9020b9212576cba782be4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758524"
---
# <a name="foldershape"></a><span data-ttu-id="6c504-103">FolderShape</span><span class="sxs-lookup"><span data-stu-id="6c504-103">FolderShape</span></span>

<span data-ttu-id="6c504-104">Das **FolderShape** -Element identifiziert die Ordnereigenschaften in einer Antwort [GetFolder](getfolder.md), [FindFolder](findfolder.md)oder [SyncFolderHierarchy](syncfolderhierarchy.md) aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="6c504-104">The **FolderShape** element identifies the folder properties to include in a [GetFolder](getfolder.md), [FindFolder](findfolder.md), or [SyncFolderHierarchy](syncfolderhierarchy.md) response.</span></span> 
  
```xml
<FolderShape>
   <BaseShape/>
   <AdditionalProperties/>
</FolderShape>
```

 <span data-ttu-id="6c504-105">**FolderResponseShapeType**</span><span class="sxs-lookup"><span data-stu-id="6c504-105">**FolderResponseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6c504-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6c504-106">Attributes and elements</span></span>

<span data-ttu-id="6c504-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6c504-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6c504-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6c504-108">Attributes</span></span>

<span data-ttu-id="6c504-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6c504-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6c504-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6c504-110">Child elements</span></span>

|<span data-ttu-id="6c504-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6c504-111">**Element**</span></span>|<span data-ttu-id="6c504-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6c504-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6c504-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="6c504-113">BaseShape</span></span>](baseshape.md) <br/> |<span data-ttu-id="6c504-114">Identifiziert die grundlegende Konfiguration von Eigenschaften in einer Antwort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c504-114">Identifies the basic configuration of properties to return in a response.</span></span>  <br/> |
|[<span data-ttu-id="6c504-115">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="6c504-115">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="6c504-116">Bezeichnet die zusätzliche Eigenschaften, die in eine Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c504-116">Identifies additional properties to return in a response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6c504-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6c504-117">Parent elements</span></span>

|<span data-ttu-id="6c504-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="6c504-118">**Element**</span></span>|<span data-ttu-id="6c504-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6c504-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6c504-120">FindFolder</span><span class="sxs-lookup"><span data-stu-id="6c504-120">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="6c504-121">Definiert eine Anforderung zum Ordner in einem Postfach zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6c504-121">Defines a request to identify folders in a mailbox.</span></span>  <br/> <span data-ttu-id="6c504-122">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="6c504-122">The following is the XPath expression to this element:</span></span>  <br/>  `/FindFolder` <br/> |
|[<span data-ttu-id="6c504-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="6c504-123">GetFolder</span></span>](getfolder.md) <br/> |<span data-ttu-id="6c504-124">Definiert eine Anforderung an einen Ordner aus dem Exchange-Speicher abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6c504-124">Defines a request to get a folder from the Exchange store.</span></span>  <br/> <span data-ttu-id="6c504-125">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="6c504-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetFolder` <br/> |
|[<span data-ttu-id="6c504-126">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="6c504-126">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md) <br/> |<span data-ttu-id="6c504-127">Definiert eine Anforderung zum Synchronisieren einer Ordnerhierarchie auf einem Client an.</span><span class="sxs-lookup"><span data-stu-id="6c504-127">Defines a request to synchronize a folder hierarchy on a client.</span></span>  <br/> <span data-ttu-id="6c504-128">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="6c504-128">The following is the XPath expression to this element:</span></span>  <br/>  `/SyncFolderHierarchy` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c504-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6c504-129">Remarks</span></span>

<span data-ttu-id="6c504-130">Das **FolderShape** -Element ist ein erforderliches untergeordnetes Element des Elements [FindFolder](findfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="6c504-130">The **FolderShape** element is a required child element of the [FindFolder](findfolder.md) element.</span></span> 
  
<span data-ttu-id="6c504-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="6c504-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="6c504-132">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6c504-132">Example</span></span>

<span data-ttu-id="6c504-133">Im folgenden Beispiel wird eine Anforderung veranschaulicht, wie alle Ordner in der ersten Ebene des Ordners Posteingang zu suchen.</span><span class="sxs-lookup"><span data-stu-id="6c504-133">The following example of a request demonstrates how to find all folders located in the first level of the Inbox folder.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="6c504-134">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6c504-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c504-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c504-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6c504-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6c504-136">Schema Name</span></span>  <br/> |<span data-ttu-id="6c504-137">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="6c504-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6c504-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6c504-138">Validation File</span></span>  <br/> |<span data-ttu-id="6c504-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6c504-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6c504-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6c504-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="6c504-141">False</span><span class="sxs-lookup"><span data-stu-id="6c504-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c504-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c504-142">See also</span></span>



[<span data-ttu-id="6c504-143">FindFolder</span><span class="sxs-lookup"><span data-stu-id="6c504-143">FindFolder</span></span>](findfolder.md)

