---
title: FolderChanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderChanges
api_type:
- schema
ms.assetid: d3f611ed-56a4-43f8-aa65-cbd7844b827f
description: Das FolderChanges-Element stellt eine Auflistung von Änderungen für einen Ordner dar.
ms.openlocfilehash: 5481496100512584fd0b9745ee42d5b9516bd7fb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458383"
---
# <a name="folderchanges"></a><span data-ttu-id="ecfb0-103">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="ecfb0-103">FolderChanges</span></span>

<span data-ttu-id="ecfb0-104">Das **FolderChanges** -Element stellt eine Auflistung von Änderungen für einen Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-104">The **FolderChanges** element represents a collection of changes for a folder.</span></span> 
  
[<span data-ttu-id="ecfb0-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="ecfb0-105">UpdateFolder</span></span>](updatefolder.md)
  
[<span data-ttu-id="ecfb0-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="ecfb0-106">FolderChanges</span></span>](folderchanges.md)
  
```xml
<FolderChanges>
   <FolderChange/>
</FolderChanges>
```

 <span data-ttu-id="ecfb0-107">**NonEmptyArrayOfFolderChangesType**</span><span class="sxs-lookup"><span data-stu-id="ecfb0-107">**NonEmptyArrayOfFolderChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ecfb0-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ecfb0-108">Attributes and elements</span></span>

<span data-ttu-id="ecfb0-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ecfb0-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ecfb0-110">Attributes</span></span>

<span data-ttu-id="ecfb0-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ecfb0-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ecfb0-112">Child elements</span></span>

|<span data-ttu-id="ecfb0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ecfb0-113">**Element**</span></span>|<span data-ttu-id="ecfb0-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ecfb0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ecfb0-115">FolderChange</span><span class="sxs-lookup"><span data-stu-id="ecfb0-115">FolderChange</span></span>](folderchange.md) <br/> |<span data-ttu-id="ecfb0-116">Stellt eine einzelne Änderung dar, die für einen einzelnen Ordner ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-116">Represents a single change to be performed on a single folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ecfb0-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ecfb0-117">Parent elements</span></span>

|<span data-ttu-id="ecfb0-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="ecfb0-118">**Element**</span></span>|<span data-ttu-id="ecfb0-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ecfb0-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ecfb0-120">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="ecfb0-120">UpdateFolder</span></span>](updatefolder.md) <br/> |<span data-ttu-id="ecfb0-121">Stellt den Vorgang dar, der zum Aktualisieren der Eigenschaften eines Ordners verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-121">Represents the operation that is used to update properties for a folder.</span></span>  <br/> <span data-ttu-id="ecfb0-122">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="ecfb0-122">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecfb0-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ecfb0-123">Remarks</span></span>

<span data-ttu-id="ecfb0-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ecfb0-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ecfb0-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ecfb0-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ecfb0-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="ecfb0-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ecfb0-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ecfb0-127">Schema Name</span></span>  <br/> |<span data-ttu-id="ecfb0-128">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ecfb0-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ecfb0-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ecfb0-129">Validation File</span></span>  <br/> |<span data-ttu-id="ecfb0-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ecfb0-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ecfb0-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ecfb0-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="ecfb0-132">False</span><span class="sxs-lookup"><span data-stu-id="ecfb0-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ecfb0-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecfb0-133">See also</span></span>



[<span data-ttu-id="ecfb0-134">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ecfb0-134">UpdateFolder operation</span></span>](updatefolder-operation.md)

