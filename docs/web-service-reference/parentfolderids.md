---
title: ParentFolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentFolderIds
api_type:
- schema
ms.assetid: e7998023-e5e0-465c-91fa-2aa6d1559f64
description: Das ParentFolderIds-Element identifiziert Ordner für die FindItem und FindFolder Vorgänge zu suchen.
ms.openlocfilehash: 7c4dcc98d1cabc8e97f2846880c73111dd307dfb
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354169"
---
# <a name="parentfolderids"></a><span data-ttu-id="5103e-103">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="5103e-103">ParentFolderIds</span></span>

<span data-ttu-id="5103e-104">Das **ParentFolderIds** -Element identifiziert Ordner für die FindItem und FindFolder Vorgänge zu suchen.</span><span class="sxs-lookup"><span data-stu-id="5103e-104">The **ParentFolderIds** element identifies folders for the FindItem and FindFolder operations to search.</span></span> 
  
```xml
<ParentFolderIds>
   <DistinguishedFolderId/>
<ParentFolderIds>
```

```xml
<ParentFolderIds>
   <FolderId/> 
<ParentFolderIds>
```

<span data-ttu-id="5103e-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="5103e-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5103e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5103e-106">Attributes and elements</span></span>

<span data-ttu-id="5103e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5103e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5103e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5103e-108">Attributes</span></span>

<span data-ttu-id="5103e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5103e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5103e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5103e-110">Child elements</span></span>

|<span data-ttu-id="5103e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5103e-111">**Element**</span></span>|<span data-ttu-id="5103e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5103e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5103e-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="5103e-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="5103e-114">Enthält den Schlüssel-ID und Ändern eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="5103e-114">Contains the identifier and change key of a folder.</span></span> <span data-ttu-id="5103e-115">Das **ParentFolderIds** -Element muss dieses Element oder das [DistinguishedFolderId](distinguishedfolderid.md) -Element verwenden.</span><span class="sxs-lookup"><span data-stu-id="5103e-115">The **ParentFolderIds** element must use either this element or the [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="5103e-116">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="5103e-116">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="5103e-117">Identifiziert die Microsoft Exchange Server 2007-Ordner, die nach Namen verwiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="5103e-117">Identifies Microsoft Exchange Server 2007 folders that can be referenced by name.</span></span> <span data-ttu-id="5103e-118">Das **ParentFolderIds** -Element muss dieses Element oder die [FolderId](folderid.md) -Element verwenden.</span><span class="sxs-lookup"><span data-stu-id="5103e-118">The **ParentFolderIds** element must use either this element or the [FolderId](folderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5103e-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5103e-119">Parent elements</span></span>

|<span data-ttu-id="5103e-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="5103e-120">**Element**</span></span>|<span data-ttu-id="5103e-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5103e-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5103e-122">FindFolder</span><span class="sxs-lookup"><span data-stu-id="5103e-122">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="5103e-123">Definiert eine Anforderung zum Ordner in einem Postfach zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5103e-123">Defines a request to identify folders in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="5103e-124">FindItem</span><span class="sxs-lookup"><span data-stu-id="5103e-124">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="5103e-125">Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="5103e-125">Defines a request to find items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="5103e-126">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="5103e-126">ResolveNames</span></span>](resolvenames.md) <br/> |<span data-ttu-id="5103e-127">Definiert eine Anforderung zum Auflösen von Names nicht eindeutig.</span><span class="sxs-lookup"><span data-stu-id="5103e-127">Defines a request to resolve ambiguous names.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5103e-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5103e-128">Remarks</span></span>

<span data-ttu-id="5103e-129">Das Element **ParentFolderIds** muss die [FolderId](folderid.md) oder das [DistinguishedFolderId](distinguishedfolderid.md) -Element verwenden.</span><span class="sxs-lookup"><span data-stu-id="5103e-129">The **ParentFolderIds** element must use either the [FolderId](folderid.md) or the [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span> <span data-ttu-id="5103e-130">Für die Suche kann eine unbegrenzte Anzahl von Ordnern definiert werden.</span><span class="sxs-lookup"><span data-stu-id="5103e-130">An unlimited number of folders can be defined for the search.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5103e-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5103e-131">Example</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="5103e-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5103e-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5103e-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="5103e-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5103e-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5103e-134">Schema Name</span></span>  <br/> |<span data-ttu-id="5103e-135">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="5103e-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5103e-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5103e-136">Validation File</span></span>  <br/> |<span data-ttu-id="5103e-137">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5103e-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5103e-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5103e-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="5103e-139">False</span><span class="sxs-lookup"><span data-stu-id="5103e-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5103e-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5103e-140">See also</span></span>

- [<span data-ttu-id="5103e-141">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="5103e-141">FindFolder operation</span></span>](findfolder-operation.md)  
- [<span data-ttu-id="5103e-142">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5103e-142">FindItem operation</span></span>](finditem-operation.md) 
- [<span data-ttu-id="5103e-143">ResolveNames-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5103e-143">ResolveNames operation</span></span>](resolvenames-operation.md)

