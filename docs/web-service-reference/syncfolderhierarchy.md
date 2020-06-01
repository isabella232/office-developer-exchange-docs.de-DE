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
description: Das SyncFolderHierarchy-Element definiert eine Anforderung zum Synchronisieren einer Ordnerhierarchie auf einem Client.
ms.openlocfilehash: 68b607dbf603e955f74dfaccadd3ce6c4c9fb6ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466647"
---
# <a name="syncfolderhierarchy"></a><span data-ttu-id="32af2-103">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="32af2-103">SyncFolderHierarchy</span></span>

<span data-ttu-id="32af2-104">Das **SyncFolderHierarchy** -Element definiert eine Anforderung zum Synchronisieren einer Ordnerhierarchie auf einem Client.</span><span class="sxs-lookup"><span data-stu-id="32af2-104">The **SyncFolderHierarchy** element defines a request to synchronize a folder hierarchy on a client.</span></span> 
  
```xml
<SyncFolderHierarchy>
   <FolderShape/>   <SyncFolderId/>
   <SyncState/>
</SyncFolderHierarchy>
```

 <span data-ttu-id="32af2-105">**SyncFolderHierarchyType**</span><span class="sxs-lookup"><span data-stu-id="32af2-105">**SyncFolderHierarchyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="32af2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="32af2-106">Attributes and elements</span></span>

<span data-ttu-id="32af2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="32af2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="32af2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="32af2-108">Attributes</span></span>

<span data-ttu-id="32af2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="32af2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="32af2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="32af2-110">Child elements</span></span>

|<span data-ttu-id="32af2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="32af2-111">**Element**</span></span>|<span data-ttu-id="32af2-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="32af2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="32af2-113">FolderShape</span><span class="sxs-lookup"><span data-stu-id="32af2-113">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="32af2-114">Gibt die Ordner Eigenschaften an, die in eine [SyncFolderHierarchy](syncfolderhierarchy.md) -Antwort eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="32af2-114">Identifies the folder properties to include in a [SyncFolderHierarchy](syncfolderhierarchy.md) response.</span></span>  <br/> |
|[<span data-ttu-id="32af2-115">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="32af2-115">SyncFolderId</span></span>](syncfolderid.md) <br/> |<span data-ttu-id="32af2-116">Stellt den Ordner dar, der die zu synchronisierenden Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="32af2-116">Represents the folder that contains the items to synchronize.</span></span> <span data-ttu-id="32af2-117">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="32af2-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="32af2-118">Von "SyncState</span><span class="sxs-lookup"><span data-stu-id="32af2-118">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="32af2-119">Enthält eine Base64-codierte Form der Synchronisierungsdaten, die nach jeder erfolgreichen Anforderung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="32af2-119">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="32af2-120">Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="32af2-120">This is used to identify the synchronization state.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="32af2-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="32af2-121">Parent elements</span></span>

<span data-ttu-id="32af2-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="32af2-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="32af2-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32af2-123">Remarks</span></span>

<span data-ttu-id="32af2-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="32af2-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="32af2-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="32af2-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="32af2-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="32af2-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="32af2-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="32af2-127">Schema name</span></span>  <br/> |<span data-ttu-id="32af2-128">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="32af2-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="32af2-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="32af2-129">Validation file</span></span>  <br/> |<span data-ttu-id="32af2-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="32af2-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="32af2-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="32af2-131">Can be empty</span></span>  <br/> |<span data-ttu-id="32af2-132">False</span><span class="sxs-lookup"><span data-stu-id="32af2-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="32af2-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32af2-133">See also</span></span>



[<span data-ttu-id="32af2-134">SyncFolderHierarchy-Vorgang</span><span class="sxs-lookup"><span data-stu-id="32af2-134">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


- [<span data-ttu-id="32af2-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="32af2-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

