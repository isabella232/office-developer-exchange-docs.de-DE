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
description: Das SyncFolderItems-Element definiert eine Anforderung zum Synchronisieren von Elementen in einem Exchange-Informationsspeicher Ordner.
ms.openlocfilehash: 0fa5b1544d5627d1423287369e72f97662c28d12
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465149"
---
# <a name="syncfolderitems"></a><span data-ttu-id="81218-103">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="81218-103">SyncFolderItems</span></span>

<span data-ttu-id="81218-104">Das **SyncFolderItems** -Element definiert eine Anforderung zum Synchronisieren von Elementen in einem Exchange-Informationsspeicher Ordner.</span><span class="sxs-lookup"><span data-stu-id="81218-104">The **SyncFolderItems** element defines a request to synchronize items in an Exchange store folder.</span></span> 
  
```xml
<SyncFolderItems>
   <ItemShape/>
   <SyncFolderId/>
   <SyncState/>
   <Ignore/>
   <MaxChangesReturned/>   <SyncScope/>
</SyncFolderItems>
```

 <span data-ttu-id="81218-105">**SyncFolderItemsType**</span><span class="sxs-lookup"><span data-stu-id="81218-105">**SyncFolderItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="81218-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="81218-106">Attributes and elements</span></span>

<span data-ttu-id="81218-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="81218-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="81218-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="81218-108">Attributes</span></span>

<span data-ttu-id="81218-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="81218-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="81218-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="81218-110">Child elements</span></span>

|<span data-ttu-id="81218-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="81218-111">**Element**</span></span>|<span data-ttu-id="81218-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="81218-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81218-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="81218-113">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="81218-114">Identifiziert die Elementeigenschaften und Inhalte, die in einer SyncFolderItems-Antwort enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="81218-114">Identifies the item properties and content to include in a SyncFolderItems response.</span></span> <span data-ttu-id="81218-115">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="81218-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="81218-116">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="81218-116">SyncFolderId</span></span>](syncfolderid.md) <br/> |<span data-ttu-id="81218-117">Stellt den Ordner dar, der die zu synchronisierenden Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="81218-117">Represents the folder that contains the items to synchronize.</span></span> <span data-ttu-id="81218-118">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="81218-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="81218-119">Von "SyncState</span><span class="sxs-lookup"><span data-stu-id="81218-119">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="81218-120">Enthält eine Base64-codierte Form der Synchronisierungsdaten, die nach jeder erfolgreichen Anforderung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="81218-120">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="81218-121">Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="81218-121">This is used to identify the synchronization state.</span></span> <span data-ttu-id="81218-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="81218-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="81218-123">Ignore</span><span class="sxs-lookup"><span data-stu-id="81218-123">Ignore</span></span>](ignore.md) <br/> |<span data-ttu-id="81218-124">Identifiziert Elemente, die während der Synchronisierung übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="81218-124">Identifies items to skip during synchronization.</span></span> <span data-ttu-id="81218-125">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="81218-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="81218-126">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="81218-126">MaxChangesReturned</span></span>](maxchangesreturned.md) <br/> |<span data-ttu-id="81218-127">Beschreibt die maximale Anzahl von Änderungen, die in einer Synchronisierungsantwort zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="81218-127">Describes the maximum number of changes that can be returned in a synchronization response.</span></span> <span data-ttu-id="81218-128">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="81218-128">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="81218-129">SyncScope</span><span class="sxs-lookup"><span data-stu-id="81218-129">SyncScope</span></span>](syncscope.md) <br/> |<span data-ttu-id="81218-130">Gibt an, ob nur Elemente oder Elemente und Ordner zugeordnete Informationen in einer Synchronisierungsantwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="81218-130">Specifies whether just items or items and folder associated information are returned in a synchronization response.</span></span> <span data-ttu-id="81218-131">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="81218-131">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="81218-132">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="81218-132">Parent elements</span></span>

<span data-ttu-id="81218-133">Keine.</span><span class="sxs-lookup"><span data-stu-id="81218-133">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="81218-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81218-134">Remarks</span></span>

<span data-ttu-id="81218-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="81218-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="81218-136">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="81218-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81218-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="81218-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="81218-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="81218-138">Schema name</span></span>  <br/> |<span data-ttu-id="81218-139">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="81218-139">messages schema</span></span>  <br/> |
|<span data-ttu-id="81218-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="81218-140">Validation file</span></span>  <br/> |<span data-ttu-id="81218-141">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="81218-141">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="81218-142">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="81218-142">Can be empty</span></span>  <br/> |<span data-ttu-id="81218-143">False</span><span class="sxs-lookup"><span data-stu-id="81218-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81218-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81218-144">See also</span></span>



[<span data-ttu-id="81218-145">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="81218-145">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="81218-146">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="81218-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

