---
title: IdOfFolderToShare
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IdOfFolderToShare
api_type:
- schema
ms.assetid: 199d1839-f061-4070-a977-874b0c08e5be
description: Das Element IdOfFolderToShare stellt den Bezeichner des Ordners auf dem Server, der freigegeben werden sollen.
ms.openlocfilehash: 1e3e53819f23bbc5753ac21b9e3ea6593ac4826c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829853"
---
# <a name="idoffoldertoshare"></a><span data-ttu-id="5eeb0-103">IdOfFolderToShare</span><span class="sxs-lookup"><span data-stu-id="5eeb0-103">IdOfFolderToShare</span></span>

<span data-ttu-id="5eeb0-104">Das Element **IdOfFolderToShare** stellt den Bezeichner des Ordners auf dem Server, der freigegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5eeb0-104">The **IdOfFolderToShare** element represents the identifier of the folder on the server that will be shared.</span></span> 
  
```
<IdOfFolderToShare Id="" ChangeKey="" />
```

 <span data-ttu-id="5eeb0-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="5eeb0-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5eeb0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5eeb0-106">Attributes and elements</span></span>

<span data-ttu-id="5eeb0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5eeb0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5eeb0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5eeb0-108">Attributes</span></span>

|<span data-ttu-id="5eeb0-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5eeb0-109">**Attribute**</span></span>|<span data-ttu-id="5eeb0-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5eeb0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5eeb0-111">Id</span><span class="sxs-lookup"><span data-stu-id="5eeb0-111">Id</span></span>  <br/> |<span data-ttu-id="5eeb0-112">Enthält eine Zeichenfolge, die einen Ordner im Exchange-Speicher identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5eeb0-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="5eeb0-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5eeb0-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="5eeb0-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="5eeb0-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="5eeb0-115">Enthält eine Zeichenfolge, die eine Version eines Ordners identifiziert, die von dem Id-Attribut angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="5eeb0-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="5eeb0-116">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="5eeb0-116">This attribute is optional.</span></span> <span data-ttu-id="5eeb0-117">Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Ordners verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5eeb0-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5eeb0-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5eeb0-118">Child elements</span></span>

<span data-ttu-id="5eeb0-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="5eeb0-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5eeb0-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5eeb0-120">Parent elements</span></span>

|<span data-ttu-id="5eeb0-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="5eeb0-121">**Element**</span></span>|<span data-ttu-id="5eeb0-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5eeb0-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5eeb0-123">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="5eeb0-123">GetSharingMetadata</span></span>](getsharingmetadata.md) <br/> |<span data-ttu-id="5eeb0-124">Definiert eine Anforderung an ein undurchsichtiger Authentifizierungstoken erhalten möchten, die die Einladung zur Freigabe identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5eeb0-124">Defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5eeb0-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5eeb0-125">Remarks</span></span>

<span data-ttu-id="5eeb0-126">Das Schema, das dieses Element beschreibt befindet sich das virtuelle IIS-Verzeichnis, dass Hosts Exchange-Webdienste des Computers, auf dem Microsoft Exchange Server ausgeführt wird die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5eeb0-126">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5eeb0-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5eeb0-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5eeb0-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="5eeb0-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5eeb0-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5eeb0-129">Schema Name</span></span>  <br/> |<span data-ttu-id="5eeb0-130">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="5eeb0-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5eeb0-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5eeb0-131">Validation File</span></span>  <br/> |<span data-ttu-id="5eeb0-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5eeb0-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5eeb0-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5eeb0-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="5eeb0-134">False</span><span class="sxs-lookup"><span data-stu-id="5eeb0-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5eeb0-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5eeb0-135">See also</span></span>



[<span data-ttu-id="5eeb0-136">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5eeb0-136">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="5eeb0-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5eeb0-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

