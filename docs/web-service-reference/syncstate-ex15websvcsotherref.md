---
title: Synchronisierungsstatus
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
description: Das Synchronisierungsstatus-Element enthält eine base64-codierten Format von der Synchronisierung von Daten, die nach jeder Anforderung erfolgreich aktualisiert werden. Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren.
ms.openlocfilehash: 3c600dde09fd813dcfb1f6e74671ebe9004701a1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839155"
---
# <a name="syncstate"></a><span data-ttu-id="f3a9f-104">Synchronisierungsstatus</span><span class="sxs-lookup"><span data-stu-id="f3a9f-104">SyncState</span></span>

<span data-ttu-id="f3a9f-105">Das **Synchronisierungsstatus** -Element enthält eine base64-codierten Format von der Synchronisierung von Daten, die nach jeder Anforderung erfolgreich aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f3a9f-105">The **SyncState** element contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="f3a9f-106">Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f3a9f-106">This is used to identify the synchronization state.</span></span> 
  
```xml
<SyncState/>
```

 <span data-ttu-id="f3a9f-107">**String**</span><span class="sxs-lookup"><span data-stu-id="f3a9f-107">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f3a9f-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f3a9f-108">Attributes and elements</span></span>

<span data-ttu-id="f3a9f-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f3a9f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f3a9f-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="f3a9f-110">Attributes</span></span>

<span data-ttu-id="f3a9f-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f3a9f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f3a9f-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f3a9f-112">Child elements</span></span>

<span data-ttu-id="f3a9f-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="f3a9f-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f3a9f-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f3a9f-114">Parent elements</span></span>

|<span data-ttu-id="f3a9f-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="f3a9f-115">**Element**</span></span>|<span data-ttu-id="f3a9f-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f3a9f-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f3a9f-117">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="f3a9f-117">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md) <br/> |<span data-ttu-id="f3a9f-118">Definiert eine Anforderung zum Synchronisieren einer Ordnerhierarchie auf einem Client an.</span><span class="sxs-lookup"><span data-stu-id="f3a9f-118">Defines a request to synchronize a folder hierarchy on a client.</span></span>  <br/> |
|[<span data-ttu-id="f3a9f-119">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f3a9f-119">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md) <br/> |<span data-ttu-id="f3a9f-120">Enthält den Status und das Ergebnis einer Anforderung SyncFolderHierarchy.</span><span class="sxs-lookup"><span data-stu-id="f3a9f-120">Contains the status and result of a SyncFolderHierarchy request.</span></span>  <br/> |
|[<span data-ttu-id="f3a9f-121">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="f3a9f-121">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="f3a9f-122">Definiert eine Anforderung zum Synchronisieren von Elementen in einem Ordner von Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="f3a9f-122">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
|[<span data-ttu-id="f3a9f-123">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f3a9f-123">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md) <br/> |<span data-ttu-id="f3a9f-124">Enthält den Status und das Ergebnis einer Anforderung SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="f3a9f-124">Contains the status and result of a SyncFolderItems request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f3a9f-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="f3a9f-125">Text value</span></span>

<span data-ttu-id="f3a9f-126">Ein Textwert ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f3a9f-126">A text value is required when this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f3a9f-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f3a9f-127">Remarks</span></span>

<span data-ttu-id="f3a9f-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f3a9f-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f3a9f-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f3a9f-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3a9f-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="f3a9f-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f3a9f-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f3a9f-131">Schema name</span></span>  <br/> |<span data-ttu-id="f3a9f-132">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f3a9f-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f3a9f-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f3a9f-133">Validation file</span></span>  <br/> |<span data-ttu-id="f3a9f-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f3a9f-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f3a9f-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f3a9f-135">Can be empty</span></span>  <br/> |<span data-ttu-id="f3a9f-136">False</span><span class="sxs-lookup"><span data-stu-id="f3a9f-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f3a9f-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3a9f-137">See also</span></span>



[<span data-ttu-id="f3a9f-138">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f3a9f-138">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
  
[<span data-ttu-id="f3a9f-139">SyncFolderHierarchy-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f3a9f-139">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


- [<span data-ttu-id="f3a9f-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f3a9f-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

