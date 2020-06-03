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
description: Das GetFolder-Element definiert eine Anforderung zum Abrufen eines Ordners aus einem Postfach im Exchange-Informationsspeicher.
ms.openlocfilehash: 41d2b1ab5fcd5d2d60c399e8070ca957ee4b66e7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458705"
---
# <a name="getfolder"></a><span data-ttu-id="ff914-103">GetFolder</span><span class="sxs-lookup"><span data-stu-id="ff914-103">GetFolder</span></span>

<span data-ttu-id="ff914-104">Das **GetFolder** -Element definiert eine Anforderung zum Abrufen eines Ordners aus einem Postfach im Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ff914-104">The **GetFolder** element defines a request to get a folder from a mailbox in the Exchange store.</span></span> 
  
```xml
<GetFolder>
   <FolderShape/>
   <FolderIds/>
</GetFolder>
```

 <span data-ttu-id="ff914-105">**Getfoldertype**</span><span class="sxs-lookup"><span data-stu-id="ff914-105">**GetFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ff914-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ff914-106">Attributes and elements</span></span>

<span data-ttu-id="ff914-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ff914-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff914-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ff914-108">Attributes</span></span>

<span data-ttu-id="ff914-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ff914-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ff914-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ff914-110">Child elements</span></span>

|<span data-ttu-id="ff914-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ff914-111">**Element**</span></span>|<span data-ttu-id="ff914-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff914-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff914-113">FolderShape</span><span class="sxs-lookup"><span data-stu-id="ff914-113">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="ff914-114">Gibt die Eigenschaften an, die für jeden im [FolderIds](folderids.md) -Element identifizierten Ordner abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ff914-114">Identifies the properties to get for each folder identified in the [FolderIds](folderids.md) element.</span></span>  <br/> |
|[<span data-ttu-id="ff914-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="ff914-115">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="ff914-116">Enthält ein Array von Ordner Bezeichnern, die zum Identifizieren von Ordnern verwendet werden, die von einem Postfach im Exchange-Informationsspeicher abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ff914-116">Contains an array of folder identifiers that are used to identify folders to get from a mailbox in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ff914-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ff914-117">Parent elements</span></span>

<span data-ttu-id="ff914-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="ff914-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ff914-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff914-119">Remarks</span></span>

<span data-ttu-id="ff914-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ff914-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ff914-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ff914-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff914-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="ff914-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ff914-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ff914-123">Schema Name</span></span>  <br/> |<span data-ttu-id="ff914-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ff914-124">Message schema</span></span>  <br/> |
|<span data-ttu-id="ff914-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ff914-125">Validation File</span></span>  <br/> |<span data-ttu-id="ff914-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ff914-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ff914-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ff914-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="ff914-128">False</span><span class="sxs-lookup"><span data-stu-id="ff914-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff914-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff914-129">See also</span></span>



[<span data-ttu-id="ff914-130">GetFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ff914-130">GetFolder operation</span></span>](getfolder-operation.md)

