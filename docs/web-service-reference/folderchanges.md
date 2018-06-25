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
description: Das Element FolderChanges stellt eine Auflistung von Änderungen für einen Ordner.
ms.openlocfilehash: 7ab89e79f6babb5e93863974835685c6975d96dd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758495"
---
# <a name="folderchanges"></a><span data-ttu-id="bb198-103">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="bb198-103">FolderChanges</span></span>

<span data-ttu-id="bb198-104">Das Element **FolderChanges** stellt eine Auflistung von Änderungen für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="bb198-104">The **FolderChanges** element represents a collection of changes for a folder.</span></span> 
  
[<span data-ttu-id="bb198-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="bb198-105">UpdateFolder</span></span>](updatefolder.md)
  
[<span data-ttu-id="bb198-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="bb198-106">FolderChanges</span></span>](folderchanges.md)
  
```xml
<FolderChanges>
   <FolderChange/>
</FolderChanges>
```

 <span data-ttu-id="bb198-107">**NonEmptyArrayOfFolderChangesType**</span><span class="sxs-lookup"><span data-stu-id="bb198-107">**NonEmptyArrayOfFolderChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bb198-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bb198-108">Attributes and elements</span></span>

<span data-ttu-id="bb198-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bb198-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb198-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="bb198-110">Attributes</span></span>

<span data-ttu-id="bb198-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="bb198-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bb198-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bb198-112">Child elements</span></span>

|<span data-ttu-id="bb198-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bb198-113">**Element**</span></span>|<span data-ttu-id="bb198-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bb198-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb198-115">FolderChange</span><span class="sxs-lookup"><span data-stu-id="bb198-115">FolderChange</span></span>](folderchange.md) <br/> |<span data-ttu-id="bb198-116">Stellt eine Änderung in einem gemeinsamen Ordner ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bb198-116">Represents a single change to be performed on a single folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bb198-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bb198-117">Parent elements</span></span>

|<span data-ttu-id="bb198-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="bb198-118">**Element**</span></span>|<span data-ttu-id="bb198-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bb198-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb198-120">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="bb198-120">UpdateFolder</span></span>](updatefolder.md) <br/> |<span data-ttu-id="bb198-121">Stellt die Operation, die verwendet wird, um Eigenschaften für einen Ordner zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="bb198-121">Represents the operation that is used to update properties for a folder.</span></span>  <br/> <span data-ttu-id="bb198-122">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="bb198-122">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb198-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bb198-123">Remarks</span></span>

<span data-ttu-id="bb198-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="bb198-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bb198-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bb198-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb198-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="bb198-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bb198-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bb198-127">Schema Name</span></span>  <br/> |<span data-ttu-id="bb198-128">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="bb198-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bb198-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bb198-129">Validation File</span></span>  <br/> |<span data-ttu-id="bb198-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bb198-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bb198-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="bb198-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="bb198-132">False</span><span class="sxs-lookup"><span data-stu-id="bb198-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb198-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb198-133">See also</span></span>



[<span data-ttu-id="bb198-134">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bb198-134">UpdateFolder operation</span></span>](updatefolder-operation.md)

