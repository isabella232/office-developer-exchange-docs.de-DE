---
title: CreateFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateFolder
api_type:
- schema
ms.assetid: 110bada1-517b-4bd6-870d-7086dc879e5d
description: Das CreateFolder-Element definiert eine Anforderung an einen Ordner im Exchange-Speicher zu erstellen.
ms.openlocfilehash: e30af23b8ed8669053b94be460d62fbf7abf24c9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19757753"
---
# <a name="createfolder"></a><span data-ttu-id="599ca-103">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="599ca-103">CreateFolder</span></span>

<span data-ttu-id="599ca-104">Das **CreateFolder** -Element definiert eine Anforderung an einen Ordner im Exchange-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="599ca-104">The **CreateFolder** element defines a request to create a folder in the Exchange store.</span></span> 
  
```xml
<CreateFolder>
   <ParentFolderId/>
   <Folders/>
</CreateFolder>
```

 <span data-ttu-id="599ca-105">**CreateFolderType**</span><span class="sxs-lookup"><span data-stu-id="599ca-105">**CreateFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="599ca-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="599ca-106">Attributes and elements</span></span>

<span data-ttu-id="599ca-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="599ca-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="599ca-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="599ca-108">Attributes</span></span>

<span data-ttu-id="599ca-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="599ca-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="599ca-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="599ca-110">Child elements</span></span>

|<span data-ttu-id="599ca-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="599ca-111">**Element**</span></span>|<span data-ttu-id="599ca-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="599ca-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="599ca-113">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="599ca-113">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="599ca-114">Das Element, das den Speicherort angibt, in der neue Ordner erstellt.</span><span class="sxs-lookup"><span data-stu-id="599ca-114">The element that identifies the location where the new folder is created.</span></span>  <br/> |
|[<span data-ttu-id="599ca-115">Ordner</span><span class="sxs-lookup"><span data-stu-id="599ca-115">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="599ca-116">Das Element, das zu erstellende Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="599ca-116">The element that contains all the folders to create.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="599ca-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="599ca-117">Parent elements</span></span>

<span data-ttu-id="599ca-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="599ca-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="599ca-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="599ca-119">Remarks</span></span>

<span data-ttu-id="599ca-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="599ca-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="599ca-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="599ca-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="599ca-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="599ca-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="599ca-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="599ca-123">Schema Name</span></span>  <br/> |<span data-ttu-id="599ca-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="599ca-124">Message schema</span></span>  <br/> |
|<span data-ttu-id="599ca-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="599ca-125">Validation File</span></span>  <br/> |<span data-ttu-id="599ca-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="599ca-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="599ca-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="599ca-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="599ca-128">False</span><span class="sxs-lookup"><span data-stu-id="599ca-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="599ca-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="599ca-129">See also</span></span>



[<span data-ttu-id="599ca-130">CreateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="599ca-130">CreateFolder operation</span></span>](createfolder-operation.md)


[<span data-ttu-id="599ca-131">Erstellen von Ordnern (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="599ca-131">Creating Folders (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

