---
title: RefreshSharingFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RefreshSharingFolder
api_type:
- schema
ms.assetid: 14571c28-effa-430a-802e-82fb99bafa7f
description: Das RefreshSharingFolder-Element definiert eine Anforderung an den angegebenen lokalen Ordner zu aktualisieren. Es ist das Basiselement für den Vorgang RefreshSharingFolder.
ms.openlocfilehash: b09e311d0ba38b0cdcc9fe0864ed3e2b0151b0fd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831043"
---
# <a name="refreshsharingfolder"></a><span data-ttu-id="54782-104">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="54782-104">RefreshSharingFolder</span></span>

<span data-ttu-id="54782-105">Das **RefreshSharingFolder** -Element definiert eine Anforderung an den angegebenen lokalen Ordner zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="54782-105">The **RefreshSharingFolder** element defines a request to refresh the specified local folder.</span></span> <span data-ttu-id="54782-106">Es ist das Basiselement für den [RefreshSharingFolder-Vorgang](refreshsharingfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="54782-106">It is the base element for the [RefreshSharingFolder operation](refreshsharingfolder-operation.md).</span></span>
  
```xml
<RefreshSharingFolder>   <SharingFolderId/></RefreshSharingFolder>
```

 <span data-ttu-id="54782-107">**RefreshSharingFolderType**</span><span class="sxs-lookup"><span data-stu-id="54782-107">**RefreshSharingFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="54782-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="54782-108">Attributes and elements</span></span>

<span data-ttu-id="54782-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="54782-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54782-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="54782-110">Attributes</span></span>

<span data-ttu-id="54782-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="54782-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="54782-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="54782-112">Child elements</span></span>

|<span data-ttu-id="54782-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="54782-113">**Element**</span></span>|<span data-ttu-id="54782-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="54782-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54782-115">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="54782-115">SharingFolderId</span></span>](sharingfolderid.md) <br/> |<span data-ttu-id="54782-116">Stellt den Bezeichner des lokalen Ordners in einer Dateifreigabe Beziehung dar.</span><span class="sxs-lookup"><span data-stu-id="54782-116">Represents the identifier of the local folder in a sharing relationship.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="54782-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="54782-117">Parent elements</span></span>

<span data-ttu-id="54782-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="54782-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54782-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="54782-119">Remarks</span></span>

<span data-ttu-id="54782-120">Das Schema, das dieses Element beschreibt befindet sich das virtuelle IIS-Verzeichnis, dass Hosts Exchange-Webdienste des Computers, auf dem Microsoft Exchange Server ausgeführt wird die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="54782-120">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="54782-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="54782-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54782-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="54782-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="54782-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="54782-123">Schema Name</span></span>  <br/> |<span data-ttu-id="54782-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="54782-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="54782-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="54782-125">Validation File</span></span>  <br/> |<span data-ttu-id="54782-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="54782-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="54782-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="54782-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="54782-128">False</span><span class="sxs-lookup"><span data-stu-id="54782-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="54782-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54782-129">See also</span></span>



- [<span data-ttu-id="54782-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="54782-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

