---
title: GetFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetFolder
api_type:
- schema
ms.assetid: 34e4c9ea-adcd-46bd-ae8f-7abb256c585a
description: Das GetFolder-Element definiert eine Anforderung an einen Ordner aus einem Postfach im Exchange-Speicher abzurufen.
ms.openlocfilehash: 233da6ce57683350d4a13f6585593ac09438f0e6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758681"
---
# <a name="getfolder"></a><span data-ttu-id="6271f-103">GetFolder</span><span class="sxs-lookup"><span data-stu-id="6271f-103">GetFolder</span></span>

<span data-ttu-id="6271f-104">Das **GetFolder** -Element definiert eine Anforderung an einen Ordner aus einem Postfach im Exchange-Speicher abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6271f-104">The **GetFolder** element defines a request to get a folder from a mailbox in the Exchange store.</span></span> 
  
```xml
<GetFolder>
   <FolderShape/>
   <FolderIds/>
</GetFolder>
```

 <span data-ttu-id="6271f-105">**GetFolderType**</span><span class="sxs-lookup"><span data-stu-id="6271f-105">**GetFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6271f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6271f-106">Attributes and elements</span></span>

<span data-ttu-id="6271f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6271f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6271f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6271f-108">Attributes</span></span>

<span data-ttu-id="6271f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6271f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6271f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6271f-110">Child elements</span></span>

|<span data-ttu-id="6271f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6271f-111">**Element**</span></span>|<span data-ttu-id="6271f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6271f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6271f-113">FolderShape</span><span class="sxs-lookup"><span data-stu-id="6271f-113">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="6271f-114">Identifiziert die Eigenschaften für jeden Ordner im [FolderIds](folderids.md) -Element identifiziert abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6271f-114">Identifies the properties to get for each folder identified in the [FolderIds](folderids.md) element.</span></span>  <br/> |
|[<span data-ttu-id="6271f-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="6271f-115">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="6271f-116">Enthält ein Array von Bezeichnern für Ordner, die verwendet werden, um Ordner zum Abrufen von einem Postfach im Exchange-Speicher zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6271f-116">Contains an array of folder identifiers that are used to identify folders to get from a mailbox in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6271f-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6271f-117">Parent elements</span></span>

<span data-ttu-id="6271f-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="6271f-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6271f-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6271f-119">Remarks</span></span>

<span data-ttu-id="6271f-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="6271f-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6271f-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6271f-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6271f-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="6271f-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6271f-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6271f-123">Schema Name</span></span>  <br/> |<span data-ttu-id="6271f-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="6271f-124">Message schema</span></span>  <br/> |
|<span data-ttu-id="6271f-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6271f-125">Validation File</span></span>  <br/> |<span data-ttu-id="6271f-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6271f-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6271f-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6271f-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="6271f-128">False</span><span class="sxs-lookup"><span data-stu-id="6271f-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6271f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6271f-129">See also</span></span>



[<span data-ttu-id="6271f-130">GetFolder Operation</span><span class="sxs-lookup"><span data-stu-id="6271f-130">GetFolder operation</span></span>](getfolder-operation.md)

