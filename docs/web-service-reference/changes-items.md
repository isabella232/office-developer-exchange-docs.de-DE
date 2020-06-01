---
title: Änderungen (Elemente)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Changes
api_type:
- schema
ms.assetid: d3139fef-0455-4b89-babd-5d6783b50a58
description: Das Changes-Element enthält ein Sequenz Array von Änderungstypen, die die Arten von Unterschieden zwischen den Elementen auf dem Client und den Elementen auf dem Exchange-Server darstellen.
ms.openlocfilehash: 6fda7b5602f172bae84ad7b211db2811def4f883
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463265"
---
# <a name="changes-items"></a><span data-ttu-id="75749-103">Änderungen (Elemente)</span><span class="sxs-lookup"><span data-stu-id="75749-103">Changes (Items)</span></span>

<span data-ttu-id="75749-104">Das **Changes** -Element enthält ein Sequenz Array von Änderungstypen, die die Arten von Unterschieden zwischen den Elementen auf dem Client und den Elementen auf dem Exchange-Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="75749-104">The **Changes** element contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span> 
  
[<span data-ttu-id="75749-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="75749-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
  
[<span data-ttu-id="75749-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="75749-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="75749-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="75749-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
  
[<span data-ttu-id="75749-108">Änderungen (Elemente)</span><span class="sxs-lookup"><span data-stu-id="75749-108">Changes (Items)</span></span>](changes-items.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
</Changes>
```

 <span data-ttu-id="75749-109">**SyncFolderItemsChangesType**</span><span class="sxs-lookup"><span data-stu-id="75749-109">**SyncFolderItemsChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="75749-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="75749-110">Attributes and elements</span></span>

<span data-ttu-id="75749-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="75749-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="75749-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="75749-112">Attributes</span></span>

<span data-ttu-id="75749-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="75749-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="75749-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="75749-114">Child elements</span></span>

|<span data-ttu-id="75749-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="75749-115">**Element**</span></span>|<span data-ttu-id="75749-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="75749-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="75749-117">Erstellen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="75749-117">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="75749-118">Identifiziert ein einzelnes Element, das im lokalen Clientspeicher erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="75749-118">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="75749-119">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="75749-119">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="75749-120">Identifiziert ein einzelnes Element, das im lokalen Clientspeicher aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="75749-120">Identifies a single item to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="75749-121">Delete (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="75749-121">Delete (ItemSync)</span></span>](delete-itemsync.md) <br/> |<span data-ttu-id="75749-122">Identifiziert ein einzelnes Element, das im lokalen Clientspeicher gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="75749-122">Identifies a single item to delete in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="75749-123">ReadFlagChange</span><span class="sxs-lookup"><span data-stu-id="75749-123">ReadFlagChange</span></span>](readflagchange.md) <br/> |<span data-ttu-id="75749-124">Wird in [SyncFolderItems-Vorgangs](syncfolderitems-operation.md) Antworten zurückgegeben, wenn ein Element gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="75749-124">Returned in [SyncFolderItems operation](syncfolderitems-operation.md) responses when an item has been read.</span></span> <span data-ttu-id="75749-125">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="75749-125">This property is read-only.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="75749-126">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="75749-126">Parent elements</span></span>

|<span data-ttu-id="75749-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="75749-127">**Element**</span></span>|<span data-ttu-id="75749-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="75749-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="75749-129">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="75749-129">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md) <br/> |<span data-ttu-id="75749-130">Enthält den Status und das Ergebnis einer [SyncFolderItems-Vorgangs](syncfolderitems-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="75749-130">Contains the status and result of a [SyncFolderItems operation](syncfolderitems-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75749-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75749-131">Remarks</span></span>

<span data-ttu-id="75749-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="75749-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="75749-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="75749-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75749-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="75749-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="75749-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="75749-135">Schema name</span></span>  <br/> |<span data-ttu-id="75749-136">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="75749-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="75749-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="75749-137">Validation file</span></span>  <br/> |<span data-ttu-id="75749-138">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="75749-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="75749-139">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="75749-139">Can be empty</span></span>  <br/> |<span data-ttu-id="75749-140">False</span><span class="sxs-lookup"><span data-stu-id="75749-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="75749-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75749-141">See also</span></span>



[<span data-ttu-id="75749-142">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="75749-142">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="75749-143">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="75749-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

