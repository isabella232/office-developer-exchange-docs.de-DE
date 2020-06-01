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
description: Das IdOfFolderToShare-Element stellt den Bezeichner des Ordners auf dem Server dar, der freigegeben werden soll.
ms.openlocfilehash: 93a4740d9adefbb35aae071f0a6bfcb4b2021b4d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457627"
---
# <a name="idoffoldertoshare"></a><span data-ttu-id="355f0-103">IdOfFolderToShare</span><span class="sxs-lookup"><span data-stu-id="355f0-103">IdOfFolderToShare</span></span>

<span data-ttu-id="355f0-104">Das **IdOfFolderToShare** -Element stellt den Bezeichner des Ordners auf dem Server dar, der freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="355f0-104">The **IdOfFolderToShare** element represents the identifier of the folder on the server that will be shared.</span></span> 
  
```
<IdOfFolderToShare Id="" ChangeKey="" />
```

 <span data-ttu-id="355f0-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="355f0-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="355f0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="355f0-106">Attributes and elements</span></span>

<span data-ttu-id="355f0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="355f0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="355f0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="355f0-108">Attributes</span></span>

|<span data-ttu-id="355f0-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="355f0-109">**Attribute**</span></span>|<span data-ttu-id="355f0-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="355f0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="355f0-111">Id</span><span class="sxs-lookup"><span data-stu-id="355f0-111">Id</span></span>  <br/> |<span data-ttu-id="355f0-112">Enthält eine Zeichenfolge, die einen Ordner im Exchange-Informationsspeicher identifiziert.</span><span class="sxs-lookup"><span data-stu-id="355f0-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="355f0-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="355f0-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="355f0-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="355f0-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="355f0-115">Enthält eine Zeichenfolge, die eine Version eines Ordners identifiziert, die durch das ID-Attribut identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="355f0-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="355f0-116">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="355f0-116">This attribute is optional.</span></span> <span data-ttu-id="355f0-117">Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Ordners verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="355f0-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="355f0-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="355f0-118">Child elements</span></span>

<span data-ttu-id="355f0-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="355f0-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="355f0-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="355f0-120">Parent elements</span></span>

|<span data-ttu-id="355f0-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="355f0-121">**Element**</span></span>|<span data-ttu-id="355f0-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="355f0-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="355f0-123">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="355f0-123">GetSharingMetadata</span></span>](getsharingmetadata.md) <br/> |<span data-ttu-id="355f0-124">Definiert eine Anforderung zum Abrufen eines nicht transparenten Authentifizierungstokens, das die Freigabeeinladung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="355f0-124">Defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="355f0-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="355f0-125">Remarks</span></span>

<span data-ttu-id="355f0-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste des Computers gehostet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="355f0-126">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="355f0-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="355f0-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="355f0-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="355f0-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="355f0-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="355f0-129">Schema Name</span></span>  <br/> |<span data-ttu-id="355f0-130">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="355f0-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="355f0-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="355f0-131">Validation File</span></span>  <br/> |<span data-ttu-id="355f0-132">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="355f0-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="355f0-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="355f0-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="355f0-134">False</span><span class="sxs-lookup"><span data-stu-id="355f0-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="355f0-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="355f0-135">See also</span></span>



[<span data-ttu-id="355f0-136">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="355f0-136">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="355f0-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="355f0-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

