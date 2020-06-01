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
description: Das FolderShape-Element identifiziert die Ordner Eigenschaften, die in einer GetFolder-, FindFolder-oder SyncFolderHierarchy-Antwort enthalten sein sollen.
ms.openlocfilehash: f841fcc4570604c474387dfa24ec07c9d2784f62
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461345"
---
# <a name="foldershape"></a><span data-ttu-id="2f406-103">FolderShape</span><span class="sxs-lookup"><span data-stu-id="2f406-103">FolderShape</span></span>

<span data-ttu-id="2f406-104">Das **FolderShape** -Element identifiziert die Ordner Eigenschaften, die in einer [GetFolder](getfolder.md)-, [FindFolder](findfolder.md)-oder [SyncFolderHierarchy](syncfolderhierarchy.md) -Antwort enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="2f406-104">The **FolderShape** element identifies the folder properties to include in a [GetFolder](getfolder.md), [FindFolder](findfolder.md), or [SyncFolderHierarchy](syncfolderhierarchy.md) response.</span></span> 
  
```xml
<FolderShape>
   <BaseShape/>
   <AdditionalProperties/>
</FolderShape>
```

 <span data-ttu-id="2f406-105">**FolderResponseShapeType**</span><span class="sxs-lookup"><span data-stu-id="2f406-105">**FolderResponseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2f406-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2f406-106">Attributes and elements</span></span>

<span data-ttu-id="2f406-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2f406-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f406-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2f406-108">Attributes</span></span>

<span data-ttu-id="2f406-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2f406-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2f406-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2f406-110">Child elements</span></span>

|<span data-ttu-id="2f406-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2f406-111">**Element**</span></span>|<span data-ttu-id="2f406-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f406-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f406-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="2f406-113">BaseShape</span></span>](baseshape.md) <br/> |<span data-ttu-id="2f406-114">Gibt die grundlegende Konfiguration von Eigenschaften an, die in einer Antwort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2f406-114">Identifies the basic configuration of properties to return in a response.</span></span>  <br/> |
|[<span data-ttu-id="2f406-115">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="2f406-115">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="2f406-116">Identifiziert zusätzliche Eigenschaften, die in einer Antwort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2f406-116">Identifies additional properties to return in a response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2f406-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2f406-117">Parent elements</span></span>

|<span data-ttu-id="2f406-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="2f406-118">**Element**</span></span>|<span data-ttu-id="2f406-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f406-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f406-120">FindFolder</span><span class="sxs-lookup"><span data-stu-id="2f406-120">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="2f406-121">Definiert eine Anforderung zum Identifizieren von Ordnern in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="2f406-121">Defines a request to identify folders in a mailbox.</span></span>  <br/> <span data-ttu-id="2f406-122">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="2f406-122">The following is the XPath expression to this element:</span></span>  <br/>  `/FindFolder` <br/> |
|[<span data-ttu-id="2f406-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="2f406-123">GetFolder</span></span>](getfolder.md) <br/> |<span data-ttu-id="2f406-124">Definiert eine Anforderung zum Abrufen eines Ordners aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="2f406-124">Defines a request to get a folder from the Exchange store.</span></span>  <br/> <span data-ttu-id="2f406-125">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="2f406-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetFolder` <br/> |
|[<span data-ttu-id="2f406-126">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="2f406-126">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md) <br/> |<span data-ttu-id="2f406-127">Definiert eine Anforderung zum Synchronisieren einer Ordnerhierarchie auf einem Client.</span><span class="sxs-lookup"><span data-stu-id="2f406-127">Defines a request to synchronize a folder hierarchy on a client.</span></span>  <br/> <span data-ttu-id="2f406-128">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="2f406-128">The following is the XPath expression to this element:</span></span>  <br/>  `/SyncFolderHierarchy` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f406-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f406-129">Remarks</span></span>

<span data-ttu-id="2f406-130">Das **FolderShape** -Element ist ein erforderliches untergeordnetes Element des [FindFolder](findfolder.md) -Elements.</span><span class="sxs-lookup"><span data-stu-id="2f406-130">The **FolderShape** element is a required child element of the [FindFolder](findfolder.md) element.</span></span> 
  
<span data-ttu-id="2f406-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="2f406-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="2f406-132">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2f406-132">Example</span></span>

<span data-ttu-id="2f406-133">Im folgenden Beispiel einer Anforderung wird veranschaulicht, wie alle Ordner gefunden werden, die sich auf der ersten Ebene des Posteingangsordners befinden.</span><span class="sxs-lookup"><span data-stu-id="2f406-133">The following example of a request demonstrates how to find all folders located in the first level of the Inbox folder.</span></span>
  
```
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

## <a name="element-information"></a><span data-ttu-id="2f406-134">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2f406-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f406-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f406-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2f406-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2f406-136">Schema Name</span></span>  <br/> |<span data-ttu-id="2f406-137">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2f406-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2f406-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2f406-138">Validation File</span></span>  <br/> |<span data-ttu-id="2f406-139">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2f406-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2f406-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2f406-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="2f406-141">False</span><span class="sxs-lookup"><span data-stu-id="2f406-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f406-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f406-142">See also</span></span>



[<span data-ttu-id="2f406-143">FindFolder</span><span class="sxs-lookup"><span data-stu-id="2f406-143">FindFolder</span></span>](findfolder.md)

