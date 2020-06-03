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
description: Das SyncFolderId-Element stellt den Ordner dar, der die zu synchronisierenden Elemente enthält.
ms.openlocfilehash: 35b66579116a00d27df722629ff980471ca0272e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530296"
---
# <a name="syncfolderid"></a><span data-ttu-id="284d7-103">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="284d7-103">SyncFolderId</span></span>

<span data-ttu-id="284d7-104">Das **SyncFolderId** -Element stellt den Ordner dar, der die zu synchronisierenden Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="284d7-104">The **SyncFolderId** element represents the folder that contains the items to synchronize.</span></span> 
  
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

<span data-ttu-id="284d7-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="284d7-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="284d7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="284d7-106">Attributes and elements</span></span>

<span data-ttu-id="284d7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="284d7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="284d7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="284d7-108">Attributes</span></span>

<span data-ttu-id="284d7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="284d7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="284d7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="284d7-110">Child elements</span></span>

|<span data-ttu-id="284d7-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="284d7-111">**Element**</span></span>|<span data-ttu-id="284d7-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="284d7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="284d7-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="284d7-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="284d7-114">Enthält den Bezeichner und den Änderungsschlüssel eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="284d7-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="284d7-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="284d7-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="284d7-116">Identifiziert Microsoft Exchange Server 2007-Ordner, auf die über den Namen verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="284d7-116">Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="284d7-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="284d7-117">Parent elements</span></span>

|<span data-ttu-id="284d7-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="284d7-118">**Element**</span></span>|<span data-ttu-id="284d7-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="284d7-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="284d7-120">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="284d7-120">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md) <br/> |<span data-ttu-id="284d7-121">Definiert eine Anforderung zum Synchronisieren einer Ordnerhierarchie in einer Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="284d7-121">Defines a request to synchronize a folder hierarchy in an Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="284d7-122">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="284d7-122">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="284d7-123">Definiert eine Anforderung zum Synchronisieren von Elementen in einem Exchange-Informationsspeicher Ordner.</span><span class="sxs-lookup"><span data-stu-id="284d7-123">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="284d7-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="284d7-124">Remarks</span></span>

<span data-ttu-id="284d7-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="284d7-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="284d7-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="284d7-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="284d7-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="284d7-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="284d7-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="284d7-128">Schema name</span></span>  <br/> |<span data-ttu-id="284d7-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="284d7-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="284d7-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="284d7-130">Validation file</span></span>  <br/> |<span data-ttu-id="284d7-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="284d7-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="284d7-132">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="284d7-132">Can be empty</span></span>  <br/> |<span data-ttu-id="284d7-133">False</span><span class="sxs-lookup"><span data-stu-id="284d7-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="284d7-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="284d7-134">See also</span></span>

- [<span data-ttu-id="284d7-135">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="284d7-135">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="284d7-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="284d7-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

