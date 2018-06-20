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
description: Das Änderungen-Element enthält ein Array Sequenz von Dateitypen ändern, die die Typen der Unterschiede zwischen den Elementen auf dem Client und der Elemente auf dem Exchange-Server darstellen.
ms.openlocfilehash: 8e38597276e3e3051a5c1494619d3220280e401f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757561"
---
# <a name="changes-items"></a><span data-ttu-id="d9cc6-103">Änderungen (Elemente)</span><span class="sxs-lookup"><span data-stu-id="d9cc6-103">Changes (Items)</span></span>

<span data-ttu-id="d9cc6-104">Das **Änderungen** -Element enthält ein Array Sequenz von Dateitypen ändern, die die Typen der Unterschiede zwischen den Elementen auf dem Client und der Elemente auf dem Exchange-Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="d9cc6-104">The **Changes** element contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span> 
  
[<span data-ttu-id="d9cc6-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="d9cc6-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
  
[<span data-ttu-id="d9cc6-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d9cc6-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="d9cc6-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d9cc6-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
  
[<span data-ttu-id="d9cc6-108">Änderungen (Elemente)</span><span class="sxs-lookup"><span data-stu-id="d9cc6-108">Changes (Items)</span></span>](changes-items.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
</Changes>
```

 <span data-ttu-id="d9cc6-109">**SyncFolderItemsChangesType**</span><span class="sxs-lookup"><span data-stu-id="d9cc6-109">**SyncFolderItemsChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d9cc6-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d9cc6-110">Attributes and elements</span></span>

<span data-ttu-id="d9cc6-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d9cc6-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9cc6-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="d9cc6-112">Attributes</span></span>

<span data-ttu-id="d9cc6-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="d9cc6-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d9cc6-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d9cc6-114">Child elements</span></span>

|<span data-ttu-id="d9cc6-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="d9cc6-115">**Element**</span></span>|<span data-ttu-id="d9cc6-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d9cc6-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9cc6-117">Erstellen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="d9cc6-117">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="d9cc6-118">Gibt ein einzelnes Element in der lokalen Client-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d9cc6-118">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="d9cc6-119">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="d9cc6-119">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="d9cc6-120">Gibt ein einzelnes Element in den Speicher des lokalen Client aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d9cc6-120">Identifies a single item to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="d9cc6-121">Löschen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="d9cc6-121">Delete (ItemSync)</span></span>](delete-itemsync.md) <br/> |<span data-ttu-id="d9cc6-122">Gibt ein einzelnes Element in der lokalen Client-Speicher zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d9cc6-122">Identifies a single item to delete in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="d9cc6-123">ReadFlagChange</span><span class="sxs-lookup"><span data-stu-id="d9cc6-123">ReadFlagChange</span></span>](readflagchange.md) <br/> |<span data-ttu-id="d9cc6-124">In [SyncFolderItems Vorgang](syncfolderitems-operation.md) Antworten zurückgegeben, wenn ein Element gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="d9cc6-124">Returned in [SyncFolderItems operation](syncfolderitems-operation.md) responses when an item has been read.</span></span> <span data-ttu-id="d9cc6-125">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d9cc6-125">This property is read-only.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d9cc6-126">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d9cc6-126">Parent elements</span></span>

|<span data-ttu-id="d9cc6-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="d9cc6-127">**Element**</span></span>|<span data-ttu-id="d9cc6-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d9cc6-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9cc6-129">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d9cc6-129">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md) <br/> |<span data-ttu-id="d9cc6-130">Enthält den Status und das Ergebnis einer Anforderung [SyncFolderItems Vorgang](syncfolderitems-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d9cc6-130">Contains the status and result of a [SyncFolderItems operation](syncfolderitems-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9cc6-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9cc6-131">Remarks</span></span>

<span data-ttu-id="d9cc6-132">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d9cc6-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d9cc6-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d9cc6-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9cc6-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="d9cc6-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d9cc6-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d9cc6-135">Schema name</span></span>  <br/> |<span data-ttu-id="d9cc6-136">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d9cc6-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d9cc6-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d9cc6-137">Validation file</span></span>  <br/> |<span data-ttu-id="d9cc6-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d9cc6-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d9cc6-139">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d9cc6-139">Can be empty</span></span>  <br/> |<span data-ttu-id="d9cc6-140">False</span><span class="sxs-lookup"><span data-stu-id="d9cc6-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9cc6-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9cc6-141">See also</span></span>



[<span data-ttu-id="d9cc6-142">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d9cc6-142">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="d9cc6-143">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d9cc6-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

