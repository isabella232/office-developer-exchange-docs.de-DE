---
title: SharingFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharingFolderId
api_type:
- schema
ms.assetid: 5ad37ceb-2922-4420-9051-c29d0d57c420
description: Das SharingFolderId-Element stellt den Bezeichner des lokalen Ordners in einer Dateifreigabe Beziehung.
ms.openlocfilehash: e0eb1fbd7155040508daf253f5eb4b1352d7426d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831485"
---
# <a name="sharingfolderid"></a><span data-ttu-id="0f21d-103">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="0f21d-103">SharingFolderId</span></span>

<span data-ttu-id="0f21d-104">Das **SharingFolderId** -Element stellt den Bezeichner des lokalen Ordners in einer Dateifreigabe Beziehung.</span><span class="sxs-lookup"><span data-stu-id="0f21d-104">The **SharingFolderId** element represents the identifier of the local folder in a sharing relationship.</span></span> 
  
```xml
<SharingFolderId Id="" ChangeKey="" />
```

 <span data-ttu-id="0f21d-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="0f21d-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0f21d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0f21d-106">Attributes and elements</span></span>

<span data-ttu-id="0f21d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0f21d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0f21d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0f21d-108">Attributes</span></span>

|<span data-ttu-id="0f21d-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0f21d-109">**Attribute**</span></span>|<span data-ttu-id="0f21d-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0f21d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0f21d-111">Id</span><span class="sxs-lookup"><span data-stu-id="0f21d-111">Id</span></span>  <br/> |<span data-ttu-id="0f21d-112">Enthält eine Zeichenfolge, die einen Ordner im Exchange-Speicher identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0f21d-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="0f21d-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0f21d-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="0f21d-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="0f21d-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="0f21d-115">Enthält eine Zeichenfolge, die eine Version eines Ordners identifiziert, die von dem Id-Attribut angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0f21d-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="0f21d-116">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="0f21d-116">This attribute is optional.</span></span> <span data-ttu-id="0f21d-117">Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Ordners verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0f21d-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0f21d-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0f21d-118">Child elements</span></span>

<span data-ttu-id="0f21d-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="0f21d-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0f21d-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0f21d-120">Parent elements</span></span>

|<span data-ttu-id="0f21d-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="0f21d-121">**Element**</span></span>|<span data-ttu-id="0f21d-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0f21d-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0f21d-123">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="0f21d-123">RefreshSharingFolder</span></span>](refreshsharingfolder.md) <br/> |<span data-ttu-id="0f21d-124">Definiert eine Anforderung an den angegebenen lokalen Ordner zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0f21d-124">Defines a request to refresh the specified local folder.</span></span>  <br/> |
|[<span data-ttu-id="0f21d-125">GetSharingFolderResponse</span><span class="sxs-lookup"><span data-stu-id="0f21d-125">GetSharingFolderResponse</span></span>](getsharingfolderresponse.md) <br/> |<span data-ttu-id="0f21d-126">Definiert eine Antwort auf eine [GetSharingFolder Vorgang](getsharingfolder-operation.md) an.</span><span class="sxs-lookup"><span data-stu-id="0f21d-126">Defines a response to a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="0f21d-127">GetSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0f21d-127">GetSharingFolderResponseMessage</span></span>](getsharingfolderresponsemessage.md) <br/> |<span data-ttu-id="0f21d-128">Enthält den Status und das Ergebnis einer einzelnen Anforderung [GetSharingFolder Vorgang](getsharingfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="0f21d-128">Contains the status and result of a single [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f21d-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0f21d-129">Remarks</span></span>

<span data-ttu-id="0f21d-130">Das Schema, das dieses Element beschreibt befindet sich das virtuelle IIS-Verzeichnis, dass Hosts Exchange-Webdienste des Computers, auf dem Microsoft Exchange Server ausgeführt wird die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0f21d-130">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0f21d-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0f21d-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0f21d-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f21d-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0f21d-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0f21d-133">Schema Name</span></span>  <br/> |<span data-ttu-id="0f21d-134">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="0f21d-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0f21d-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0f21d-135">Validation File</span></span>  <br/> |<span data-ttu-id="0f21d-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0f21d-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0f21d-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0f21d-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="0f21d-138">False</span><span class="sxs-lookup"><span data-stu-id="0f21d-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0f21d-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f21d-139">See also</span></span>



- [<span data-ttu-id="0f21d-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0f21d-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

