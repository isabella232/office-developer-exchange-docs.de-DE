---
title: Des SavedItemFolderId
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
ms.openlocfilehash: c57a7fb4abc2f7ee7b599f56f016811d6ff2c21c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831277"
---
# <a name="saveditemfolderid"></a><span data-ttu-id="1c9b9-103">Des SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="1c9b9-103">SavedItemFolderId</span></span>

<span data-ttu-id="1c9b9-104">Das Element **des SavedItemFolderId** identifiziert den Zielordner für Vorgänge, die zu aktualisieren, senden und Elemente in einem Postfach erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c9b9-104">The **SavedItemFolderId** element identifies the target folder for operations that update, send, and create items in a mailbox.</span></span> 
  
```xml
<SavedItemFolderId>
   <FolderId/>
</SavedItemFolderId>
```

 <span data-ttu-id="1c9b9-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="1c9b9-105">**TargetFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1c9b9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1c9b9-106">Attributes and elements</span></span>

<span data-ttu-id="1c9b9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1c9b9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1c9b9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1c9b9-108">Attributes</span></span>

<span data-ttu-id="1c9b9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1c9b9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1c9b9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1c9b9-110">Child elements</span></span>

|<span data-ttu-id="1c9b9-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1c9b9-111">**Element**</span></span>|<span data-ttu-id="1c9b9-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c9b9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1c9b9-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="1c9b9-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="1c9b9-114">Enthält den Bezeichner und ein Änderungsprotokoll Schlüssel einen Zielordner für Vorgänge, die zu aktualisieren, senden und Elemente im Exchange-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c9b9-114">Contains the identifier and change key of a target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1c9b9-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="1c9b9-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="1c9b9-116">Gibt einen Zielordner durch einen benannten Bezeichner für Vorgänge, die zu aktualisieren, senden und erstellen Sie Elemente im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="1c9b9-116">Identifies a target folder by a named identifier for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1c9b9-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1c9b9-117">Parent elements</span></span>

|<span data-ttu-id="1c9b9-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="1c9b9-118">**Element**</span></span>|<span data-ttu-id="1c9b9-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c9b9-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1c9b9-120">CreateItem</span><span class="sxs-lookup"><span data-stu-id="1c9b9-120">CreateItem</span></span>](createitem.md) <br/> |<span data-ttu-id="1c9b9-121">Definiert eine Anforderung zum Erstellen eines Elements im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="1c9b9-121">Defines a request to create an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="1c9b9-122">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="1c9b9-122">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateItem` <br/> |
|[<span data-ttu-id="1c9b9-123">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="1c9b9-123">UpdateItem</span></span>](updateitem.md) <br/> |<span data-ttu-id="1c9b9-124">Definiert eine Anforderung zum Aktualisieren eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="1c9b9-124">Defines a request to update an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="1c9b9-125">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="1c9b9-125">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem` <br/> |
|[<span data-ttu-id="1c9b9-126">SendItem</span><span class="sxs-lookup"><span data-stu-id="1c9b9-126">SendItem</span></span>](senditem.md) <br/> |<span data-ttu-id="1c9b9-127">Definiert eine Anforderung zum Senden eines Elements im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="1c9b9-127">Defines a request to send an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="1c9b9-128">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="1c9b9-128">The following is the XPath expression to this element:</span></span>  <br/>  `/SendItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c9b9-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1c9b9-129">Remarks</span></span>

<span data-ttu-id="1c9b9-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="1c9b9-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1c9b9-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1c9b9-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c9b9-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c9b9-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1c9b9-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1c9b9-133">Schema Name</span></span>  <br/> |<span data-ttu-id="1c9b9-134">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="1c9b9-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1c9b9-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1c9b9-135">Validation File</span></span>  <br/> |<span data-ttu-id="1c9b9-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1c9b9-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1c9b9-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1c9b9-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="1c9b9-138">False</span><span class="sxs-lookup"><span data-stu-id="1c9b9-138">False</span></span>  <br/> |
   

