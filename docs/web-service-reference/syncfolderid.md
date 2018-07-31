---
title: SyncFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderId
api_type:
- schema
ms.assetid: 3645fa03-236d-4e5f-b8b9-5d98f7f35fa2
description: Das SyncFolderId-Element darstellt, den Ordner, der zu synchronisierenden Elemente enthält.
ms.openlocfilehash: c90a20095ca4706f0c6edae3e98eaadd6024d817
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354400"
---
# <a name="syncfolderid"></a><span data-ttu-id="8aa1b-103">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="8aa1b-103">SyncFolderId</span></span>

<span data-ttu-id="8aa1b-104">Das **SyncFolderId** -Element darstellt, den Ordner, der zu synchronisierenden Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="8aa1b-104">The **SyncFolderId** element represents the folder that contains the items to synchronize.</span></span> 
  
```xml
<SyncFolderId>
   <FolderId/>
</SyncFolderId>
```

```xml
<SyncFolderId>
   <DistinguishedFolderId/> 
</SyncFolderId>
```

<span data-ttu-id="8aa1b-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="8aa1b-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="8aa1b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8aa1b-106">Attributes and elements</span></span>

<span data-ttu-id="8aa1b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8aa1b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8aa1b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8aa1b-108">Attributes</span></span>

<span data-ttu-id="8aa1b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8aa1b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8aa1b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8aa1b-110">Child elements</span></span>

|<span data-ttu-id="8aa1b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8aa1b-111">**Element**</span></span>|<span data-ttu-id="8aa1b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8aa1b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8aa1b-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="8aa1b-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="8aa1b-114">Enthält den Schlüssel-ID und Ändern eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="8aa1b-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="8aa1b-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="8aa1b-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="8aa1b-116">Identifiziert MicrosoftExchange Server 2007-Ordner, die nach Namen verwiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="8aa1b-116">Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8aa1b-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8aa1b-117">Parent elements</span></span>

|<span data-ttu-id="8aa1b-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="8aa1b-118">**Element**</span></span>|<span data-ttu-id="8aa1b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8aa1b-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8aa1b-120">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="8aa1b-120">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md) <br/> |<span data-ttu-id="8aa1b-121">Definiert eine Anforderung zum Synchronisieren einer Ordnerhierarchie in einen Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="8aa1b-121">Defines a request to synchronize a folder hierarchy in an Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8aa1b-122">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="8aa1b-122">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="8aa1b-123">Definiert eine Anforderung zum Synchronisieren von Elementen in einem Ordner von Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="8aa1b-123">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8aa1b-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8aa1b-124">Remarks</span></span>

<span data-ttu-id="8aa1b-125">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8aa1b-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8aa1b-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8aa1b-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8aa1b-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="8aa1b-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8aa1b-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8aa1b-128">Schema name</span></span>  <br/> |<span data-ttu-id="8aa1b-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8aa1b-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8aa1b-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8aa1b-130">Validation file</span></span>  <br/> |<span data-ttu-id="8aa1b-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8aa1b-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8aa1b-132">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8aa1b-132">Can be empty</span></span>  <br/> |<span data-ttu-id="8aa1b-133">False</span><span class="sxs-lookup"><span data-stu-id="8aa1b-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8aa1b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8aa1b-134">See also</span></span>

- [<span data-ttu-id="8aa1b-135">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8aa1b-135">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="8aa1b-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8aa1b-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

