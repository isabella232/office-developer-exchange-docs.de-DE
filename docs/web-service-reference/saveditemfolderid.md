---
title: SavedItemFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SavedItemFolderId
api_type:
- schema
ms.assetid: 4b8b475c-9ca5-48c9-acb0-8848b53be1ce
description: Das Element des SavedItemFolderId identifiziert den Zielordner für Vorgänge, die zu aktualisieren, senden und Elemente in einem Postfach erstellen.
ms.openlocfilehash: 3f46070a538f5e03007925565a8888efe06b62b7
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354162"
---
# <a name="saveditemfolderid"></a><span data-ttu-id="2d490-103">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="2d490-103">SavedItemFolderId</span></span>

<span data-ttu-id="2d490-104">Das Element **des SavedItemFolderId** identifiziert den Zielordner für Vorgänge, die zu aktualisieren, senden und Elemente in einem Postfach erstellen.</span><span class="sxs-lookup"><span data-stu-id="2d490-104">The **SavedItemFolderId** element identifies the target folder for operations that update, send, and create items in a mailbox.</span></span> 
  
```xml
<SavedItemFolderId>
   <FolderId/>
</SavedItemFolderId>
```

```xml
<SavedItemFolderId>
   <DistinguishedFolderId/>
</SavedItemFolderId>
```

<span data-ttu-id="2d490-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="2d490-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2d490-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2d490-106">Attributes and elements</span></span>

<span data-ttu-id="2d490-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2d490-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d490-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2d490-108">Attributes</span></span>

<span data-ttu-id="2d490-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2d490-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2d490-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2d490-110">Child elements</span></span>

|<span data-ttu-id="2d490-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2d490-111">**Element**</span></span>|<span data-ttu-id="2d490-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2d490-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d490-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="2d490-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="2d490-114">Enthält den Bezeichner und ein Änderungsprotokoll Schlüssel einen Zielordner für Vorgänge, die zu aktualisieren, senden und Elemente im Exchange-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2d490-114">Contains the identifier and change key of a target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2d490-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="2d490-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="2d490-116">Gibt einen Zielordner durch einen benannten Bezeichner für Vorgänge, die zu aktualisieren, senden und erstellen Sie Elemente im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="2d490-116">Identifies a target folder by a named identifier for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2d490-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2d490-117">Parent elements</span></span>

|<span data-ttu-id="2d490-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="2d490-118">**Element**</span></span>|<span data-ttu-id="2d490-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2d490-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d490-120">CreateItem</span><span class="sxs-lookup"><span data-stu-id="2d490-120">CreateItem</span></span>](createitem.md) <br/> |<span data-ttu-id="2d490-121">Definiert eine Anforderung zum Erstellen eines Elements im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="2d490-121">Defines a request to create an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="2d490-122">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="2d490-122">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateItem` <br/> |
|[<span data-ttu-id="2d490-123">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="2d490-123">UpdateItem</span></span>](updateitem.md) <br/> |<span data-ttu-id="2d490-124">Definiert eine Anforderung zum Aktualisieren eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="2d490-124">Defines a request to update an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="2d490-125">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="2d490-125">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem` <br/> |
|[<span data-ttu-id="2d490-126">SendItem</span><span class="sxs-lookup"><span data-stu-id="2d490-126">SendItem</span></span>](senditem.md) <br/> |<span data-ttu-id="2d490-127">Definiert eine Anforderung zum Senden eines Elements im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="2d490-127">Defines a request to send an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="2d490-128">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="2d490-128">The following is the XPath expression to this element:</span></span>  <br/>  `/SendItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d490-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2d490-129">Remarks</span></span>

<span data-ttu-id="2d490-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="2d490-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2d490-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2d490-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d490-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="2d490-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2d490-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2d490-133">Schema Name</span></span>  <br/> |<span data-ttu-id="2d490-134">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2d490-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2d490-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2d490-135">Validation File</span></span>  <br/> |<span data-ttu-id="2d490-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2d490-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2d490-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2d490-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="2d490-138">False</span><span class="sxs-lookup"><span data-stu-id="2d490-138">False</span></span>  <br/> |
   

