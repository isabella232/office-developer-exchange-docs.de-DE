---
title: Von "SyncState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncState
api_type:
- schema
ms.assetid: e5ebaae3-0f07-481d-ac67-d9687a3c7ac3
description: Das von "SyncState-Element enthält eine Base64-codierte Form der Synchronisierungsdaten, die nach jeder erfolgreichen Anforderung aktualisiert wird. Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren.
ms.openlocfilehash: 8e2d9a633cdad0a124b87e4e794399c06d3b5445
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458964"
---
# <a name="syncstate"></a><span data-ttu-id="f9077-104">Von "SyncState</span><span class="sxs-lookup"><span data-stu-id="f9077-104">SyncState</span></span>

<span data-ttu-id="f9077-105">Das **von "SyncState** -Element enthält eine Base64-codierte Form der Synchronisierungsdaten, die nach jeder erfolgreichen Anforderung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f9077-105">The **SyncState** element contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="f9077-106">Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f9077-106">This is used to identify the synchronization state.</span></span> 
  
```xml
<SyncState/>
```

 <span data-ttu-id="f9077-107">**String**</span><span class="sxs-lookup"><span data-stu-id="f9077-107">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f9077-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f9077-108">Attributes and elements</span></span>

<span data-ttu-id="f9077-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f9077-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f9077-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="f9077-110">Attributes</span></span>

<span data-ttu-id="f9077-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f9077-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f9077-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9077-112">Child elements</span></span>

<span data-ttu-id="f9077-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="f9077-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f9077-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9077-114">Parent elements</span></span>

|<span data-ttu-id="f9077-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="f9077-115">**Element**</span></span>|<span data-ttu-id="f9077-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f9077-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9077-117">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="f9077-117">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md) <br/> |<span data-ttu-id="f9077-118">Definiert eine Anforderung zum Synchronisieren einer Ordnerhierarchie auf einem Client.</span><span class="sxs-lookup"><span data-stu-id="f9077-118">Defines a request to synchronize a folder hierarchy on a client.</span></span>  <br/> |
|[<span data-ttu-id="f9077-119">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f9077-119">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md) <br/> |<span data-ttu-id="f9077-120">Enthält den Status und das Ergebnis einer SyncFolderHierarchy-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f9077-120">Contains the status and result of a SyncFolderHierarchy request.</span></span>  <br/> |
|[<span data-ttu-id="f9077-121">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="f9077-121">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="f9077-122">Definiert eine Anforderung zum Synchronisieren von Elementen in einem Exchange-Informationsspeicher Ordner.</span><span class="sxs-lookup"><span data-stu-id="f9077-122">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
|[<span data-ttu-id="f9077-123">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f9077-123">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md) <br/> |<span data-ttu-id="f9077-124">Enthält den Status und das Ergebnis einer SyncFolderItems-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f9077-124">Contains the status and result of a SyncFolderItems request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f9077-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="f9077-125">Text value</span></span>

<span data-ttu-id="f9077-126">Ein Textwert ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f9077-126">A text value is required when this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f9077-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9077-127">Remarks</span></span>

<span data-ttu-id="f9077-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f9077-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f9077-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f9077-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9077-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="f9077-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f9077-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f9077-131">Schema name</span></span>  <br/> |<span data-ttu-id="f9077-132">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f9077-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f9077-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f9077-133">Validation file</span></span>  <br/> |<span data-ttu-id="f9077-134">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f9077-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f9077-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f9077-135">Can be empty</span></span>  <br/> |<span data-ttu-id="f9077-136">False</span><span class="sxs-lookup"><span data-stu-id="f9077-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f9077-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9077-137">See also</span></span>



[<span data-ttu-id="f9077-138">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f9077-138">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
  
[<span data-ttu-id="f9077-139">SyncFolderHierarchy-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f9077-139">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


- [<span data-ttu-id="f9077-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f9077-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

