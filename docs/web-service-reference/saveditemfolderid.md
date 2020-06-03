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
description: Das SavedItemFolderId-Element identifiziert den Zielordner für Vorgänge, die Elemente in einem Postfach aktualisieren, senden und erstellen.
ms.openlocfilehash: 8e18b8863a54aa4e9d6e65f7a54e20904f5a9599
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465275"
---
# <a name="saveditemfolderid"></a><span data-ttu-id="1eb53-103">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="1eb53-103">SavedItemFolderId</span></span>

<span data-ttu-id="1eb53-104">Das **SavedItemFolderId** -Element identifiziert den Zielordner für Vorgänge, die Elemente in einem Postfach aktualisieren, senden und erstellen.</span><span class="sxs-lookup"><span data-stu-id="1eb53-104">The **SavedItemFolderId** element identifies the target folder for operations that update, send, and create items in a mailbox.</span></span> 
  
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

<span data-ttu-id="1eb53-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="1eb53-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="1eb53-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1eb53-106">Attributes and elements</span></span>

<span data-ttu-id="1eb53-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1eb53-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1eb53-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1eb53-108">Attributes</span></span>

<span data-ttu-id="1eb53-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1eb53-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1eb53-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1eb53-110">Child elements</span></span>

|<span data-ttu-id="1eb53-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1eb53-111">**Element**</span></span>|<span data-ttu-id="1eb53-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1eb53-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1eb53-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="1eb53-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="1eb53-114">Enthält den Bezeichner und den Änderungsschlüssel eines Zielordners für Vorgänge, die Elemente im Exchange-Informationsspeicher aktualisieren, senden und erstellen.</span><span class="sxs-lookup"><span data-stu-id="1eb53-114">Contains the identifier and change key of a target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1eb53-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="1eb53-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="1eb53-116">Identifiziert einen Zielordner anhand eines benannten Bezeichners für Vorgänge, die Elemente im Exchange-Informationsspeicher aktualisieren, senden und erstellen.</span><span class="sxs-lookup"><span data-stu-id="1eb53-116">Identifies a target folder by a named identifier for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1eb53-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1eb53-117">Parent elements</span></span>

|<span data-ttu-id="1eb53-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="1eb53-118">**Element**</span></span>|<span data-ttu-id="1eb53-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1eb53-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1eb53-120">CreateItem</span><span class="sxs-lookup"><span data-stu-id="1eb53-120">CreateItem</span></span>](createitem.md) <br/> |<span data-ttu-id="1eb53-121">Definiert eine Anforderung zum Erstellen eines Elements im Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1eb53-121">Defines a request to create an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="1eb53-122">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="1eb53-122">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateItem` <br/> |
|[<span data-ttu-id="1eb53-123">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="1eb53-123">UpdateItem</span></span>](updateitem.md) <br/> |<span data-ttu-id="1eb53-124">Definiert eine Anforderung zum Aktualisieren eines Elements im Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1eb53-124">Defines a request to update an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="1eb53-125">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="1eb53-125">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem` <br/> |
|[<span data-ttu-id="1eb53-126">SendItem</span><span class="sxs-lookup"><span data-stu-id="1eb53-126">SendItem</span></span>](senditem.md) <br/> |<span data-ttu-id="1eb53-127">Definiert eine Anforderung zum Senden eines Elements im Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1eb53-127">Defines a request to send an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="1eb53-128">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="1eb53-128">The following is the XPath expression to this element:</span></span>  <br/>  `/SendItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1eb53-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1eb53-129">Remarks</span></span>

<span data-ttu-id="1eb53-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="1eb53-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1eb53-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1eb53-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1eb53-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="1eb53-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1eb53-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1eb53-133">Schema Name</span></span>  <br/> |<span data-ttu-id="1eb53-134">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="1eb53-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1eb53-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1eb53-135">Validation File</span></span>  <br/> |<span data-ttu-id="1eb53-136">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="1eb53-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1eb53-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1eb53-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="1eb53-138">False</span><span class="sxs-lookup"><span data-stu-id="1eb53-138">False</span></span>  <br/> |
   

