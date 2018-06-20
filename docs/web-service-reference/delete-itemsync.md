---
title: Löschen (ItemSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Delete
api_type:
- schema
ms.assetid: 4f372d57-2e39-46af-9d83-6c8c55108587
description: Das Delete-Element identifiziert ein einzelnes Element in der lokalen Client-Speicher zu löschen.
ms.openlocfilehash: 18b7ae2f97db2de64896680c3aa76f2590c03177
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757907"
---
# <a name="delete-itemsync"></a><span data-ttu-id="d32b2-103">Löschen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="d32b2-103">Delete (ItemSync)</span></span>

<span data-ttu-id="d32b2-104">Das **Löschen** -Element identifiziert ein einzelnes Element in der lokalen Client-Speicher zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d32b2-104">The **Delete** element identifies a single item to delete in the local client store.</span></span> 
  
- [<span data-ttu-id="d32b2-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="d32b2-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)  
- [<span data-ttu-id="d32b2-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d32b2-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="d32b2-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d32b2-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)  
- [<span data-ttu-id="d32b2-108">Änderungen (Elemente)</span><span class="sxs-lookup"><span data-stu-id="d32b2-108">Changes (Items)</span></span>](changes-items.md)  
- [<span data-ttu-id="d32b2-109">Löschen (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="d32b2-109">Delete (ItemSync)</span></span>](delete-itemsync.md)
  
```xml
<Delete>
   <ItemId/>
</Delete>
```

<span data-ttu-id="d32b2-110">**SyncFolderItemsDeleteType**</span><span class="sxs-lookup"><span data-stu-id="d32b2-110">**SyncFolderItemsDeleteType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d32b2-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d32b2-111">Attributes and elements</span></span>

<span data-ttu-id="d32b2-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d32b2-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d32b2-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="d32b2-113">Attributes</span></span>

<span data-ttu-id="d32b2-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="d32b2-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d32b2-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d32b2-115">Child elements</span></span>

|<span data-ttu-id="d32b2-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d32b2-116">**Element**</span></span>|<span data-ttu-id="d32b2-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d32b2-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d32b2-118">ItemId</span><span class="sxs-lookup"><span data-stu-id="d32b2-118">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="d32b2-119">Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="d32b2-119">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d32b2-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d32b2-120">Parent elements</span></span>

|<span data-ttu-id="d32b2-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="d32b2-121">**Element**</span></span>|<span data-ttu-id="d32b2-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d32b2-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d32b2-123">Änderungen (Elemente)</span><span class="sxs-lookup"><span data-stu-id="d32b2-123">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="d32b2-124">Enthält ein Array Sequenz von Dateitypen ändern, die den Typ der Unterschiede zwischen den Elementen auf dem Client und der Elemente auf dem Exchange-Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="d32b2-124">Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d32b2-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d32b2-125">Remarks</span></span>

<span data-ttu-id="d32b2-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d32b2-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d32b2-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d32b2-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d32b2-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="d32b2-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d32b2-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d32b2-129">Schema name</span></span>  <br/> |<span data-ttu-id="d32b2-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d32b2-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="d32b2-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d32b2-131">Validation file</span></span>  <br/> |<span data-ttu-id="d32b2-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d32b2-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d32b2-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d32b2-133">Can be empty</span></span>  <br/> |<span data-ttu-id="d32b2-134">False</span><span class="sxs-lookup"><span data-stu-id="d32b2-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d32b2-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d32b2-135">See also</span></span>

- [<span data-ttu-id="d32b2-136">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d32b2-136">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="d32b2-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d32b2-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

