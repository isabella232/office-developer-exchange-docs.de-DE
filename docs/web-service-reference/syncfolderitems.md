---
title: SyncFolderItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderItems
api_type:
- schema
ms.assetid: 463ed78c-bf82-4cd8-971a-d18425e9e7be
description: Das SyncFolderItems-Element definiert eine Anforderung zum Synchronisieren von Elementen in einem Ordner von Exchange-Speicher.
ms.openlocfilehash: 368e19babfccaeab40380103495c63d30647905c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839150"
---
# <a name="syncfolderitems"></a><span data-ttu-id="d1093-103">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="d1093-103">SyncFolderItems</span></span>

<span data-ttu-id="d1093-104">Das **SyncFolderItems** -Element definiert eine Anforderung zum Synchronisieren von Elementen in einem Ordner von Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="d1093-104">The **SyncFolderItems** element defines a request to synchronize items in an Exchange store folder.</span></span> 
  
```xml
<SyncFolderItems>
   <ItemShape/>
   <SyncFolderId/>
   <SyncState/>
   <Ignore/>
   <MaxChangesReturned/>   <SyncScope/>
</SyncFolderItems>
```

 <span data-ttu-id="d1093-105">**SyncFolderItemsType**</span><span class="sxs-lookup"><span data-stu-id="d1093-105">**SyncFolderItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d1093-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d1093-106">Attributes and elements</span></span>

<span data-ttu-id="d1093-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d1093-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d1093-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d1093-108">Attributes</span></span>

<span data-ttu-id="d1093-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d1093-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d1093-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d1093-110">Child elements</span></span>

|<span data-ttu-id="d1093-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d1093-111">**Element**</span></span>|<span data-ttu-id="d1093-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d1093-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d1093-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="d1093-113">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="d1093-114">Identifiziert die Elementeigenschaften und den Inhalt in einer Antwort SyncFolderItems aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="d1093-114">Identifies the item properties and content to include in a SyncFolderItems response.</span></span> <span data-ttu-id="d1093-115">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d1093-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="d1093-116">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="d1093-116">SyncFolderId</span></span>](syncfolderid.md) <br/> |<span data-ttu-id="d1093-117">Stellt den Ordner, der zu synchronisierenden Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="d1093-117">Represents the folder that contains the items to synchronize.</span></span> <span data-ttu-id="d1093-118">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d1093-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="d1093-119">Synchronisierungsstatus</span><span class="sxs-lookup"><span data-stu-id="d1093-119">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d1093-120">Enthält eine base64-codierten Format von der Synchronisierung von Daten, die nach jeder Anforderung erfolgreich aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d1093-120">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="d1093-121">Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d1093-121">This is used to identify the synchronization state.</span></span> <span data-ttu-id="d1093-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="d1093-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="d1093-123">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="d1093-123">Ignore</span></span>](ignore.md) <br/> |<span data-ttu-id="d1093-124">Identifiziert Elemente, während der Synchronisierung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="d1093-124">Identifies items to skip during synchronization.</span></span> <span data-ttu-id="d1093-125">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="d1093-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="d1093-126">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="d1093-126">MaxChangesReturned</span></span>](maxchangesreturned.md) <br/> |<span data-ttu-id="d1093-127">Beschreibt die maximale Anzahl von Änderungen, die in einer Synchronisierung Antwort zurückgegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="d1093-127">Describes the maximum number of changes that can be returned in a synchronization response.</span></span> <span data-ttu-id="d1093-128">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d1093-128">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="d1093-129">SyncScope</span><span class="sxs-lookup"><span data-stu-id="d1093-129">SyncScope</span></span>](syncscope.md) <br/> |<span data-ttu-id="d1093-130">Gibt an, ob nur Elemente oder Elemente und verknüpften Ordnerinformationen in eine Synchronisierung Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d1093-130">Specifies whether just items or items and folder associated information are returned in a synchronization response.</span></span> <span data-ttu-id="d1093-131">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="d1093-131">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d1093-132">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d1093-132">Parent elements</span></span>

<span data-ttu-id="d1093-133">Keine.</span><span class="sxs-lookup"><span data-stu-id="d1093-133">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1093-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d1093-134">Remarks</span></span>

<span data-ttu-id="d1093-135">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d1093-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d1093-136">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d1093-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1093-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1093-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d1093-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d1093-138">Schema name</span></span>  <br/> |<span data-ttu-id="d1093-139">Nachrichten-schema</span><span class="sxs-lookup"><span data-stu-id="d1093-139">messages schema</span></span>  <br/> |
|<span data-ttu-id="d1093-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d1093-140">Validation file</span></span>  <br/> |<span data-ttu-id="d1093-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d1093-141">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d1093-142">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d1093-142">Can be empty</span></span>  <br/> |<span data-ttu-id="d1093-143">False</span><span class="sxs-lookup"><span data-stu-id="d1093-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d1093-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1093-144">See also</span></span>



[<span data-ttu-id="d1093-145">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d1093-145">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="d1093-146">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d1093-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

