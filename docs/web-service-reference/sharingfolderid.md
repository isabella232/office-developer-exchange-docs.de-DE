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
description: Das SharingFolderId-Element stellt den Bezeichner des lokalen Ordners in einer Freigabebeziehung dar.
ms.openlocfilehash: 02780251639ee651ca65d8eadded43260852aaf8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526578"
---
# <a name="sharingfolderid"></a><span data-ttu-id="6d2f5-103">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="6d2f5-103">SharingFolderId</span></span>

<span data-ttu-id="6d2f5-104">Das **SharingFolderId** -Element stellt den Bezeichner des lokalen Ordners in einer Freigabebeziehung dar.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-104">The **SharingFolderId** element represents the identifier of the local folder in a sharing relationship.</span></span> 
  
```xml
<SharingFolderId Id="" ChangeKey="" />
```

 <span data-ttu-id="6d2f5-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="6d2f5-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6d2f5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6d2f5-106">Attributes and elements</span></span>

<span data-ttu-id="6d2f5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6d2f5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6d2f5-108">Attributes</span></span>

|<span data-ttu-id="6d2f5-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6d2f5-109">**Attribute**</span></span>|<span data-ttu-id="6d2f5-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6d2f5-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6d2f5-111">Id</span><span class="sxs-lookup"><span data-stu-id="6d2f5-111">Id</span></span>  <br/> |<span data-ttu-id="6d2f5-112">Enthält eine Zeichenfolge, die einen Ordner im Exchange-Informationsspeicher identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="6d2f5-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="6d2f5-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="6d2f5-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="6d2f5-115">Enthält eine Zeichenfolge, die eine Version eines Ordners identifiziert, die durch das ID-Attribut identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="6d2f5-116">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-116">This attribute is optional.</span></span> <span data-ttu-id="6d2f5-117">Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Ordners verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6d2f5-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6d2f5-118">Child elements</span></span>

<span data-ttu-id="6d2f5-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6d2f5-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6d2f5-120">Parent elements</span></span>

|<span data-ttu-id="6d2f5-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="6d2f5-121">**Element**</span></span>|<span data-ttu-id="6d2f5-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6d2f5-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6d2f5-123">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="6d2f5-123">RefreshSharingFolder</span></span>](refreshsharingfolder.md) <br/> |<span data-ttu-id="6d2f5-124">Definiert eine Anforderung zum Aktualisieren des angegebenen lokalen Ordners.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-124">Defines a request to refresh the specified local folder.</span></span>  <br/> |
|[<span data-ttu-id="6d2f5-125">GetSharingFolderResponse</span><span class="sxs-lookup"><span data-stu-id="6d2f5-125">GetSharingFolderResponse</span></span>](getsharingfolderresponse.md) <br/> |<span data-ttu-id="6d2f5-126">Definiert eine Antwort auf eine [GetSharingFolder-Vorgangs](getsharingfolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-126">Defines a response to a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="6d2f5-127">GetSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6d2f5-127">GetSharingFolderResponseMessage</span></span>](getsharingfolderresponsemessage.md) <br/> |<span data-ttu-id="6d2f5-128">Enthält den Status und das Ergebnis einer einzelnen [GetSharingFolder-Vorgangs](getsharingfolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-128">Contains the status and result of a single [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d2f5-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d2f5-129">Remarks</span></span>

<span data-ttu-id="6d2f5-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste des Computers gehostet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-130">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6d2f5-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6d2f5-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d2f5-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="6d2f5-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6d2f5-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6d2f5-133">Schema Name</span></span>  <br/> |<span data-ttu-id="6d2f5-134">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="6d2f5-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6d2f5-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6d2f5-135">Validation File</span></span>  <br/> |<span data-ttu-id="6d2f5-136">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6d2f5-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6d2f5-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6d2f5-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="6d2f5-138">False</span><span class="sxs-lookup"><span data-stu-id="6d2f5-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6d2f5-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d2f5-139">See also</span></span>



- [<span data-ttu-id="6d2f5-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6d2f5-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

