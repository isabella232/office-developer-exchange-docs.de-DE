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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758681"
---
# <a name="getfolder"></a><span data-ttu-id="86dee-103">GetFolder</span><span class="sxs-lookup"><span data-stu-id="86dee-103">GetFolder</span></span>

<span data-ttu-id="86dee-104">Das **GetFolder** -Element definiert eine Anforderung an einen Ordner aus einem Postfach im Exchange-Speicher abzurufen.</span><span class="sxs-lookup"><span data-stu-id="86dee-104">The **GetFolder** element defines a request to get a folder from a mailbox in the Exchange store.</span></span> 
  
```xml
<GetFolder>
   <FolderShape/>
   <FolderIds/>
</GetFolder>
```

 <span data-ttu-id="86dee-105">**GetFolderType**</span><span class="sxs-lookup"><span data-stu-id="86dee-105">**GetFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="86dee-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="86dee-106">Attributes and elements</span></span>

<span data-ttu-id="86dee-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="86dee-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="86dee-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="86dee-108">Attributes</span></span>

<span data-ttu-id="86dee-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="86dee-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="86dee-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="86dee-110">Child elements</span></span>

|<span data-ttu-id="86dee-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="86dee-111">**Element**</span></span>|<span data-ttu-id="86dee-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="86dee-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86dee-113">FolderShape</span><span class="sxs-lookup"><span data-stu-id="86dee-113">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="86dee-114">Identifiziert die Eigenschaften für jeden Ordner im [FolderIds](folderids.md) -Element identifiziert abgerufen.</span><span class="sxs-lookup"><span data-stu-id="86dee-114">Identifies the properties to get for each folder identified in the [FolderIds](folderids.md) element.</span></span>  <br/> |
|[<span data-ttu-id="86dee-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="86dee-115">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="86dee-116">Enthält ein Array von Bezeichnern für Ordner, die verwendet werden, um Ordner zum Abrufen von einem Postfach im Exchange-Speicher zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="86dee-116">Contains an array of folder identifiers that are used to identify folders to get from a mailbox in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="86dee-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="86dee-117">Parent elements</span></span>

<span data-ttu-id="86dee-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="86dee-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="86dee-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="86dee-119">Remarks</span></span>

<span data-ttu-id="86dee-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="86dee-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="86dee-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="86dee-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86dee-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="86dee-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="86dee-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="86dee-123">Schema Name</span></span>  <br/> |<span data-ttu-id="86dee-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="86dee-124">Message schema</span></span>  <br/> |
|<span data-ttu-id="86dee-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="86dee-125">Validation File</span></span>  <br/> |<span data-ttu-id="86dee-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="86dee-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="86dee-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="86dee-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="86dee-128">False</span><span class="sxs-lookup"><span data-stu-id="86dee-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="86dee-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86dee-129">See also</span></span>



[<span data-ttu-id="86dee-130">GetFolder Operation</span><span class="sxs-lookup"><span data-stu-id="86dee-130">GetFolder operation</span></span>](getfolder-operation.md)

