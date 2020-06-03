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
description: Das CreateFolder-Element definiert eine Anforderung zum Erstellen eines Ordners im Exchange-Informationsspeicher.
ms.openlocfilehash: c2a971a6b827553a1632c2a86e4d36e3b83a2de3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457543"
---
# <a name="createfolder"></a><span data-ttu-id="2a80d-103">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="2a80d-103">CreateFolder</span></span>

<span data-ttu-id="2a80d-104">Das **CreateFolder** -Element definiert eine Anforderung zum Erstellen eines Ordners im Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="2a80d-104">The **CreateFolder** element defines a request to create a folder in the Exchange store.</span></span> 
  
```xml
<CreateFolder>
   <ParentFolderId/>
   <Folders/>
</CreateFolder>
```

 <span data-ttu-id="2a80d-105">**Createfoldertype**</span><span class="sxs-lookup"><span data-stu-id="2a80d-105">**CreateFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2a80d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2a80d-106">Attributes and elements</span></span>

<span data-ttu-id="2a80d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2a80d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a80d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2a80d-108">Attributes</span></span>

<span data-ttu-id="2a80d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2a80d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2a80d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2a80d-110">Child elements</span></span>

|<span data-ttu-id="2a80d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2a80d-111">**Element**</span></span>|<span data-ttu-id="2a80d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2a80d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a80d-113">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="2a80d-113">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="2a80d-114">Das-Element, das den Speicherort angibt, an dem der neue Ordner erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2a80d-114">The element that identifies the location where the new folder is created.</span></span>  <br/> |
|[<span data-ttu-id="2a80d-115">Ordner</span><span class="sxs-lookup"><span data-stu-id="2a80d-115">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="2a80d-116">Das-Element, das alle Ordner enthält, die erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2a80d-116">The element that contains all the folders to create.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2a80d-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2a80d-117">Parent elements</span></span>

<span data-ttu-id="2a80d-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="2a80d-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2a80d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a80d-119">Remarks</span></span>

<span data-ttu-id="2a80d-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="2a80d-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a80d-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2a80d-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a80d-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a80d-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2a80d-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2a80d-123">Schema Name</span></span>  <br/> |<span data-ttu-id="2a80d-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2a80d-124">Message schema</span></span>  <br/> |
|<span data-ttu-id="2a80d-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2a80d-125">Validation File</span></span>  <br/> |<span data-ttu-id="2a80d-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2a80d-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2a80d-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2a80d-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="2a80d-128">False</span><span class="sxs-lookup"><span data-stu-id="2a80d-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2a80d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a80d-129">See also</span></span>



[<span data-ttu-id="2a80d-130">CreateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2a80d-130">CreateFolder operation</span></span>](createfolder-operation.md)


[<span data-ttu-id="2a80d-131">Erstellen von Ordnern (Exchange Webdienste)</span><span class="sxs-lookup"><span data-stu-id="2a80d-131">Creating Folders (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

