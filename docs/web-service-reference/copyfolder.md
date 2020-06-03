---
title: CopyFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyFolder
api_type:
- schema
ms.assetid: 7d5cd08a-fe81-4cb6-a5a0-6dec2d3c93d4
description: Das CopyFolder-Element definiert eine Anforderung zum Kopieren von Ordnern in einem Postfach im Exchange-Informationsspeicher.
ms.openlocfilehash: fa75272540169a96d5567181d27b8a8f056cce42
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452510"
---
# <a name="copyfolder"></a><span data-ttu-id="d5f18-103">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="d5f18-103">CopyFolder</span></span>

<span data-ttu-id="d5f18-104">Das **CopyFolder** -Element definiert eine Anforderung zum Kopieren von Ordnern in einem Postfach im Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d5f18-104">The **CopyFolder** element defines a request to copy folders in a mailbox in the Exchange store.</span></span> 
  
```xml
<CopyFolder>
   <ToFolderId/>
   <FolderIds/>
</CopyFolder>
```

 <span data-ttu-id="d5f18-105">**CopyFolderType**</span><span class="sxs-lookup"><span data-stu-id="d5f18-105">**CopyFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5f18-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d5f18-106">Attributes and elements</span></span>

<span data-ttu-id="d5f18-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d5f18-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5f18-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d5f18-108">Attributes</span></span>

<span data-ttu-id="d5f18-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d5f18-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5f18-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5f18-110">Child elements</span></span>

|<span data-ttu-id="d5f18-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5f18-111">**Element**</span></span>|<span data-ttu-id="d5f18-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5f18-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5f18-113">Tofolder-Datei</span><span class="sxs-lookup"><span data-stu-id="d5f18-113">ToFolderId</span></span>](tofolderid.md) <br/> |<span data-ttu-id="d5f18-114">Stellt den Zielordner für einen kopierten Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="d5f18-114">Represents the destination folder for a copied folder.</span></span>  <br/> |
|[<span data-ttu-id="d5f18-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="d5f18-115">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="d5f18-116">Enthält ein Array von Ordnern, die in den durch das [tofolder](tofolderid.md) -Element identifizierten Ordner kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d5f18-116">Contains an array of folders to copy to the folder identified by the [ToFolderId](tofolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d5f18-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5f18-117">Parent elements</span></span>

<span data-ttu-id="d5f18-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="d5f18-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d5f18-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5f18-119">Remarks</span></span>

<span data-ttu-id="d5f18-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d5f18-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d5f18-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d5f18-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5f18-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5f18-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d5f18-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d5f18-123">Schema Name</span></span>  <br/> |<span data-ttu-id="d5f18-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d5f18-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d5f18-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d5f18-125">Validation File</span></span>  <br/> |<span data-ttu-id="d5f18-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d5f18-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d5f18-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d5f18-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="d5f18-128">False</span><span class="sxs-lookup"><span data-stu-id="d5f18-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5f18-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5f18-129">See also</span></span>



[<span data-ttu-id="d5f18-130">CopyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d5f18-130">CopyFolder operation</span></span>](copyfolder-operation.md)

