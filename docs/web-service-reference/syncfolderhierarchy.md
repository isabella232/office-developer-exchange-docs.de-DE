---
title: SyncFolderHierarchy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchy
api_type:
- schema
ms.assetid: 55df4d01-e48e-4263-a851-78a66ad1093a
description: Das SyncFolderHierarchy-Element definiert eine Anforderung zum Synchronisieren einer Ordnerhierarchie auf einem Client an.
ms.openlocfilehash: f72640e5605dd83e92cd323cb00e4d2f64406245
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839146"
---
# <a name="syncfolderhierarchy"></a><span data-ttu-id="a8390-103">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="a8390-103">SyncFolderHierarchy</span></span>

<span data-ttu-id="a8390-104">Das **SyncFolderHierarchy** -Element definiert eine Anforderung zum Synchronisieren einer Ordnerhierarchie auf einem Client an.</span><span class="sxs-lookup"><span data-stu-id="a8390-104">The **SyncFolderHierarchy** element defines a request to synchronize a folder hierarchy on a client.</span></span> 
  
```xml
<SyncFolderHierarchy>
   <FolderShape/>   <SyncFolderId/>
   <SyncState/>
</SyncFolderHierarchy>
```

 <span data-ttu-id="a8390-105">**SyncFolderHierarchyType**</span><span class="sxs-lookup"><span data-stu-id="a8390-105">**SyncFolderHierarchyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a8390-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a8390-106">Attributes and elements</span></span>

<span data-ttu-id="a8390-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a8390-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8390-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a8390-108">Attributes</span></span>

<span data-ttu-id="a8390-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a8390-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a8390-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a8390-110">Child elements</span></span>

|<span data-ttu-id="a8390-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a8390-111">**Element**</span></span>|<span data-ttu-id="a8390-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a8390-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8390-113">FolderShape</span><span class="sxs-lookup"><span data-stu-id="a8390-113">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="a8390-114">Gibt die Eigenschaften des Ordners in einer Antwort [SyncFolderHierarchy](syncfolderhierarchy.md) aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="a8390-114">Identifies the folder properties to include in a [SyncFolderHierarchy](syncfolderhierarchy.md) response.</span></span>  <br/> |
|[<span data-ttu-id="a8390-115">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="a8390-115">SyncFolderId</span></span>](syncfolderid.md) <br/> |<span data-ttu-id="a8390-116">Stellt den Ordner, der zu synchronisierenden Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="a8390-116">Represents the folder that contains the items to synchronize.</span></span> <span data-ttu-id="a8390-117">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8390-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a8390-118">Synchronisierungsstatus</span><span class="sxs-lookup"><span data-stu-id="a8390-118">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a8390-119">Enthält eine base64-codierten Format von der Synchronisierung von Daten, die nach jeder Anforderung erfolgreich aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a8390-119">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="a8390-120">Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a8390-120">This is used to identify the synchronization state.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a8390-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a8390-121">Parent elements</span></span>

<span data-ttu-id="a8390-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="a8390-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8390-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a8390-123">Remarks</span></span>

<span data-ttu-id="a8390-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a8390-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a8390-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a8390-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8390-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8390-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a8390-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a8390-127">Schema name</span></span>  <br/> |<span data-ttu-id="a8390-128">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a8390-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a8390-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a8390-129">Validation file</span></span>  <br/> |<span data-ttu-id="a8390-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a8390-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a8390-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a8390-131">Can be empty</span></span>  <br/> |<span data-ttu-id="a8390-132">False</span><span class="sxs-lookup"><span data-stu-id="a8390-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8390-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8390-133">See also</span></span>



[<span data-ttu-id="a8390-134">SyncFolderHierarchy-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a8390-134">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


- [<span data-ttu-id="a8390-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a8390-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

