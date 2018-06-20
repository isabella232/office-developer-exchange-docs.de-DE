---
title: MoveFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveFolder
api_type:
- schema
ms.assetid: f2bb0a73-94d7-4bc7-8902-bd9c69120221
description: Das MoveFolder-Element definiert eine Anforderung an einen Ordner im Exchange-Speicher zu verschieben.
ms.openlocfilehash: 42a990ced18cc13c7694042df786d33c018f346c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830485"
---
# <a name="movefolder"></a><span data-ttu-id="c0285-103">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="c0285-103">MoveFolder</span></span>

<span data-ttu-id="c0285-104">Das **MoveFolder** -Element definiert eine Anforderung an einen Ordner im Exchange-Speicher zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="c0285-104">The **MoveFolder** element defines a request to move a folder in the Exchange store.</span></span> 
  
```xml
<MoveFolder>
   <ToFolderId/>
   <FolderIds/>
</MoveFolder>
```

 <span data-ttu-id="c0285-105">**MoveFolderType**</span><span class="sxs-lookup"><span data-stu-id="c0285-105">**MoveFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c0285-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c0285-106">Attributes and elements</span></span>

<span data-ttu-id="c0285-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c0285-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0285-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c0285-108">Attributes</span></span>

<span data-ttu-id="c0285-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c0285-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c0285-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0285-110">Child elements</span></span>

|<span data-ttu-id="c0285-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c0285-111">**Element**</span></span>|<span data-ttu-id="c0285-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0285-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0285-113">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="c0285-113">ToFolderId</span></span>](tofolderid.md) <br/> |<span data-ttu-id="c0285-114">Stellt den Zielordner für einen Ordner verschoben.</span><span class="sxs-lookup"><span data-stu-id="c0285-114">Represents the destination folder for a moved folder.</span></span>  <br/> |
|[<span data-ttu-id="c0285-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="c0285-115">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="c0285-116">Enthält ein Array der Ordner an, in den das Element [ToFolderId](tofolderid.md) identifizierten Ordner verschieben.</span><span class="sxs-lookup"><span data-stu-id="c0285-116">Contains an array of folders to move to the folder identified by the [ToFolderId](tofolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c0285-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0285-117">Parent elements</span></span>

<span data-ttu-id="c0285-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="c0285-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c0285-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c0285-119">Remarks</span></span>

<span data-ttu-id="c0285-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c0285-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0285-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c0285-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0285-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="c0285-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c0285-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c0285-123">Schema Name</span></span>  <br/> |<span data-ttu-id="c0285-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c0285-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c0285-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c0285-125">Validation File</span></span>  <br/> |<span data-ttu-id="c0285-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c0285-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c0285-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c0285-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="c0285-128">False</span><span class="sxs-lookup"><span data-stu-id="c0285-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0285-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0285-129">See also</span></span>



[<span data-ttu-id="c0285-130">MoveFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c0285-130">MoveFolder operation</span></span>](movefolder-operation.md)

